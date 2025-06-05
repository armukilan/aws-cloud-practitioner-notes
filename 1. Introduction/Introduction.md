# Introduction

## What is cloud computing?

Cloud computing is the on-demand delivery of compute power, database, storage, applications,
and other IT resources through a cloud services platform via the internet with pay-as-you-go
pricing. Whether you are running applications that share photos to millions of mobile users or
you’re supporting the critical operations of your business, a cloud services platform provides rapid
access to flexible and low-cost IT resources. With cloud computing, you don’t need to make large
upfront investments in hardware and spend a lot of time on the heavy lifting of managing that
hardware. Instead, you can provision exactly the right type and size of computing resources you
need to power your newest bright idea or operate your IT department. You can access as many
resources as you need, almost instantly, and only pay for what you use.
Cloud computing provides a simple way to access servers, storage, databases and a broad set of
application services over the internet. A cloud services platform such as Amazon Web Services
owns and maintains the network-connected hardware required for these application services, while
you provision and use what you need via a web application.

## History

- Dedicated Server - One physical machine, dedicated to a single business. Runs a single app, website - Very expensive, high maintainance, High security
- Virtual Private Server - One physical machine, dedicated to a single business. Physical machine virtualized into sub-machines, runs multiple web apps, better utilization, isolation of resources
- Shared Hosting - Onephysical machine, shared by hundred of business, relies on most people under-utilizing resource, cheap, limited functionality, poor isolation
- Cloud - Multiple Physical machine - act as one system, system abstracted into multiple cloud service. Flexible, Scalable, Secure, Cost-effective, High configurability

## AWS

launched in 2006

SQS - 2004
S3 - 2006 Maarch
EC2 - 2006 August
All amazon.com to cloud - November 2010
AWS certification - April 2013

## CSP - Cloud Service provider
CSP provides
- company which provides multiple cloud services ranging from tens to hundreds of services 
- cloud services can be chained together to create cloud architectures 
- cloud services are accessible via a single unified API eg. AWS API and from that you can access the CLI the SDK
- those cloud services utilize metered building based on usage so this could be per second per hour uh vpcu memory storage
- cloud services have Rich monitoring built in so you know every API action is tracked and you have access to that so this case it's a cloud trail
- cloud services have infrastructure as a service offering (IAAS) that means they have networking, compute, storage databases
- those cloud services offers automation via infrastructure (IAC) as code so you can write code to set everything up

Note:  if a company offers multiple cloud services under a single UI but do not meet most of or all of these requirements it would just be referred to as a cloud platform eg. twilio, Hashi Corp or datab bricks 
those are Cloud platforms and AWS, Azure gcp are cloud service providers 

## landscape of CSP

Tier -1 - (Top)Early to market, wide offering, strong synergies, well recognized - AWS, Azure, GCP, Alibaba Cloud
Tier -2 - (Mid)backed by well known companies, slow to innovate and turned to specialization - IBM cloud, Oracle cloud, Huawei cloud, tencent cloud
Ter - 3 - (Light)VPS turned to offer core IaaS service, simple, cost-effective - Vultr, Diital ocean, akamai
Tier - 4 - (Private)Infrastructure as service software deployed to run in organization own private data - Openstack, Apache cloudstack, Vmware vsphere

## Gartner Magic Quadrant for Cloud

Gardner magic quadrant for cloud is a series of market research reports published by the IT consulting firm Gartner that rely on proprietary qualitative  data analysis methods to demonstrate market trends such as Direction, maturity and participants.

## Common cloud service

a cloud service provider can have hundreds of cloud services that are grouped into various types of services but the four most common types of cloud services for infrastructures of service / four core for Infrastructure as service is compute, storage, networking and DB.
AWS has 200+ services

In AWS - Compute - EC2, Storage - EBS, Database - RDS, Networking - VPC

## Evolution of computing

### Dedicated

-physically a physical server wholly utilized by single customer that's considered single tenant and uh for Google Cloud we're talking about um single node clusters and bare metal machines where you have control of the virtualization so you can install any kind of hypervisor or virtualization you wanted the system 

-the trade-off here though is that you have to guess upfront what your capacity is going to be and you're never going to 100% utilize that machine because it's going to have to be a bit under in case the utilization goes up that's you're choosing the CP use and 

-the memories you're going to end up overpaying because you're uh you'll have under underutilized server 

- it's not going to be easy to vertically scale it's not like you can just say resize it because the machine you have is what you have right you can't add more I mean I suppose they can insert more memory for you but that's a manual migration uh so it's very difficult um and replacing the server is also very difficult 

- you're limited by the host operating system it's not virtualized so whatever is on there is on there um and that's that's what 

- your apps are going to have access to if you decide to run more than one app which is not a good practice for these kind of machines uh you're going to end up with uh resource sharing where one machine might utilize more than the others 

- technically with a dedicated machine you have a guarantee of security privacy and full utility of the underlying resource (but it's up to you to make sure that it's more secure so you have that's up to your skills of security right whereas if you had a virtual machine or anything above that there's more responsibility on the cloud service provider to just provide a secure machine and they can do a better job than you so why would you use a dedicated machine well maybe you're doing high performance Computing where you need these machines like very close together and you have to choose what kind of virtualization you need to have)


### VM

- Run multiple VM in one machine
- Hypervisor - software layer that runs the VM
- Physical server shared by multiple customer
- Pay for fraction of server
- operpay for underutilized VM
- Limited by guest OS
- Multiple apps on single VM can result in resource sharing
- Easy to export or import images for migration
- easy to vertical or horizontality scale

### Containers

-  a virtual machine running these things called containers
- Docker deamon is the name of software layer lets you run multiple containers
- you can maximize the uh the the capacity because you can easily add new containers resize those containers use up the rest of the space it's a lot more flexible and more cost-effective
- containers will share the same underlying OS but they are more efficient than multiple VM
- multiple apps can run side by side without being limited uh by the the same OS requirements and not cause conflicts during resource sharing so containers are really good but you know the tradeoff is there a lot more work to maintain

### Functions
- Managed VM running managed containers
- Serverless compute
- Upload piece of code, choose the amount of memory and duration
- Responsible for code and data, nothing else
- Cost-effective, pay only for the time code is running, VM runs only if there is code to be executed
- Cold starts is side effect


## Types of Cloud Computing

best way to represent this is a stacked pyramid and we'll start our way at the top 
- SAAS also known as software as a service so this is a product that is run and managed by the cloud service provider you don't have to worry about how the service is maintained, it just works and available eg. Salesforce, gmail, office 365
- PAAS SAS is generally designed for customers in mind then came along platforms of service um also known as PAAS and these focus on the development or sorry the deployment and management of your apps so you don't worry about provisioning configuring or understanding the hardware or operating system eg. Elastic beanstalk, heroku, google app engine
- IAAS the basic building blocks for cloud it it provides access to networking features computers and data storage space and the idea here is you don't worry about the IT staff data centers and hardware and so that would be like Microsoft Azure AWS Oracle Cloud things like that and these are for administrators Eg. Azure, AWS, Oracle cloud


## Cloud deployment model

- Public CLoud - Everything (The workload or project is built on CSP), cloud native or cloud first
- Private - Everything on premises, built in company. These cloud could be openstack
- Hybrid - Using both On-premise and a cloud provider
- Cross cloud - Multiple cloud providers aka multi cloud - AWS EKS - Azure Arc - GCP Kubernetes Engine 


## AWS Free Tier

There is always free tier available
To check - Click your name at top right -> My billing Dashboard -> Billing Preferences -> Click receive free tier usage alerts and give your email address

## Computing power

The throughput measured at which a computer can complete a computational task