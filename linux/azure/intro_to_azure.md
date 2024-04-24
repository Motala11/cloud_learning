# An introduction to Azure

- [An introduction to Azure](#an-introduction-to-azure)
  - [The basics of Azure](#the-basics-of-azure)
  - [Azure regions and availability zones: how they work and include up-to-date diagrams to help](#azure-regions-and-availability-zones-how-they-work-and-include-up-to-date-diagrams-to-help)
  - [How is Azure structured/organised?](#how-is-azure-structuredorganised)
  - [What types of services does Azure provide?](#what-types-of-services-does-azure-provide)
  - [Ways to access Azure?](#ways-to-access-azure)
  - [Explain the difference between Azure and Azure DevOps](#explain-the-difference-between-azure-and-azure-devops)
  - [Why use the Azure Pricing Calculator?](#why-use-the-azure-pricing-calculator)


Microsoft Azure is a cloud computing platform and services suite, which provides a wide range of cloud services for building, deploying and managing applications and services through Microsoft-managed data centers.

## The basics of Azure 
- Overview of Microsoft Azure as a cloud computing platform.
- Key features and benefits.
- Introduction to Azure Resource Manager (ARM) and Azure Portal.
- Provides a wide range of services, such as computing, storage, networking, databases and more.
## Azure regions and availability zones: how they work and include up-to-date diagrams to help 
- Azure regions are geographical areas that contain data centers. Each region is designed to be independent of other regions, providing redundancy and isolation. Azure regions are spread across the globe to ensure low latency and high availability for customers
-  Availability zones are physically separate data centers within an Azure region. Each availability zone is connected through high-speed, private fiber-optic networks and is designed to be independent of other zones within the same region. This architecture provides redundancy and resiliency, allowing applications to remain available even if one availability zone fails.
- The diagram below depicts how the Azure availability zones work, as they collaborate with Microsoft data centers.
![alt text](image.png)
## How is Azure structured/organised? 
- Azure's organisational structure is hierarchical, which provides a logical way to organise and manage resources. The key components include subscriptions, resource groups, resources and management groups.
- Subscriptions are the fundamental unit of billing in Azure. They represent the agreement between the customer and Microsoft to use Azure services.
- A resource group is a logical container that holds related Azure resources for an application or a project. Resources within a resource group share the same lifecycle, permissions and policies.
- Resources are the components that make up Azure services, such as virtual machines, databases, storage accounts and web apps.
- Management groups are a hierarchical structure for organizing Azure subscriptions and resources across an organization.
## What types of services does Azure provide? 
- Compute:
    - Virtual Machines (IaaS): On-demand, scalable virtual machines with customizable configurations,      including Windows and Linux VMs.
- Storage:
    - Blob Storage: Object storage service for storing and managing unstructured data, including documents, images, videos, and backups.
    - File Storage: Fully managed file shares in the cloud, accessible via the SMB protocol.
    - Disk Storage: Persistent, high-performance block storage for Azure Virtual Machines.
    - Data Lake Storage: Scalable and secure data lake solution for big data analytics and AI workloads.
    - Azure Backup: Cloud-based backup and recovery service for protecting data and workloads.
- Networking:
    - Virtual Network: Isolated and customizable network infrastructure for connecting Azure resources securely.
    - Azure Load Balancer: High-performance, scalable load balancing service for distributing incoming traffic across multiple resources.
    - Azure VPN Gateway: Managed VPN service for connecting on-premises networks to Azure securely.
    - Azure DNS: Scalable, reliable DNS hosting service for domain management in Azure.
- Databases:
    - Azure SQL Database: Fully managed relational database service based on SQL Server for building and managing applications.
    - Azure Cosmos DB: Globally distributed, multi-model database service for building highly responsive and scalable applications.
    - Azure Database for MySQL/PostgreSQL: Fully managed database services for MySQL and PostgreSQL databases in Azure.
    - Azure Redis Cache: Fully managed, in-memory data store for caching data to improve application performance.
- AI/ML:
    - Azure Cognitive Services: Pre-built AI models and APIs for vision, speech, language, and search capabilities.
    - Azure Machine Learning: Cloud-based machine learning platform for building, training, and deploying machine learning models at scale.
    - Azure Bot Service: Bot development platform for building intelligent bots that interact with users across multiple channels.
- IoT:
    - Azure IoT Hub: Managed service for connecting, monitoring, and managing IoT devices securely at scale.
    - Azure IoT Central: Fully managed IoT software-as-a-service (SaaS) solution for building and scaling IoT applications.
    - Azure IoT Edge: Edge computing service for deploying and managing AI and IoT solutions at the edge.
- IaaS:
    - With IaaS, Azure provides virtualized computing resources, such as virtual machines, storage, and networking, over the internet.
    - Users have full control over the operating systems, applications, and configurations of the virtual machines.
    - Examples include Azure Virtual Machines, Azure Virtual Network, and Azure Disk Storage.
- PaaS:
    - PaaS offerings provide a platform and environment for developers to build, deploy, and manage applications without managing underlying infrastructure.
    - Azure handles the infrastructure, runtime, middleware, and other services, allowing developers to focus on application development and deployment.
    - Examples include Azure App Service, Azure SQL Database, and Azure Functions.
- SaaS:
    - SaaS offerings deliver software applications over the internet on a subscription basis, eliminating the need for users to install, maintain, and manage the software locally.
    - Azure offers various SaaS applications and services, including Microsoft 365 (formerly Office 365), Dynamics 365, and Azure DevOps.
## Ways to access Azure? 
- Explanation of various access methods, including Azure Portal, Azure CLI, Azure PowerShell, and Azure REST API.
- Overview of Azure mobile app for monitoring and managing resources on the go.
## Explain the difference between Azure and Azure DevOps 
- Clarification of Azure as a cloud computing platform for building, deploying, and managing applications and services.
- Explanation of Azure DevOps as a set of cloud-based collaboration tools for software development, including version control, build automation, and release management.
## Why use the Azure Pricing Calculator? 
- Explanation of the Azure Pricing Calculator as a tool for estimating costs associated with Azure services.
- Benefits of using the calculator for budgeting, planning, and optimizing Azure spending.
- Overview of key features and how to use the calculator effectively.