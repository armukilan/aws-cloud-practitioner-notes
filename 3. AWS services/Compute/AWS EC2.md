# AWS EC2

- Secure and resizable compute capacity for virtually any workload, Highly configurable virtual server
- It is designed to make web-scale computing easier for developers.
- Resizable compute capacity, takes minute to launch
- Allows you to launch VM (VM is an emulation of a physical computer usin software. Server virtualization allows you to easily create, copy, resize or migrate your server).
- Multiple VM can run on same physical server, so you can share the cost with others.
- When we launch a virtual machine, we call it an "instance"
- Highly configurable
	- Amount of CPU (Intel, AMD, and Arm processors)
	- Amount of RAM
	- Network bandwidth (400 Gbps Ethernet networking)
	- OS (Windows, Ubuntu, Amazon Linux, MAC) (An AMI - Amazon machine Image is a predefined configuration for a VM)
	- Attach multiple Block storage (EBS)
- EC2 is the backbone of AWS - most of the service use EC2 - S3, RDS, DynamoDB, Lambda (Anything and everything on AWS uses EC2 instance underneath)


## Steps

- Choose OS via Amazon Machine Image (AMI) - Redhat, Ubuntu etc.
- Instance type - t2.nano, t2.micro etc. 
- Add storage - SSD, HDD, Virtual Magnetic tape, Multiple volume
- Configure Instance - Security Group, Key pair, User Data, IAM, Placement group

## Instance Families

- instance families are different combinations of CPU memory storage and networking capacity 
- instance families allow you to choose the appropriate combination of capacity to meet your application's unique requirements 
- different instance families are different because of the varying Hardware used to give them their unique properties.
- Commonly instance families are called instance types, but an instance type is a combination of size and family


### Amazon EC2 Instance Types

- **General Purpose** 
	- A1, T2, T3, T3a, T4g, M4, M5, M5n, M6zn, m6g, m6i, Mac
	- balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. 
	- Applications that use these resources in equal proportions such as web servers and code repositories. 

- **Compute Optimized** - 
	- C5, C4, Cba, C5n, C6g, C6gn
	- Ideal for compute bound applications that benefit from high performance processors. 
	- Batch processing workloads, media transcoding, high performance web servers, high performance computing (HPC), scientific modeling, dedicated gaming servers and ad server engines, machine learning inference and other compute intensive applications.

- **Memory Optimized** - 
	- R4, R5, R5a, R5b, R5n, X1, X1e, High Memory, z1d
	- Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.
	- In-memory caches, in-memory database, real time big data analytics

- **Accelerated Computing** - 
	- P2, P3, P4, G3, G4ad, G4dn, F1, Inf1, VT1
	- Accelerated computing uses hardware accelerators, or co-processors
	- floating point number calculations, graphics processing, or data pattern matching, ML, Computer Finance, seismic analysis, speech recognization
(The Accelerated Computing instance category includes instance families that use hardware accelerators, or co-processors, to perform some functions, such as floating-point number calculation and graphics processing, more efficiently than is possible in software running on CPUs. Amazon EC2 provides a broad choice of accelerators including GPUs, purpose built AI chips AWS Trainium and AWS Inferentia, FPGAs and more.)

- **Storage Optimized** 
	- I3, I3en, D2, D3, D3en, H1
	- high, sequential read and write access to very large data sets on local storage. They are optimized to deliver millions of low-latency, random I/O operations per second (IOPS) to applications
	- NoSql, in-memory or transactional Db, data warehousing

- **HPC Optimized** - High performance computing (HPC) instances are purpose built to offer the best price performance for running HPC workloads at scale on AWS. HPC instances are ideal for applications that benefit from high-performance processors such as large, complex simulations and deep learning workloads.

**What are Amazon EC2 UltraServers** - Amazon EC2 UltraServers are ideal for customers seeking the highest AI training and inference performance for models at the trillion-parameter scale. UltraServers connect multiple EC2 instances using a dedicated, high-bandwidth, low-latency accelerator interconnect, so you can use a tightly coupled mesh of accelerators across EC2 instances and access significantly more compute and memory than standalone EC2 instances.

### Instance types

- Instance type is a particular instance size and instance family
- Common pattern - nano, micro, smaall, medium, large, xlarge, 2xlarge, 4xlarge, 8xlarge .....
- Exceptions - c6g.metal -Bare metal machine, c5.9xlarge
- Insatnce size - generally double in price and key attributes

## Dedicated Instance vs Dedicated Host

[Diference](dd1.png)

## Levels of Tenency

[Difference](dd2.png)

## Benefits of Amazon EC2

