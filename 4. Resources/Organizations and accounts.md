# Organizations and accounts 

- AWS organizations allow the creation of new AWS accounts and allows you to centrally manage billing, control access, compliance, security and share resources across your AWS accounts
- Root account user is a single signin identity that has complete access to all AWS services and resources in an account. Each account has a root account user
- Generally you will have a master or root account and even within that you'll have a root account user and for every additional account that you have you'll notice over here we have a root account user 

- Organizational unit these are commonly abbreviated to OU so they are a group of AWS accounts within an organization which can contain other organizational units creating a hierarchy so here is one where we have called Starfleet and here's one called Federation planets and underneath we have multiple accounts (accounts within that organizational unit) and even though it does not show it here you can create an organizational unit within an organizational unit 

- Service control policies (scps) and these give Central control over the allowed permissions for all AWS accounts in your organization helping to ensure your accounts stay within your organization's guidelines
- There's this concept of AWS IAM policies and all you're doing is you're creating a policy that's going to be uh organizational uniwide or organizational wide or for select accounts so it's just a way of applying I am policies across multiple accounts 

- AWS organizations must be turned on and once it's turned on it cannot be turned off it's generally recommended that you do turn it on because basically when if you're going to run any kind of serious workload you're going to be using AWS organizations to isolate your AWS accounts based on workloads 
- You can create as many AWS accounts as you like - one account will be the master or root account and I say root account here because this is the new language here and some of the documentation still calls it master account so just understand this is the root account not to be confused with the root account user so another clarification 

- AWS account is not the same as a user account which is another thing that is confusing so when you sign up for AWS you get AWS account and then it creates you a user account which happens to be a root user account

[Organization](org1.png)


# AWS Control Tower

- AWS control tower helps Enterprises quickly set up a secure AWS multi-account and provides you with a baseline environment to get started with a multi-account architecture 

- Landing Zone 
	- this is a baseline environment following well architected and best practices to start launching production ready workloads
	- AWS SSO enabled by default so it's very easy to move between AWS accounts, it will have centralized logging for AWS cloud trail so that you know they're going to be tamper evident or tamper proof away from your workloads where they can't be affected and it'll have cross account security auditing 

- Account Factory
	- They call this a vending machine but uh they changed it to account Factory 
	- The idea is that it automates provisioning of new accounts in your organization 
	- it standardizes the provisioning of new accounts with pre-approved account configuration 
	- you can configure account Factory with pre-approved Network configuration and region selections 
	- enable self-service for your Builders to configure and provision to accounts using AWS service catalog (AWS service catalog is just pre-approved workloads via Cloud information templates you created to to allow to launch this Server these resources 

- Guard rails
	- prepackaged governance rules for security, operations, compliance, that customers can select and apply enterprise-wide or to specific groups of accounts 

- AWS control tower is the replacement of the retired AWS Landing zone so if you remember AWS Landing zones which was never a self serve easy thing to sign up for it required a lot of money.

# AWS Config

## Change Management

- Change management in the context of cloud infrastructure is when we have a formal process to 
	- monitor changes 
	- enforce changes 
	- remediate changes

- compliances code (CAC) 
	- CAC is when we utilize programming to automate the monitoring, enforcing and remediating changes to stay compliant with the compliance program or expected configuration. 


## AWS config 

- a compliances code framework that allows us to manage change in your AWS accounts on a per region basis meaning that you have to turn this on for every region that you need it for 
- simple example where let's say we create a config Rule and we have an ec2 instance and we expect it to be in a particular State and then in the other case we have an RDS instance and it's in a state that we do not like so the idea is that we try to remediate it to put it in the state that we want it to be and those config rules are just powered by lambdas as you can see based on the Lambda icon there.

[AWS config](org2.png)

## When should you use AWS config 

- I want this resource to stay configured a specific way for compliance 
- I want to keep track of configuration changes to resources 
- I want a list of all resources within a region 
- I want to analyze potential security weaknesses and you need detailed historical information


# AWS Quick Starts

- I think this is now renamed as AWS solutions library. (Not sure)

- AWS quick starts are pre-built templates by AWS and AWS partners to help deploy a wide range of stacks 
- It reduces hundreds of manual procedures into just a few steps 

- Quick Start is composed of three parts it has a 

	- reference architecture for the deployment 
	- AWS cloud formation templates that automate and configure the deployment
	- a deployment guide explain the architecture implementation in detail

	- example of one that you might want to launch like the AWS Q&A bot and then you will get an architectural diagram and a lot of information about it and from there you can just go press the button and launch this infrastructure 

	- Most quick start reference deployments enable you to spin up a fully functional architecture in less than an hour

# Tagging

- Tag is a key and value pair that you can assign to AWS resource 
- as you are creating a resource it's going to prompt you to say hey what tags do you want to add you're going to give a key you're going to give a value 
- some examples could be something like based on Department, status, team, environment, project, location

- Tags allow you to organize your resources in the following way 
	- resource management - specific workloads, environments eg.developer environments 
	- cost management and optimization - cost tracking, budgets and alerts 
	- operations management - business commitments and SLA operations eg.Mission critical Services 
	- security - classification of data security impact 
	- governance and Regulatory Compliance 
	- automation 
	- workload Automation 

- it's important to understand that tagging can be used in Junction with IAM policy so that you can restrict access or things like that based on those tags

# Resource Groups

- A collection of resources that share one or more tags or another way to look at it is a way for you to take multiple tags and organize them into resource groups. 
- it helps you organize and consolidate information based on your project and the resources that you use 
- resource groups can display details about a group of resources based on metrics, alarms, configuration settings 
- at any time you can modify the settings of your resource groups to change what resources appear 
- There is a service called Resource groups and tag editor

# Business Centric Services

[Additional](org3.png)