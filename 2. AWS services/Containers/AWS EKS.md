# AWS EKS

Start, run, and scale Kubernetes without thinking about cluster management

## Long Answer

Amazon EKS simplifies running Kubernetes on Amazon Web Services (AWS) by managing tasks such as health monitoring, scaling, and updating the Kubernetes control plane. This allows you to focus on building and running your applications without worrying about underlying infrastructure. As a managed service, Amazon EKS integrates seamlessly with other AWS services, offering a standardized approach to deploy, manage, and scale containerized applications, whether you're running microservices, batch processing jobs, or machine learning workloads. It streamlines Kubernetes usage on AWS, providing the power of container orchestration without the complexity of managing clusters.


## What problems does Amazon EKS solve?

Amazon EKS addresses several challenges that organizations face when working with Kubernetes. To learn more, review the information below each of the following six images.

- **Kubernetes complexity**: Setting up and managing Kubernetes clusters can be intricate and require specialized expertise.
- **Infrastructure management**: Provisioning and maintaining infrastructure for Kubernetes clusters can be resource intensive.
- **Scalability challenges**: Scaling Kubernetes clusters manually to meet varying workload demands can be difficult.
- **High availability**: Making sure there is high availability and fault tolerance for Kubernetes clusters can be challenging.
- **Cost optimization**: Managing costs associated with running Kubernetes clusters can be complex.

## What are the benefits of Amazon EKS?

- **Automated and managed Kubernetes operations**: Amazon EKS offers a managed control plane for Kubernetes clusters. This service takes care of setup, management, and maintenance tasks, so you can concentrate on building and deploying applications. To reduce operational overhead, Amazon EKS streamlines Kubernetes operations with features such as automatic updates, scaling, and monitoring.

- **Scalable and highly available infrastructure**: Amazon EKS uses the AWS scalable and highly available infrastructure, which provides resilience and performance for your workloads.

- **AWS service integration**:Amazon EKS integrates seamlessly with other AWS services for a secure and compliant environment.

- **Secure and compliant environment**- Amazon EKS is certified by multiple compliance programs for regulated and sensitive applications. It is compliant with the following:
	- Security operations center (SOC)
	- Payment card industry (PCI)
	- International Organization for Standardization (ISO)
	- Federal Risk and Authorization Management Program (FedRAMP) – Moderate
	- Information Security Registered Assessors Program (IRAP)
	- Cloud Computing Compliance Controls Catalog (C5)
	- Korea-Information Security Management System (K-ISMS)
	- Esquema Nacional de Seguridad (ENS) High
	- Outsourced Service Provider’s Audit Report (OSPAR)
	- Health Information Trust Alliance Common Security Framework (HITRUST CSF)
	- Amazon EKS is also a Health Insurance Portability and Accountability Act of 1996 (HIPAA) eligible service.

- **Flexible deployment options**: You can use Amazon EKS Anywhere to create and operate Kubernetes clusters on-premises, which facilitates hybrid cloud strategies. You can run nodes on AWS hosted infrastructure in AWS Regions, AWS Local Zones, and AWS Wavelength Zones. You can also run nodes in your on-premises environments with AWS Outposts and Amazon EKS Hybrid Nodes.


## How much does Amazon EKS cost?

- The Amazon EKS pricing model has two main components: the **Amazon EKS control plane cost** and the **cost of the underlying compute resources**. With Amazon EKS pay only for each Amazon EKS cluster created and the associated AWS resources. These resources include EC2 instances or AWS Fargate profiles, used to run the Kubernetes workloads. These costs are based on the following:

	- The **Amazon EKS control plane** incurs a flat hourly rate for each cluster you create. This covers the management and orchestration of the Kubernetes environment. (Amazon EKS has per cluster pricing based on Kubernetes cluster version support, pricing for Amazon EKS Auto Mode, and per vCPU pricing for Amazon EKS Hybrid Nodes.)
	- The **compute resources**, such as Amazon Elastic Compute Cloud (Amazon EC2) instances or AWS Fargate profiles, are billed separately based on their usage. (You also pay for the resources you use to run your applications on Kubernetes worker nodes such as Amazon EC2 instances, Amazon EBS volumes, and public IPv4 addresses.)

Although you pay for EC2 instances and storage, there's an additional charge for the Amazon EKS service itself. Amazon EKS does not offer a flat fee model for unlimited clusters. The pricing is based on actual usage and the number of clusters created. Amazon EKS does not charge based on the number of Pods. Amazon EKS pricing is based on the number of clusters and the underlying resources used, not the individual Kubernetes objects, such as Pods.


