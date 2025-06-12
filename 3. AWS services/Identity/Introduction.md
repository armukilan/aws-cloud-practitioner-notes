# Zero Trust Model

- The Zero trust model operates on the principal of "Trust no one, verify everything"
- Malicious actors being able to bypass conventional access controls demonstrates traditional security measures are no longer sufficient

- In the zero trust model, Identity becomes the primary security perimeter.

## What do we mean by primary security perimeter 

- The primary or new security perimeter defines the first line of defense and it's security controls that protect a company's Cloud resources and assets 

## Network Centric (Old-way)

- traditional security focused on firewalls and VPN since there were few employees or workstations outside the office or they were in a specific remote office

## Identity-Centric (New-Way)

- Bring your own device, remote workstations which are becoming more common, we can't always trust that the employee is in a secure location, we have identity based security controls like MFA, providing provisional access based on the level risk from where, when and what a user wants to access 

- Identity Centric does not replace but it augments Network Centric security so it's just an additional layer of consideration for security when we're thinking about our AWS Cloud workloads 


# Zero Trust on AWS

- Zero trust has to do a lot with identity security controls and so let's talk about what is at our disposal on AWS 
- AWS have identity and access management IM this is where we create users or groups or policies 
	- Policy is a set of permissions that allow you to say this user is allowed to use these services with these particular actions
	- permission boundaries - say these aren't the permissions the user has currently but these are the boundaries to which we want them to have so they should never have access ML services and if someone's to apply them permissions it'll always be within these boundaries
	- service control policies (organization-wide policies) so if you have a policy where you don't want anyone to run anything in the Canada region you can apply that policy at the organizational level and it will be enforced then within an policy 
	- IAM policy conditions little knobs you can tweak to say how do I control based on a bunch of different factors so there's 
		- aws:SourceIP: Source IP so restrict where the IP address is coming from
		- aws:ReuestedRegion: a requested region so restrict based on the region as we just mentioned as an example 
		- aws:MultiFactorAuthPresent: so restrict if MFA is turned off 
		- aws:CurrentTime: current time so restrict access based on time of day maybe you know your employees should never be really using things at night and so that could be an indicator that someone is doing something malicious so you know only give them access during a certain time a day

- AWS does not have a ready to use identity controls that are intelligent which is why AWS is considered not to have a true zero trust offering for customers and third party services need to be used.

- Here where we have a collection of AWS services that can be set up in an intelligence-ish detection of identity concerns but requires expert knowledge. 
	- AWS CloudTrial: Tracks all API calls 
	- Amazon guard Duty: Intrusion detection and protection system so it could detect suspicious or malicious activity on those cloud trail logs and other logs 
	- Amazon detective: Analyze, investigate and quickly identify security issues that it could ingest from guard duty
	- AWS Cloud Trial -> Amazon Guardduty -> Amazon Detective


## Zero Trust on AWS with Third Party

- AWS does technically implement a zero trust model but does not allow for intelligent identity security controls 
- you can do it but it's a lot of work so uh let's kind of compare it against kind of a third party where we would get the controls that we would not necessarily get with AWS 

- Example Azure active directory has a real time and calculated risk detection Based on data points than AWS and this is based on 
	- device and application 
	- time of day 
	- location 
	- whether MFA is turned on
	- what is being accessed and 
	- the security controls verification or logic restriction is much more robust 

- This is where third party Solutions are going to come into play so you have 
	- Azure active directory 
	- Google Beyond Corp
	- Jump Cloud 
	- all these have more intelligent security controls for realtime detection 
	- You use AWS single Sign On to connect those directories to your AWS account

## Directory Service

- It's a service that Maps the names of network resources to network addresses 
- A directory service is shared information infrastructure for locating, managing, administrating and organizing resources such as volumes, folders, files, printers, users, groups, devices, telephone numbers and other objects 
- A directory service is a critical component of a network operating system - A directory server or a name server is a server which provides a directory service 

