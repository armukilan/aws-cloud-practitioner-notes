# AWS API

- Software that allows 2 applications/services to talk to each other. 
- The most common type of API is via HTTP/S request

- API request is an HTTP API and you can interact by sending HTTPS request, using an application interacting with API like postman

- Each AWS service has its own service endpoint which you send request

- To authorize, you will need to generate a signed request.
- You make a reseperate request with your AWS credential and get back a token.

-You need to also provide an ACTION and accompanying parameters as a payload.

- Rarely do users directly send HTTP requests directly to AWS API. It s much easier to interact with the API via a variety of Developer tools. eg. AWS Management console, AWS SDK, AWS CLI


## AWS Management Console

- Web based unified console build, manage and monitor everything from simple web app to complex cloud deployment 9console.aws.amazon.com)
- Manually launch everything, with limited programming knkwledge. Also called clickops, since you perform everything with clicks

## Service console

- AWS service console each have their own customized console
- Find it by searching by their name
- Some AWS service console will act as umbrella containing many AWS service - eg. VPC, EC2, system manager, sagemaker, cloudwatch (console)

## AWS account ID

- Every AWS account has a unique account ID
- Drop down the current user in the console in the global navigation
- 12 digits.
- Used when:
	- Logging in with non-root user account
	- Cross-account roles
	- Support cases
- Keep the ID private,as it is one of the component used to identitfy an acocunt and attack
- It is available in IAM too.
- Ex. Cross account role in IAM, Policy in IAM

## AWS tools for Power shell
- task automation and configuration management   framework.
- A command line shell and a scripting language
- Poweshell built on top of .NET common language runtime (CLR) and accepts and returns .NET objects.
- AWS tools for powershells lets you interact with the APS API via powershell commandlets
- A commandlet is a special type of command in powershell in the form of capitalized  verb-and-noun eg. New-S3Bucket
- Powershell is in both Windows as well as AWS (Refer docs for powershell in AWS docs)

## AWS resource Name
- ARN uniquely identify AWS resource.
- Required to specify a resource unambigously across all AWS.
- Types:
	- arn:partition:service:region:account-id:resource-id
	- arn:partition:service:region:account-id:resource-type/resource-id
	- arn:partition:service:region:account-id:resource-type:resource-id
- Partition:
	- aws - AWS region
	- aws-ch - China
	- aws-us-gov - AWS Govcloud
- Service - identifies the service - s3, ec2
- account id
- resource id - name or path eg. user/Bob, instance/i-62342389dsjskjd832
- You can copy fro AWS management console
- Resource ARN could include path
- Path includes a wildcard character, namely an astreick
- eg. We use ARN in case of some 

## AWS CLI

- Proccess command to a computer program in the form of lines of text.
- OS implement a command-line interface in a shell.
- Terminal - Text only interface
- Console - Physical computer to physically input information into a terminal
- Shell - Command line program that users interact with to input commands. Popular shell programs - Bash, Zsh, powershell
- People use terminal, shell, console to generally describe interacting with shell

- AWS CLI - Users to programatically interact with AWS API via entering single or multi-line commands ito shell or terminal.
- AWS CLI - Python executable, Python is required to install AWS CLI
- AWS CLI can be on windows, MAC or Linux, name of cli program is aws
- You can use gitpod.io, console.aws.amazon.com, or download and install AWS CLI

## AWS SDK

- SDK - Collection of software development tools in one installable package
- Can use AWS SDK to programatically create, modify, delete or interact with AWS resources
- AWS SDK - various languages - Java, Py, Node.js, Ruby, Go, .NET, PHP, JS, C++ 
- Resourse - Goto AWS SDK in Google search

## AWS Cloudshell

- Browser based shell built into AWS console.
- Scoped per region, sanme credential as logged in user. free service
- Pre installed tools - AWS Cli, py, node.js, make. pip. sudo, tar, tmux, vim, wget, zip and more 
- 1 GB of storage free per AWS region
- FIles saved in home directory are available for future sessions in same region
- Shell env - Switch b/w Bash, Powershell, Zsh
- Available in select region

## Infrastructure as Code (IaC)

- this allows you to write a configuration script to automate creating updating or destroying your Cloud infrastructure
- blueprint of your infrastructure
- it allows you to easily share version or inventory your Cloud infrastructure
- two different offerings for IAC

	- AWS CloudFormation (CFN) - a declarative I tool
		- declarative means what you see is what you get 
		- it's explicit
		- more verbose but uh there is zero chance of misconfiguration unless the file is so big that you're missing something
		- Use scripting language eg.  Json yaml XML
	- AWS Cloud Kit Development (CDK) - Imperative tool
		- you say what you want and the rest is filled in 
		- it's implicit
		- less verbose you could end up with some misconfiguration
		- it does more than declarative
		- favorite programming language maybe python JavaScript


## AWS CloudFormation

- cloud formation allows you to write infrastructure as code as either Json or yaml
- The reason why it was adus started with Json and then everybody got sick of writing Json and so they introduced jaml which is a lot more concise 
- cloud formation is simple but it can lead to large files or is limited in some regards to creating Dynamic repeal infrastructure compared to cdk
- Cloud information can be easier for devops engineers who do not have a background in web programming languages
- since cdk generates out cloudformation it's still important to be able to read and understand Cloud information in order to debug IaC stacks

## AWS toolkit for VSCode

- AWS toolkit is an open-source plugin for VSCode to create, debug and deploy AWS code.
- AWS explorer : Explore wide range of AWS resources linked to your account
- AWS CDK explorer: Allows you to explore your stacks defined by CDK
- Amazon ECS: Provides Intellisense for ECS task-defined definitions.
- Serverless applications: Create, debug and deploy serverless apps via SAM and CFN 

## Access Keys

- Key and secret required to have programmatic access to AWS resource while interacting with the AWS API outside the AWS management console
- An access key is commonly referred to as AWS credentials

- Never share your access keys
- Never commit access keys to a codebase
- You can have two active access keys
- You can deactivate access keys
- Access keys have whatever access a user has to AWS resource.
- Access keys are to be stored in *~/.aws/credentials* account
- Default will be the access key when no profile is displayed
- You can store multiple access keys by giving the profile names
- You can use aws configure CLI command to populate the credential file
- The AWS SDK will automatically read from these Env variable
- This si the safe way of using an access key within your code.


