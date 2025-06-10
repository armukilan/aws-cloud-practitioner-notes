# AWS EC2

- Secure and resizable compute capacity for virtually any workload
- It is designed to make web-scale computing easier for developers.
- Allows you to launch VM (VM is an emulation of a physical computer usin software. Server virtualization allows you to easily create, copy, resize or migrate your server).
- Multiple VM can run on same physical server, so you can share the cost with others.
- When we launch a virtual machine, we call it an "instance"
- Highly configurable
	- Amount of CPU (Intel, AMD, and Arm processors)
	- Amount of RAM
	- Network bandwidth (400 Gbps Ethernet networking)
	- OS (Windows, Ubuntu, Amazon Linux, MAC) (An AMI - Amazon machine Image is a predefined configuration for a VM)
	- Attach multiple Block storage (EBS)
- EC2 is the backbone of AWS - most of the service use EC2 - S3, RDS, DynamoDB, Lambda 

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






## Use cases

- **Run cloud-native and enterprise applications** - Amazon EC2 delivers secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs.
- **Scale for HPC applications** - Access the on-demand infrastructure and capacity you need to run HPC applications faster and cost-effectively.
- **Develop for Apple platforms** - Build, test, and sign on-demand macOS workloads. Access environments in minutes, dynamically scale capacity as needed, and benefit from AWS’s pay-as-you-go pricing.
- **Train and deploy ML applications** - Amazon EC2 delivers the broadest choice of compute, networking (up to 400 Gbps), and storage services purpose-built to optimize price performance for ML projects.

## Amazon EC2 Instance Types

- **General Purpose** - General purpose instances provide a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads. These instances are ideal for applications that use these resources in equal proportions such as web servers and code repositories. 

- **Compute Optimized** - Compute Optimized instances are ideal for compute bound applications that benefit from high performance processors. Instances belonging to this category are well suited for batch processing workloads, media transcoding, high performance web servers, high performance computing (HPC), scientific modeling, dedicated gaming servers and ad server engines, machine learning inference and other compute intensive applications.

- **Memory Optimized** - Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.

- **Accelerated Computing** - Accelerated computing instances use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs.
(The Accelerated Computing instance category includes instance families that use hardware accelerators, or co-processors, to perform some functions, such as floating-point number calculation and graphics processing, more efficiently than is possible in software running on CPUs. Amazon EC2 provides a broad choice of accelerators including GPUs, purpose built AI chips AWS Trainium and AWS Inferentia, FPGAs and more.)

- **Storage Optimized** - Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver millions of low-latency, random I/O operations per second (IOPS) to applications

- **HPC Optimized** - High performance computing (HPC) instances are purpose built to offer the best price performance for running HPC workloads at scale on AWS. HPC instances are ideal for applications that benefit from high-performance processors such as large, complex simulations and deep learning workloads.

**What are Amazon EC2 UltraServers** - Amazon EC2 UltraServers are ideal for customers seeking the highest AI training and inference performance for models at the trillion-parameter scale. UltraServers connect multiple EC2 instances using a dedicated, high-bandwidth, low-latency accelerator interconnect, so you can use a tightly coupled mesh of accelerators across EC2 instances and access significantly more compute and memory than standalone EC2 instances.


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