- **SLA commitment** : Access reliable, scalable infrastructure on demand. Scale capacity within minutes with SLA commitment of 99.99% availability.
- **AWS Nitro System** : Provide secure compute for your applications. Security is built into the foundation of Amazon EC2 with the AWS Nitro System.
- **Optimize performance and cost** : Optimize performance and cost with flexible options like AWS Graviton-based instances, Amazon EC2 Spot instances, and AWS Savings Plans.
- **AWS Migration Tools** : Migrate and build apps with ease using AWS Migration Tools, AWS Managed Services, or Amazon Lightsail. Learn how AWS can help.



## Nitro System

- A combination of dedicated hardware and lightweight hypervisor enabling faster Innovation and enhanced security 
- All new ec2 instant types use the nitro system
	- Nitro Cards : specialized cards for VPS, EBS, instant storage and controller cards
	- Nitro security chips : these are integrated into the motherboard protects Hardware resources
	- Nitro hypervisor : lightweight hyper visor memory and CPU allocation bare metal like performance
	- Nitro enclaves?


## Bare Metal Instance

- You can launch EC2 instances that have no hypervisor so you can run workloads directly on the hardware for maximum performance and control.
- We have the M5 and R5 EC2 instances that can run bare metal
- **Bottle rocket** This is a Linux based open source operating system that is purpose built by AWS for running containers on VMs or bare metal hosts


## Pricing Model

[Pricing Model](dd3.png)

### On-Demand

- the on demand pricing model is a pay as you go model where you consume compute and then you pay later 
- when you launch an ec2 instance by default you are using that on demand pricing 
- On Demand has no upfront payment and no long long-term commitment 
- you are charged by the second up to a minimum of 60 seconds so technically a minute or the hour 
- let's just talk about the difference between those uh per second billing and those per hour billing 
	- per second are for Linux, windows, windows with SQL Enterprise, windows with SQL standard, windows with SQL web instances that do not have a separate hourly charge 
	- everything else is going to be per hour 

- When you launch ec2 instance you can't tell when something is per second or per hour you just have to know that it has a separate hourly charge but generally you know if you're just launching things it's going to probably be the per sec billing when you look up the hourly or the uh the pricing it's always shown in the hourly rate so even if it is using uh per second billing when you uh look up that pricing it's always going to show it to you like that but on your bill you'll see it down to the second up to the first 60 seconds 

- on demand is great for workloads that are short term spiky or unpredictable 
- when you have a new app development this is where you want to experiment and then when you're ready to uh start saving because you know exactly what that workload is going to be over the span of a year or three that's where we're going to get into reserved instances


### Reserved Instances (RI)

- RI is designed for applications that have a steady state, predictable usage or required Reserve capacity
- Reduced pricing is based on term x Class offering x RI attributes x Payment option

	- Term: Idea here is the longer the term the greater the savings 
		- you're committing to a one-year or three-year contract with AWS 
		- These do not renew so at the end of the year, you have to renew
		- when they do expire your instances are just going to flip back over to On Demand with no interruptions to service

	- Class - the less flexible the offering the greater the savings 
		- standard this is up to a 75 reduction in the price compared to on demand and the idea here is you can modify some RI attributes 
		- convertible so you save up to 54% reduced pricing compared to on demand and you can exchange RI based on the RI attributes if the value is greater or equal in value 
		- schedule but this no longer exists so if you do come across it just know that AWS is not planning on offering this 

	- payment options so the greater upfront the greater the savings 
		- all upfront so full payment is made at the start of the term 
		- partial upfront a portion of the cost must be paid upfront and the remaining hours in the terms are built at a discounted rate
		- no upfront so you are billed at a discounted hourly rate for every hour within the term regardless of whether the reserved is being used 

- RI can be shared between multiple accounts within an organization 
- Unused RI can be sold in the reserved instance Marketplace 


- RI attributes (aka Instance attributes) are limited based on class offering and can affect the final price of an RI instance. There are 4 RI attributes:
	- instance type - like an M4 large and this is composed of an instance family so the M4 and the instance size so large 
	- region this is where the reserved instance is purchased 
	- Tenency whether your instance runs on shared so the default multi-tenant or a single tenant which would be dedicated hardware 
	- platform OS - Windows or Linux.

[EC2 Regional and Zonal RI](d4.png)

[EC2 Regional and Zonal Limits](dd5.png)


### Capacity Reservation

- EC2 instances are backed by different kinds of hardware and so there is a finite amount of servers of available within an availability Zone per instance type or family 
- remember an availability zone is just a data center or a collection of data centers and they only have so many servers in there so if they run out because the demand is too great you just cannot spin anything up and so that's what's happening you go to launch specific ec2 instant type but AWS is like sorry we don't have any right now.

- The solution to that is capacity reservation - a service of ec2 that allows you to request a reserve of EC2 instance type for a specific region and a AZ 
- The reserve capacity is charged at the selected instance type on demand rate whether an instance is running or not
- you can also use Regional Reserve instances With Your Capacity reservations to benefit from billing discounts

[Standard and convertible RI](dd6.png)


### RI marketplace