- Each resource on the network is considered an object by the directory server
- Information about a particular resource is stored as a collection of attributes associated with that resource or object 
- Well-known directory Services would be
	- domain name service - the directory service for the internet 
	- Microsoft active directory - they have a cloud hosted one called Azure active directory 
	- apache directory service 
	- Oracle internet directory (OID) 
	- OpenLDAP 
	- Cloud Identity 
	- Jump Cloud

## Actice Directory

- Microsoft introduced active directory domain services in Windows 2000 to give organizations's ability to manage multiple on- premise infrastructure components and systems using a single identity per user.

[Identity](id1.png)

## Identity Providers (IdP)

- Identity provider is a system entity that creates, maintains and manages identity information for principles and also provides authentication services to Applications within a federation or distributor Network 
- Trusted provider of your user identity that lets you use authenticate to access other service 
- identity providers - Facebook, Amazon, Google, Twitter, GitHub, LinkedIn. 

- Federate identity is a method of linking a user's identity across multiple separate identity management systems. 
	- OpenID so this is an open standard and decentralized Authentication Protocol allows you to be able to log in to different social media platforms using Google or Facebook account open ideas about providing who you are 
	- OAuth2.0 this is an industry standard protocol for authorization oath doesn't share password data but instead uses authorization tokens to prove an identity between consumers and service providers oath is about granting access to functionality
	- SAML the security assertion markup language which is an open standard for exchanging authentication and authorization between an identity provider and a service provide. Important use for SAML is single sign on Via the browser.


## Single-Sign-On

- single sign (SSO) is an authentication scheme that allows a user to log in with a single ID and password to different systems and software. 
- SSO allows IT departments to administer a single identity that can access many machines and cloud services 

- Eg. Azure active directory this is just an example of a very popular one 
- You use samle to do SSO and you can connect to all things - Google workspaces, Salesforce or your computer
- idea here is uh once you log in you don't have to log in multiple times 
- so you log into your primary directory and then after that you're not going to be presented with a login screen some Services might show an intermediate screen but the idea is you're not entering your credentials in multiple times.

## LDAP

- lightweight directory access protocol is an open, vendor neutral, industry standard application protocol for accessing and maintaining distributed directory information Services over uh IP network 
- A common use of LDAP is to provide a central place to store usernames and passwords 
- LDAP enables for same signon 
- same sign on allows users to use a single ID and password but they have to enter it every single time they want to log in so maybe you have your on premise active directory and then it's going to store it in that LDAP  and so the idea is that you know all these services like Google, kubernetes, jenkings is going to deal with that ldap server 

## Why would you use ldap over SSO which is more convenient or seamless 

- Most SSO systems are using LDAP under the hood 
- LDAP was not designed natively to work with web applications
- some systems only support integration with LDAP and not SSO so you got to take what you can get

## MFA

- MFA is a security control where after you fill in your user's name and email password you have to use a second device such as a phone to confirm that it's you that is logging in 
- MFA protects against people who have stolen your password 
- MFA is an option in most Cloud providers and even social media websites such as Facebook 
- The idea is I have my uh username or email and password I'm going to try to log in this is the first factor and the second Factor multiactor is I'm going to use a secondary device so maybe my phone we're going to enter in different codes or maybe it's passwordless so I just have to press a button to confirm that it's me and then I'll get access so in the context to AWS it's strongly recommended that you turn on MFA for all your accounts especially the AWS root account

## Security Keys

- security key is a second device used as a second step in authentication process to gain access to a device workstation or application
- a security key can resemble a memory stick and when your finger makes contact with a button of exposed metal on the device it will generate and autofill a security token 
- a popular brand of security Keys is the Yubikey 

- it works out of the box with Gmail Facebook and hundreds more 
- supports FIDO2/Webauthn, U2F 
- it's waterproof and crust resistance 
- USB-A and NFC dual connectors on a single key