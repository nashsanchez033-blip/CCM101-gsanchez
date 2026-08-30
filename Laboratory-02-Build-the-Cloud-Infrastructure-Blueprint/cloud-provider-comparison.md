# Cloud Provider Comparison

## Research the Major Cloud Providers

### Overview

Cloud computing providers may use different product names for services that perform similar infrastructure functions. For this comparison, Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP) were examined based on their official documentation.

Although the three providers offer similar fundamental capabilities, each platform has its own terminology, ecosystem, and areas of strength. Understanding these equivalent services is important because cloud engineers may work with different providers depending on the requirements of an organization.

---

## 1. Infrastructure Service Mapping

| Infrastructure Component | Amazon Web Services (AWS) | Microsoft Azure | Google Cloud Platform (GCP) |
|---|---|---|---|
| **Compute** | **Amazon EC2** – Provides virtual servers that can be configured for different workloads. | **Azure Virtual Machines** – Provides scalable virtual machines for Windows and Linux workloads. | **Compute Engine** – Provides customizable virtual machines running on Google infrastructure. |
| **Storage** | **Amazon S3** – Object storage designed for storing and retrieving large amounts of data. | **Azure Blob Storage** – Object storage optimized for large amounts of unstructured data. | **Cloud Storage** – Managed object storage using buckets for storing data. |
| **Networking** | **Amazon VPC** – Creates a logically isolated virtual network for AWS resources. | **Azure Virtual Network (VNet)** – Provides private networking for Azure resources, including subnets and network interfaces. | **Virtual Private Cloud (VPC)** – Provides networking for Compute Engine, GKE, and other Google Cloud workloads. |
| **Identity and Access Management (IAM)** | **AWS IAM** – Controls authentication and permissions for AWS resources. | **Microsoft Entra ID + Azure RBAC** – Provides identity management and role-based access to Azure resources. | **Google Cloud IAM** – Controls which identities can access resources and what actions they can perform. |

---

## 2. Compute Comparison

### AWS – Amazon EC2

Amazon EC2 provides virtual computing capacity that can be used to run applications and workloads in the AWS cloud. It allows organizations to choose different instance configurations depending on their processing, memory, and workload requirements.

### Microsoft Azure – Azure Virtual Machines

Azure Virtual Machines provide on-demand and scalable computing resources. Azure allows users to select VM sizes based on processing power, memory, storage, and networking requirements.

### Google Cloud – Compute Engine

Compute Engine provides customizable virtual machines that run on Google's infrastructure. It can be used for applications, development environments, services, and other workloads requiring virtualized compute resources.

### Comparison

All three providers use virtual machines as a major compute service. The main difference is the platform terminology: AWS uses **EC2**, Azure uses **Virtual Machines**, and Google Cloud uses **Compute Engine**.

---

## 3. Storage Comparison

### AWS – Amazon S3

Amazon S3 is an object storage service used to store and retrieve data. It uses buckets to organize objects and is commonly used for backups, application data, websites, data lakes, and archives.

### Microsoft Azure – Azure Blob Storage

Azure Blob Storage is Microsoft's object storage solution for the cloud. It is designed for large amounts of unstructured data such as documents, images, videos, logs, backups, and other files.

### Google Cloud – Cloud Storage

Google Cloud Storage is a scalable managed object storage service. Data is stored as objects inside containers called buckets, which can be accessed and controlled through Google Cloud services and IAM permissions.

### Comparison

All three platforms provide object storage designed for scalable data storage. Their main equivalent services are **Amazon S3**, **Azure Blob Storage**, and **Google Cloud Storage**.

---

## 4. Networking Comparison

### AWS – Amazon VPC

Amazon VPC allows users to create a logically isolated virtual network for AWS resources. It can contain subnets and other networking components used to control how resources communicate with each other and external networks.

### Microsoft Azure – Azure Virtual Network

Azure Virtual Network provides networking for Azure resources such as virtual machines. It supports subnets, IP addresses, network interfaces, and security-related networking features.

### Google Cloud – Virtual Private Cloud

Google Cloud VPC provides networking for Compute Engine virtual machines, Google Kubernetes Engine clusters, and other cloud workloads. Google Cloud VPC is designed to provide scalable and flexible connectivity between cloud resources.

### Comparison