- allows you to sell your unused standard RI to recoup your spend for RI right you do not intend or cannot use 

- reserved instances can be sold after they have been active for at least 30 days and once AWS has received the upfront payment 
- you must have a US bank account to sell RI on the RI Marketplace 
- there must be at least one month remaining in the term for the RI you are listing 
- you will retain the pricing and capacity benefit of your reservation until it's sold and the transaction is complete 
- your company name and address upon request will be shared with the buyer for tax purposes 
- a seller can set Only The Upfront price of an RI. The usage price and other configurations such as instance type, availability Zone, platform will remain the same as when the RI was initially purchased 
- the term length will be rounded down to the nearest month for example a reservation with 9 months and 15 days remaining will appear as 9 months on the RI Marketplace 
- you can sell up to 20,000 USD in reserved instances per year
- reserved instances in the gov Cloud uh region cannot be sold on the ri Marketplace


### Spot Instance

- AWS has unused compute capacity that they want to maximize the utility of their idle servers 
- Idea is just like when a hotel offers booking discounts to fill vacant Suites or planes offer discounts to fill vacant seats 
- Spot instances provide a discount of 90% compared to On Demand pricing 
- spot instances can be terminated if the Computing capacity is needed by other on demand customers but from what I hear rarely rarely does spot instances ever get terminated 
- designed for applications that have flexible start and end times or applications that are only feasible at very low compute cost so you see some options here like load balancing workloads flexible workloads Big Data workloads 
- there is another service called **AWS batch** which is for doing batch processing and this is easy and convinient way to use spot pricing.
- there are some termination conditions 
	- instances can be terminated by AWS at any time 
	- if your instance is terminated by AWS you don't get charged for a partial hour of usage 
	- if you terminate an instance you will be still charged for an hour that it ran



### Dedicated Instances

[Dedicated Instances](dd7.png)

### Savings Plan

- Similar discounts as Reserved Instances, but simplifies the purchasing process.
- 3 Types - Compute savings plan, EC2 Instance savings plan, Sagemaker savings plan
- Terms - 1 year or 3 year
- Payment opt - All, partial or no upfront

- Compute 
	- compute savings plans provides the most flexibility and helps to reduce your cost by 66%. 
	- These plans automatically apply to ec2 instances usage, aAWS fargate, AWS Lambda service usage regardless of the instance family, size, AZ region, OS or tenency 

- EC2 instances
	- provides the lowest prices offering saving up to 72% in exchange for commitment to usage of individual instance families in a region 
	- so automatically reduce your cost on the selected instance family in the region regardless of AZ, size, OS, tendency gives you the flexibility to change your usage between instances with a within a family in that region 

- Sagemaker
	- Reduce Sage maker cost by up to 64% automatically apply to Sage maker usage regardless of instance family, size, component, AWS region


## Use cases

- **Run cloud-native and enterprise applications** - Amazon EC2 delivers secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs.
- **Scale for HPC applications** - Access the on-demand infrastructure and capacity you need to run HPC applications faster and cost-effectively.
- **Develop for Apple platforms** - Build, test, and sign on-demand macOS workloads. Access environments in minutes, dynamically scale capacity as needed, and benefit from AWS’s pay-as-you-go pricing.
- **Train and deploy ML applications** - Amazon EC2 delivers the broadest choice of compute, networking (up to 400 Gbps), and storage services purpose-built to optimize price performance for ML projects.




## High Performance Computing

- A cluster of a hundred of thousands of servers with fast connections between each of them with the purpose of boosting Computing capacity 
- When you need a supercomputer to perform computational problems too large to run on a standard computer or computers or would take too long.
- **AWS Parallel cluster** which is an AWS supported open source cluster management tool that makes it easy for you to deploy and manage higher performance Computing HPC clusters on AWS.


## Cost and Capacity Management

- Cost - How do we save money?
- Capacity - How do we meet the demand of traffic and usages through adding or upgrading servers

## EC2 spot instances reserved instances saving plans 

-  ways to save on Computing by paying up in full or partially or by committing to a yearly contract or multi-year contract or by being flexible about the availability and interruption to Computing Services 

## AWS batch 

- plans, schedules and executes your batch computing workloads across the full range of AWS computing Services which can utilize spot instances to save money 

## AWS compute Optimizer 

- suggest how to reduce cost and improve performance by using machine learning to analyze your previous usage history.

## EC2 auto scan groups (ASGs) 

- Automatically add or remove EC2 servers to meet the current demand all of traffic 
- They will save you money and meet capacity since you only run the amount of servers you need 

## Elastic load balancer 

- This distributes traffic to multiple instances, can reroute traffic from unhealthy instances to healthy instances and can route traffic to EC2 instances running in different availability zones

## Elastic Beanstalk (ELB)

- ELB is for easy deploying web applications without developers having to worry about setting up and understanding the underlying ad Services. 
- Similar to Heroku 