## Use cases

- Containerized applications : You can run and manage containerized applications and deploy and scale applications seamlessly across clusters of EC2 instances.
- Microservices : Amazon EKS is suitable for building and running microservices-based applications. Individual services can package and deploy as containers, to enable agility and scalability.
- Hybrid cloud solutions : You can build hybrid cloud solutions by integrating on-premises Kubernetes clusters with the AWS Cloud infrastructure.
- Enterprise requirements : Amazon EKS supports enterprise-level requirements and provides features such as high availability, security, and integrations with other AWS services.
- Batch processing and CI/CD : You can run batch processing jobs and implement continuous integration and continuous delivery (CI/CD) pipelines for containerized applications.
- Machine learning workloads : With its ability to manage graphics processing unit (GPU) resources, you can deploy and scale machine learning workloads in a containerized environment.

## What else should I keep in mind about Amazon EKS?

- **Operational Management and best practices** - Adopt infrastructure as code (IaC) tools to manage Amazon EKS clusters. Implement proper resource tagging for cost allocation and management. Use Amazon EKS managed node groups for streamlined node provisioning and lifecycle management. Regularly review and optimize your cluster configuration for cost efficiency.

- **Monitoring and Logging** - Set up comprehensive monitoring for Amazon EKS clusters by using Amazon CloudWatch Container Insights. Implement logging solutions to collect and analyze container logs. Use tools for detailed cluster metrics and visualization to maintain optimal performance.

- **Security and Access Control** - Implement robust security measures for Amazon EKS clusters. Use IAM roles for service accounts to manage access to AWS resources. Enable network policies to control traffic between Pods. Regularly update and patch the Kubernetes version and nodes to address vulnerabilities.

Note: Amazon EKS uses a control plane to manage the Kubernetes head node, which is responsible for the overall management of the Kubernetes cluster. Nodes run in the user's AWS account and are responsible for running the containerized applications, not for managing the Kubernetes control plane. Data planes are not a concept used in Amazon EKS for managing the Kubernetes control plane. Although a management console can be used to interact with Amazon EKS, they are not used to manage the Kubernetes control plane directly.

Note: Nodes in Amazon EKS are the Amazon EC2 instances or AWS Fargate profiles that run containerized applications. The control plane manages the overall cluster but does not directly run containerized applications. Load balancers distribute traffic but do not run the containerized applications themselves. Auto Scaling groups help manage the number of nodes but do not directly run the containers.


See: Skillbuilder - [Amazon EKS](https://explore.skillbuilder.aws/learn/courses/22416/amazon-elastic-kubernetes-service-eks-getting-started/lessons/170823/amazon-elastic-kubernetes-service-eks-getting-started)


-----

# Amazon EKS Anywhere

Create and operate Kubernetes clusters on your own infrastructure

## Use Cases

- Deploy across hybrid environments : Unify how you run applications across cloud and on-premises environments with Amazon EKS to accelerate your modernization initiatives.

- Deploy high-performing large language models (LLMs) : Deploy secure, scalable, and high-performing LLMs to drive generative AI applications for both training and inference, fully leveraging the capabilities of AWS infrastructure, including graphics processing unit (GPU) instances.

- Maintain data sovereignty - Keep large datasets on premises and maintain legal requirements concerning data location.

## Amazon EKS Anywhere Pricing Summary:

Amazon EKS Anywhere is open-source software you can run on your own hardware in your data center or at the edge.

- **Enterprise Subscription**: You can buy a support plan to get help with your EKS clusters, EKS Anywhere Curated Packages, and receive extended Kubernetes support.
- **Curated Packages**: These are add-ons that give extra features like load balancing, monitoring, and auto-scaling for EKS Anywhere.
- **Enterprise Subscription**: You need an AWS Enterprise Support or AWS Enterprise On-Ramp Support Plan to buy the subscription.
- **Subscription Details**:
	- Purchase: You can buy subscriptions through the EKS console, API, or AWS CLI.
	- Terms: Subscriptions are available for 1-year or 3-year terms.
- **Billing**:
	- 1-year term: $24,000 per cluster, billed $2,000 per month.
	- 3-year term: $18,000 per cluster per year, billed $1,500 per month.
	- The price is the same regardless of your cluster size.
	- You can buy multiple cluster licenses under one subscription.
	- You can cancel within 7 days for a full refund.
	- Include one or many Amazon EKS Anywhere cluster licenses in a single Amazon EKS Anywhere Enterprise Subscription purchase.


EKS hybrid node and EKS Auto mode still remaining
