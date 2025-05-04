## Cloud Storage

Cloud storage refers to storing data in remote servers that are accessed via the internet. It offers scalability, durability, and accessibility, making it foundational to cloud computing services.

---

### Types of Cloud Storage

| Storage Type       | Description                                                                                                               |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| **Object Storage** | Stores data as objects with metadata and unique identifiers. Ideal for unstructured data such as images, videos, backups. |
| **Block Storage**  | Splits data into fixed-sized blocks. Used for high-performance storage needs like databases and VM disks.                 |
| **File Storage**   | Stores data in hierarchical file/folder structure. Used for shared storage scenarios like NAS.                            |


#### Object Storage

* Stores data as objects (data + metadata + unique ID)
* Ideal for unstructured data like images, videos, and backups
* Accessed via APIs (e.g., Amazon S3, Azure Blob, GCP Cloud Storage)
* Highly scalable and supports metadata tagging and versioning

#### Block Storage

* Divides data into fixed-size blocks
* Each block acts like an individual hard drive
* Low latency, high performance (suitable for databases and OS-level access)
* Examples: Amazon EBS, Azure Managed Disks

#### File Storage

* Data organized in a hierarchical file system
* Shared access using protocols like NFS or SMB
* Suitable for applications requiring a traditional file system
* Examples: Amazon EFS, Azure Files


### Use Cases

| Use Case                         | Suitable Storage |
| -------------------------------- | ---------------- |
| Media content, backups, logs     | Object Storage   |
| Databases, VM disks              | Block Storage    |
| File sharing, collaborative work | File Storage     |

---

### Storage Tiers

| Tier Type        | Purpose                           | Characteristics                    |
| ---------------- | --------------------------------- | ---------------------------------- |
| **Hot Tier**     | Frequently accessed data          | High cost, low latency             |
| **Cool Tier**    | Infrequently accessed data        | Lower cost, higher latency         |
| **Archive Tier** | Rarely accessed or long-term data | Very low cost, high retrieval time |

---

### Key Features

* **Scalability**: Automatically scales to accommodate growing data.
* **Durability**: Cloud providers replicate data across multiple data centers (e.g., 99.999999999% durability in AWS S3).
* **Availability**: Ensures data is accessible when needed, supported by SLAs.
* **Data Lifecycle Management**: Enables automated transition of data between storage tiers based on usage policies.

---

### Storage Access Methods

* **APIs**: RESTful APIs (e.g., S3, Azure Blob Storage)
* **Mounting as Drive**: File storage can be mounted as a shared drive (e.g., NFS, SMB)
* **SDKs/CLIs**: Offered by providers for integration and automation

---

### Lifecycle Management

* Automates data movement across storage tiers
* Policies can define transitions (e.g., move to archive after 90 days)
* Reduces cost while preserving data

---

### Redundancy and Replication

* Ensures durability and high availability
* Data can be replicated across:

  * **Availability Zones** (within region)
  * **Geographically distant regions** (multi-region)
* Types of replication:

  * **Synchronous**: Immediate replication with consistency
  * **Asynchronous**: Delayed replication, better performance
* Examples:

  * AWS S3 Cross-Region Replication (CRR)
  * Azure Geo-Redundant Storage (GRS)

---

### Storage Gateways

* Connect on-premise environments to cloud storage
* Types:

  * **File Gateway**: NFS/SMB protocol access to cloud object storage
  * **Volume Gateway**: Presents iSCSI block volumes locally
  * **Tape Gateway**: Replaces physical tapes with cloud-based virtual tapes
* Use cases:

  * Backup and archiving
  * Hybrid cloud storage extension
  * Disaster recovery

---

### Cloud Storage Providers

| Provider | Services                                            |
| -------- | --------------------------------------------------- |
| AWS      | S3 (Object), EBS (Block), EFS (File)                |
| Azure    | Blob Storage, Disk Storage, File Storage            |
| GCP      | Cloud Storage (Object), Persistent Disks, Filestore |
| Others   | IBM Cloud Object Storage, Oracle Cloud Storage      |

---

### Security & Management

* **Encryption**: Data is encrypted at rest and in transit.
* **Access Control**: IAM policies, ACLs, signed URLs.
* **Auditing**: Logs for access and usage tracking.
* **Compliance**: HIPAA, GDPR, SOC 2 depending on provider.

---
