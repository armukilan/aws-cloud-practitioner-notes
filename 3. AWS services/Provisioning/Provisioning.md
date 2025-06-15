# Provisioning

[Basics](prov1.png)

# Platform as Service

- Platform as a service allows customers to develop, run and manage applications without the complexity of building and maintaining the infrastructure typically associated with developing and launching an app 


# AWS Elastic Beanstalk

- Elastic Beanstalk is a PaaS for deploying web apps with little to no knowledge of the underlying infrastructure so you can focus on writing application code instead of setting up an automated deployment pipeline or devops tasks 

- Choose a platform, upload your code and it runs with little knowledge of the infrastructure 
- AWS us will say that it's generally not recommended for production application (this for Enterprises and large companies) 
- if you're a small to medium company you can run elastic beanstalk for quite a long time it'll work out 

- Elastic beanstalk is powered by cloud formation templates and it sets up for you: 
	- elastic load balancer 
	- Auto scaling group 
	- RDS database
	- ec2 instances preconfigured for particular platforms
	- monitoring integration with cloudwatch, SNS 
	- deployment strategies like in-place, blue/green deployment 
	- security built in so it could rotate out your passwords for your database
	- Can run dockerized envs

	- when we talk about platforms you can see we have Docker, multicontainer Docker, go, .net, Java, nodejs, Ruby, PHP, python, Tomcat, go  - a bunch of stuff and just to kind of give you that architectural diagram to show you that it can launch of multiple things

