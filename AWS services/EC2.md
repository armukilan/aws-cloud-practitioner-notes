# AWS EC2

Secure and resizable compute capacity for virtually any workload

## Why Amazon EC2?

Amazon Elastic Compute Cloud (Amazon EC2) offers the broadest and deepest compute platform, with over 750 instances and choice of the latest processor, storage, networking, operating system, and purchase model to help you best match the needs of your workload. We are the first major cloud provider that supports Intel, AMD, and Arm processors, the only cloud with on-demand EC2 Mac instances, and the only cloud with 400 Gbps Ethernet networking. We offer the best price performance for machine learning training, as well as the lowest cost per inference instances in the cloud. More SAP, high performance computing (HPC), ML, and Windows workloads run on AWS than any other cloud.

## Benefits of Amazon EC2

- **SLA commitment** : Access reliable, scalable infrastructure on demand. Scale capacity within minutes with SLA commitment of 99.99% availability.
- **AWS Nitro System** : Provide secure compute for your applications. Security is built into the foundation of Amazon EC2 with the AWS Nitro System.
- **Optimize performance and cost** : Optimize performance and cost with flexible options like AWS Graviton-based instances, Amazon EC2 Spot instances, and AWS Savings Plans.
- **AWS Migration Tools** : Migrate and build apps with ease using AWS Migration Tools, AWS Managed Services, or Amazon Lightsail. Learn how AWS can help.

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

- **Storage Optimized** - Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver millions of low-latency, random I/O operations per second (IOPS) to applications

- **HPC Optimized** - High performance computing (HPC) instances are purpose built to offer the best price performance for running HPC workloads at scale on AWS. HPC instances are ideal for applications that benefit from high-performance processors such as large, complex simulations and deep learning workloads.

## Instance Features

Amazon EC2 instances provide a number of additional features to help you deploy, manage, and scale your applications.

Amazon EC2 allows you to choose between Fixed Performance instance families (e.g. M6, C6, and R6) and Burstable Performance Instance families (e.g. T3). Burstable Performance Instances provide a baseline level of CPU performance with the ability to burst above the baseline.

### 🔹 Burstable Performance with CPU Credits
T instances work based on a CPU credit system:

- **Baseline Performance** : Each T instance has a baseline level of CPU performance based on its size (e.g., t3.micro, t3.medium).
- **Burst Capability** : When more CPU is needed, the instance can burst beyond the baseline.
- **CPU Credits** :
	- Earned when the instance is idle or using less than the baseline.
	- Spent when the instance uses more than the baseline.
	- 1 CPU Credit = 1 vCPU at 100% for 1 minute.
	- ✅ Example: If your t3.small instance is idle for 10 minutes, it earns 10 CPU credits. Later, it can use those credits to run at full CPU power for 10 minutes.

### 🔹 T Unlimited Mode
T instances can be launched in T Unlimited mode, which provides even more flexibility:

- **Sustained High Performance**: If your workload requires constant high CPU, the instance continues running without throttling—even if it runs out of CPU credits.
- **Smart Billing** :
	- If your average CPU usage stays at or below the baseline during a 24-hour window, no extra charges.
	- If it exceeds the baseline, you are billed a small amount: $0.05 per vCPU-hour of surplus usage.
