# Cloud Computing

## Sources
<details>
<summary>Cloud Computing (PEC-CS701B) </summary>
<details>
<summary>1. Definition of Cloud Computing and its Basics (Lectures)</summary>

- Defining a Cloud
- Cloud Types
  - NIST model
  - Cloud Cube Marks/Unit model
- Deployment models
  - Public Clouds
  - Private Clouds
  - Hybrid Clouds
  - Community Clouds
- Service Models
  - Platform as a Service (PaaS)
  - Software as a Service (SaaS) with examples of services/service providers
  - Infrastructure as a Service (IaaS)
  - Cloud Reference model
- Characteristics of Cloud Computing
  - A shift in paradigm
  - Benefits and advantages of Cloud Computing
- A brief introduction on:
  - Composability
  - Infrastructure
  - Platforms
  - Virtual Appliances
  - Communication Protocols
  - Applications
  - Connecting to the Cloud by Clients
- IaaS
  - Basic concept
  - Workload
  - Partitioning of virtual private server instances
  - Pods
  - Aggregations
  - Silos
- PaaS
  - Basic concept
  - Tools and development environment with examples
- SaaS
  - Basic concept and characteristics
  - Open SaaS and SOA
  - Examples of SaaS platform
  - Identity as a Service (IDaaS)
  - Compliance as a Service (CaaS)

</details>

<details>
<summary>2. Use of Platforms in Cloud Computing</summary>

- [X] Concepts of Abstraction and Virtualization
- Virtualization technologies
  - Types of virtualization (access, application, CPU, storage)
  - Mobility patterns (P2V, V2V, V2P, P2P, D2C, C2C, C2D, D2D)
- Load Balancing and Virtualization
  - Basic Concepts
  - Network resources for load balancing
  - Advanced load balancing (including Application Delivery Controller and Application Delivery Network)
  - Mention of The Google Cloud as an example of use of load balancing
- Hypervisors
  - Virtual machine technology and types
  - VMware
  - vSphere Machine Imaging (including mention of Open Virtualization Format – OVF)
- Porting of applications in the Cloud
  - The simple Cloud API and AppZero Virtual Application appliance
  - Concepts of Platform as a Service
  - Definition of services
  - Distinction between SaaS and PaaS (knowledge of Salesforce.com and Force.com)
  - Application development Use of PaaS Application frameworks
  - Discussion of Google Applications Portfolio
    - Indexed search
    - Dark Web
    - Aggregation and disintermediation
    - Productivity applications and service
    - Adwords
    - Google Analytics
    - Google Translate, a brief discussion on Google Toolkit (including introduction of Google APIs in brief)
    - Major features of Google App Engine service
- Windows Azure platform
  - Microsoft’s approach
  - Architecture and main elements
  - Overview of Windows Azure AppFabric
  - Content Delivery Network
  - SQL Azure
  - Windows Live services

</details>

<details>
<summary>3. Cloud Infrastructure</summary>

- Cloud Management
  - An overview of the features of network management systems and a brief introduction of related products from large cloud vendors
  - Monitoring of an entire cloud computing deployment stack – an overview with mention of some products
  - Lifecycle management of cloud services (six stages of lifecycle)
- Concepts of Cloud Security
  - Cloud security concerns
  - Security boundary
  - Security service boundary
  - Overview of security mapping
  - Security of data
    - Brokered cloud storage access
    - Storage location and tenancy
    - Encryption
    - Auditing and compliance
  - Identity management (awareness of Identity protocol standards)

</details>

<details>
<summary>4. Concepts of Services and Applications</summary>

- Service Oriented Architecture
  - Basic concepts of message-based transactions
  - Protocol stack for an SOA architecture
  - Event-driven SOA
  - Enterprise Service Bus
  - Service catalogs
- Applications in the Cloud
  - Concepts of cloud transactions
  - Functionality mapping
  - Application attributes
  - Cloud service attributes
  - System abstraction and Cloud Bursting
  - Applications and Cloud APIs
- Cloud-based Storage
  - Cloud storage definition
    - Manned
    - Unmanned
- Webmail Services
  - Cloud mail services including
    - Google Gmail
    - Mail2Web
    - Windows Live Hotmail
    - Yahoo mail
  - Concepts of Syndication services

</details>

</details>


## [Cloud Computing](lessons/cloud_computing/readme.md)  

### [Cloud Service Models](lessons/cloud_computing/cloud_service_models/readme.md)  
- [Infrastructure as a Service (IaaS)](lessons/cloud_computing/cloud_service_models/iaas.md)  
- [Platform as a Service (PaaS)](lessons/cloud_computing/cloud_service_models/paas.md)  
- [Software as a Service (SaaS)](lessons/cloud_computing/cloud_service_models/saas.md)  
- [Function as a Service (FaaS)](lessons/cloud_computing/cloud_service_models/faas.md)  

### [Cloud Deployment Models](lessons/cloud_computing/cloud_deployment_models/readme.md)  
- [Public Cloud](lessons/cloud_computing/cloud_deployment_models/public_cloud.md)  
- [Private Cloud](lessons/cloud_computing/cloud_deployment_models/private_cloud.md)  
- [Hybrid Cloud](lessons/cloud_computing/cloud_deployment_models/hybrid_cloud.md)  
- [Community Cloud](lessons/cloud_computing/cloud_deployment_models/community_cloud.md)  

