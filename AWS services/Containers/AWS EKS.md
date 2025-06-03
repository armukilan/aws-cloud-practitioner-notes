# AWS EKS

Start, run, and scale Kubernetes without thinking about cluster management

## Long Answer

Amazon EKS streamlines running Kubernetes on Amazon Web Services (AWS). It handles tasks such as health monitoring, scaling, and updating the Kubernetes control plane. You can focus on building and running your applications instead of worrying about the underlying infrastructure.

Amazon EKS provides a managed Kubernetes service that integrates with other AWS services. You get a standardized way to deploy, manage, and scale containerized applications using Kubernetes, whether you run microservices, batch processing jobs, or machine learning (ML) workloads. Amazon EKS streamlines the use of Kubernetes on AWS and gives you the power of container orchestration without the complexity of managing Kubernetes clusters.

Note: Amazon EKS provides a managed Kubernetes service that integrates with other AWS services.

## What problems does Amazon EKS solve?

Amazon EKS is a managed service that streamlines the deployment, management, and scaling of Kubernetes clusters on AWS. Running Kubernetes clusters on your own can be complex and time consuming. Amazon EKS solves this problem by providing a fully managed Kubernetes control plane. This means you can focus on building and deploying applications instead of managing infrastructure.

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

- **Secure and compliant environment**-
Amazon EKS is certified by multiple compliance programs for regulated and sensitive applications. It is compliant with the following:

Security operations center (SOC)

Payment card industry (PCI)

International Organization for Standardization (ISO)

Federal Risk and Authorization Management Program (FedRAMP) – Moderate

Information Security Registered Assessors Program (IRAP)

Cloud Computing Compliance Controls Catalog (C5)

Korea-Information Security Management System (K-ISMS)

Esquema Nacional de Seguridad (ENS) High

Outsourced Service Provider’s Audit Report (OSPAR)

Health Information Trust Alliance Common Security Framework (HITRUST CSF)

Amazon EKS is also a Health Insurance Portability and Accountability Act of 1996 (HIPAA) eligible service.

- **Flexible deployment options**: You can use Amazon EKS Anywhere to create and operate Kubernetes clusters on-premises, which facilitates hybrid cloud strategies. You can run nodes on AWS hosted infrastructure in AWS Regions, AWS Local Zones, and AWS Wavelength Zones. You can also run nodes in your on-premises environments with AWS Outposts and Amazon EKS Hybrid Nodes.


## How much does Amazon EKS cost?

Amazon EKS follows a pay-as-you-go model, so you only pay for the resources you actually use. This pricing model offers scalability as a key advantage. As your application's demands grow or shrink, you can readily adjust your resource allocation without upfront costs or long-term commitments. This adaptability helps you optimize your expenses while making sure that your Kubernetes clusters have the necessary resources to run efficiently. With Amazon EKS, there are no minimum fees or upfront commitments. Amazon EKS has per cluster pricing based on Kubernetes cluster version support, pricing for Amazon EKS Auto Mode, and per vCPU pricing for Amazon EKS Hybrid Nodes. You also pay for the resources you use to run your applications on Kubernetes worker nodes such as Amazon EC2 instances, Amazon EBS volumes, and public IPv4 addresses.

The Amazon EKS pricing model has two main components: the Amazon EKS control plane cost and the cost of the underlying compute resources. These costs are based on the following:

The Amazon EKS control plane incurs a flat hourly rate for each cluster you create. This covers the management and orchestration of the Kubernetes environment.

The compute resources, such as Amazon Elastic Compute Cloud (Amazon EC2) instances or AWS Fargate profiles, are billed separately based on their usage.

Refer to the AWS pricing page for the most up-to-date information about specific rates and potential discounts.