The three providers all provide virtual networking environments that isolate and connect cloud resources. The equivalent services are called **Amazon VPC**, **Azure Virtual Network**, and **Google Cloud VPC**.

---

## 5. Identity and Access Management Comparison

### AWS – AWS IAM

AWS Identity and Access Management controls who can be authenticated and what permissions they have when accessing AWS resources. IAM policies can be used to provide full or limited access depending on the requirements of a user, service, or application.

### Microsoft Azure – Microsoft Entra ID and Azure RBAC

Microsoft Azure uses Microsoft Entra ID for identity and authentication, while Azure role-based access control (RBAC) is used to assign permissions to users, groups, applications, and other security principals. This allows organizations to control access to Azure resources according to assigned roles.

### Google Cloud – Google Cloud IAM

Google Cloud IAM allows administrators to control who can access Google Cloud resources and what actions they can perform. IAM uses identities, roles, and permissions to provide controlled access and supports the principle of least privilege.

### Comparison

All three providers use identity and permission systems to protect cloud resources. AWS uses **AWS IAM**, Azure combines **Microsoft Entra ID with Azure RBAC**, while Google Cloud uses **Google Cloud IAM**.

---

# Guide Questions

## 1. Which cloud provider offers the broadest range of services? Explain your answer.

**Amazon Web Services (AWS)** can be considered the provider with the broadest overall service portfolio. It offers a large collection of services covering compute, storage, networking, databases, security, analytics, AI/ML, containers, serverless computing, and many other cloud workloads. The exact "broadest" ranking can change as providers add services, but AWS is widely recognized for the breadth and maturity of its cloud service catalog.

---

## 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products? Why?

**Microsoft Azure** would be the most practical choice for an organization that primarily uses Microsoft products. Azure integrates closely with Microsoft's ecosystem, including Windows Server, Microsoft Entra ID, Microsoft 365, SQL Server, and other Microsoft technologies, making identity management and hybrid-cloud integration easier for organizations already invested in Microsoft products.

---

## 3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?

**Google Cloud Platform (GCP)** is particularly recognized for its strengths in Artificial Intelligence, Machine Learning, and Kubernetes. Google Cloud's ecosystem includes advanced AI/ML services and Google Kubernetes Engine (GKE), which builds on Google's experience with container orchestration and Kubernetes.

---

## 4. What similarities did you observe among the three cloud providers?

The three providers offer equivalent core infrastructure services even though they use different product names. All provide virtual computing, scalable storage, virtual networking, and identity/access management, allowing organizations to build secure and scalable cloud environments using similar fundamental concepts.

---

# Quick Service Translation Guide

| If You Know This Concept... | AWS | Azure | Google Cloud |
|---|---|---|---|
| Virtual Machine | EC2 | Azure Virtual Machines | Compute Engine |
| Object Storage | S3 | Blob Storage | Cloud Storage |
| Virtual Network | VPC | Virtual Network | VPC |
| Identity & Permissions | IAM | Entra ID + Azure RBAC | Cloud IAM |

---

# Key Takeaways

### 1. Same Concept, Different Name

One of the most important observations is that cloud providers often solve the same infrastructure problem using different product names.

For example:

**Virtual Machine → EC2 → Azure VM → Compute Engine**

The names are different, but the basic purpose is similar: providing virtualized computing resources.

### 2. Cloud Skills Are Transferable

Learning one cloud provider does not mean that the knowledge becomes useless when working with another provider. Concepts such as virtual machines, storage, networking, IAM, subnets, permissions, and scalability are transferable across platforms.

### 3. Choosing a Provider Depends on the Workload

There is no single cloud provider that is automatically the best for every organization. The best choice depends on factors such as existing technology, application requirements, security needs, pricing, available skills, integration requirements, and the type of workload being deployed.

---

# Conclusion

AWS, Microsoft Azure, and Google Cloud provide the fundamental infrastructure services required to build modern cloud environments. Although their service names and implementations differ, the core concepts remain similar: compute resources run workloads, storage services keep data, networking connects resources, and IAM systems control access.

For a cloud engineer, understanding these similarities is more valuable than memorizing product names alone. Knowing how one provider's service maps to another makes it easier to design, migrate, troubleshoot, and manage infrastructure across different cloud platforms.