### [Cloud Architecture](lessons/cloud_computing/cloud_architecture/readme.md)  
- [Frontend (Client-Side)](lessons/cloud_computing/cloud_architecture/frontend.md)  
- [Backend (Cloud Infrastructure)](lessons/cloud_computing/cloud_architecture/backend.md)  
- [Virtualization](lessons/cloud_computing/cloud_architecture/virtualization.md)  
- [Middleware](lessons/cloud_computing/cloud_architecture/middleware.md)  
- [APIs and Interfaces](lessons/cloud_computing/cloud_architecture/apis.md)  

### [Cloud Providers](lessons/cloud_computing/cloud_providers/readme.md)  
- [Amazon Web Services (AWS)](lessons/cloud_computing/cloud_providers/aws.md)  
- [Microsoft Azure](lessons/cloud_computing/cloud_providers/azure.md)  
- [Google Cloud Platform (GCP)](lessons/cloud_computing/cloud_providers/gcp.md)  
- [IBM Cloud](lessons/cloud_computing/cloud_providers/ibm.md)  
- [Oracle Cloud](lessons/cloud_computing/cloud_providers/oracle.md)  

### [Virtualization in Cloud Computing](lessons/cloud_computing/virtualization/readme.md)  
- [Hypervisors (Type 1 & Type 2)](lessons/cloud_computing/virtualization/hypervisors.md)  
- [Virtual Machines (VMs)](lessons/cloud_computing/virtualization/vms.md)  
- [Containers (Docker, Kubernetes)](lessons/cloud_computing/virtualization/containers.md)  
- [Serverless Computing](lessons/cloud_computing/virtualization/serverless.md)  

### [Cloud Storage](lessons/cloud_computing/cloud_storage/readme.md)  
- [Object Storage](lessons/cloud_computing/cloud_storage/object_storage.md)  
- [Block Storage](lessons/cloud_computing/cloud_storage/block_storage.md)  
- [File Storage](lessons/cloud_computing/cloud_storage/file_storage.md)  
- [Storage Tiers (Hot, Cold, Archive)](lessons/cloud_computing/cloud_storage/storage_tiers.md)  

### [Cloud Security](lessons/cloud_computing/cloud_security/readme.md)  
- [Identity and Access Management (IAM)](lessons/cloud_computing/cloud_security/iam.md)  
- [Encryption (Data at Rest & In Transit)](lessons/cloud_computing/cloud_security/encryption.md)  
- [Firewalls & Network Security](lessons/cloud_computing/cloud_security/firewalls.md)  
- [Compliance and Governance](lessons/cloud_computing/cloud_security/compliance.md)  
- [Zero Trust Security Model](lessons/cloud_computing/cloud_security/zero_trust.md)  
- [Cloud Security Threats](lessons/cloud_computing/cloud_security/threats.md)  

### [Cloud Networking](lessons/cloud_computing/cloud_networking/readme.md)  
- [Virtual Private Cloud (VPC)](lessons/cloud_computing/cloud_networking/vpc.md)  
- [Load Balancing](lessons/cloud_computing/cloud_networking/load_balancing.md)  
- [Content Delivery Network (CDN)](lessons/cloud_computing/cloud_networking/cdn.md)  
- [DNS & Networking Protocols](lessons/cloud_computing/cloud_networking/dns.md)  
- [Edge Computing](lessons/cloud_computing/cloud_networking/edge_computing.md)  

### [Cloud Management & Monitoring](lessons/cloud_computing/cloud_management/readme.md)  
- [Cloud Cost Management](lessons/cloud_computing/cloud_management/cost_management.md)  
- [Performance Monitoring](lessons/cloud_computing/cloud_management/performance_monitoring.md)  
- [Service-Level Agreements (SLA)](lessons/cloud_computing/cloud_management/sla.md)  
- [Auto-scaling and Resource Optimization](lessons/cloud_computing/cloud_management/auto_scaling.md)  
- [Cloud Orchestration](lessons/cloud_computing/cloud_management/orchestration.md)  
- [Disaster Recovery & Backup](lessons/cloud_computing/cloud_management/disaster_recovery.md)  

### [Cloud Computing Benefits](lessons/cloud_computing/cloud_benefits/readme.md)  
- [Scalability](lessons/cloud_computing/cloud_benefits/scalability.md)  
- [Cost Efficiency](lessons/cloud_computing/cloud_benefits/cost_efficiency.md)  
- [High Availability](lessons/cloud_computing/cloud_benefits/high_availability.md)  
- [Disaster Recovery](lessons/cloud_computing/cloud_benefits/disaster_recovery.md)  
- [Business Continuity](lessons/cloud_computing/cloud_benefits/business_continuity.md)  

### [Cloud Computing Challenges](lessons/cloud_computing/cloud_challenges/readme.md)  
- [Security Risks](lessons/cloud_computing/cloud_challenges/security_risks.md)  
- [Compliance Issues](lessons/cloud_computing/cloud_challenges/compliance_issues.md)  
- [Vendor Lock-in](lessons/cloud_computing/cloud_challenges/vendor_lockin.md)  
- [Downtime & Performance Concerns](lessons/cloud_computing/cloud_challenges/downtime_performance.md)  
- [Data Privacy & Regulations](lessons/cloud_computing/cloud_challenges/data_privacy.md)  
- [Integration Complexity](lessons/cloud_computing/cloud_challenges/integration_complexity.md)  
