# AWS Identity and Access Management (IAM)

- Create and manage AWS users and groups and use permissions to allow and deny their access to AWS 


## Componenets

- IAM policies : so these are Json documents which Grant permissions for specific user, groups or a role to access services. policies are attached to IAM identities 
- IAM permissions : an API action that can or cannot be performed and they represented in the IAM policy document.

## IAM identity 

- IAM users: These are end users who log into the console or interact with AWS resources programmatically or via clicking UI interfaces 
- IAM groups: group up your users so they all share the same permission levels of the group maybe it's admins, developers or Auditors 
- IAM roles: so these roles Grant AWS resources permissions to specific AWS API actions and Associate policies to a role and then assign it to an AWs resource just understand that roles are when you're attaching these to resources so like if you have an ec2 instance and you say it has to access S3 you're going to be attaching a a role not a policy directly

## Anatomy of IAM policy

- IAM policy are writtern in JSON, and contain all the permission which determines what API are allowed or denied.

[Anatomy](id2.png)

## Principle of least previlege

- Principle of least privilege is the computer security concept of providing a user role or application the least amount of permissions to perform an operation or an action
	- Just enough access (JEA) permitting only the exact actions for the identity perform a task 
	- Just in time (JIT) permitting the smallest length of duration an identity can use permissions

## Risk-based adaptive policies 

- Each attempt to access a resource generates a risk score of how likely the request is to be from a compromized source 
- The risk score could be based on many factors such as device, user location, IP address, what service is being accessed and when 
- AWS does not have a risk-based adaptive policies built into IAM you can roll your own 
- ConsoleMe so this is an open- Source Netflix project to self-serve short-lived IAM policies so an end user can access AWS resources while enforcing JEA and JIT Link: [Github](https://github.com/Netflix/consoleme)

## AWS Root User

- AWS account and the account which holds all the AWS resources including the different types of user 
- Root user a special account with full access that cannot be deleted 
- user this is a user for common tasks that is assigned permissions

- AWS account root user is a special user who's created at the time of the AWS account creation 
- The root user account uses an email and password to log in as opposed to the regular user who's going to provide their account ID/ alias, username and password 
- the root user account cannot be deleted 
- the root user account has full permissions to the account and its permissions cannot be limited 
	- if you take an IAM policy to explicitly deny the root user access resources it's not something you can do 
	- however you can do it in the case of AWS organizations service control policies (SCP) because a service control policy applies to a bunch of accounts so it just it's one level above and so that is a way of limiting root users but generally you can't limit them within their own account 
- There can only be one root user per AWS account 
- the root user is instead for very specific and specialized tasks that are infrequently or rarely performed 
- Root account should not be used for daily or common tasks 
- it's strongly recommended to never use the root users access keys because you can generate those and use them 
- it's strongly recommended to turn on MFA for the root user 

- Administrative  tasks that only the root user can perform 
	- changing your account settings *
		- this includes account name, email address, root user password, root user access Keys 
		- other account settings such as contact information, payment currency preference, regions do not require the root user credentials 
	- Restore IAM user permissions 
		- if there's an IAM admin who accidentally revokes their own permissions you can sign into the root user to edit policies and restore those permissions 
	- you can also activate IAM access to the billing and cost Management console 
	- you can view certain tax invoices 
	- you can close your AWS account *
	- you can change or cancel your AWS support plan *
	- register as a seller in the reserved instance Marketplace 
	- enable MFA delete on S3 buckets 
	- edit or delete an Amazon S3 bucket policy that includes an invalid VPC ID or VPC endpoint ID 
	- sign up for govcloud 
	- something that's not in here which this I took this from the documentation - you can use the AWS root account user to create the organization you can't create that with any other user.

* Important for exams

## AWS SSO

- AWS SSO is where you create or connect your Workforce identities in AWS once and manage access centrally across your aws organization.
- Choose your identity Source 
	- AWS SSO 
	- active directory 
	- SAML 2.0 IDP 
- you're going to manage user permission centrally 
	- AWS accounts 
	- AWS applications
	- SAML application 
- Users can you get single click access to all these things

[Identity](id3.png)
