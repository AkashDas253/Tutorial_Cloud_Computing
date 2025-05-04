## Cloud Security

Cloud security encompasses the strategies, controls, processes, and technologies that protect cloud computing environments from internal and external cybersecurity threats. It ensures the **confidentiality**, **integrity**, and **availability** of data and systems hosted in the cloud.

---

### Identity and Access Management (IAM)

* Manages **who can access** cloud resources and **what actions** they can perform.
* Key Elements:

  * **Users, Roles, Policies, Groups**
  * **Granular permissions** through JSON-based policies
  * **Role-Based Access Control (RBAC)** and **Attribute-Based Access Control (ABAC)**
* Integration with **SSO**, **LDAP**, and **Multi-Factor Authentication (MFA)**

---

### Authentication and Authorization

* **Authentication**: Verifies user identity (e.g., username + password, MFA, certificates).
* **Authorization**: Determines permissions after authentication (e.g., what resources a user can access).
* Cloud services often use:

  * **OAuth 2.0**, **SAML**, **OpenID Connect** for federated access
  * **IAM roles and policies** for resource-level control

---

### Encryption (At Rest and In Transit)

* **Encryption at Rest**:

  * Protects stored data using AES-256 or similar
  * Implemented by default or via customer-supplied keys
* **Encryption in Transit**:

  * Secures data during transmission using **TLS/SSL**
  * Applies to API calls, web access, internal service communication
* Ensures protection against eavesdropping and man-in-the-middle attacks

---

### Key Management Services (KMS)

* Secure creation, storage, and lifecycle management of **encryption keys**
* Supports:

  * **Automatic rotation**
  * **Customer-managed keys (CMK)**
  * **Bring Your Own Key (BYOK)**
* Examples:

  * AWS KMS, Azure Key Vault, Google Cloud KMS

---

### Firewalls and Network Security

* **Virtual Firewalls**:

  * Control traffic between cloud networks and the internet
* **Web Application Firewalls (WAF)**:

  * Protect against application-layer attacks (SQL injection, XSS)
* Support rules based on:

  * IP, protocol, port, geolocation

---

### Security Groups and ACLs

* **Security Groups**:

  * Stateful firewalls attached to virtual instances
  * Allow or deny **inbound/outbound traffic**
* **Network Access Control Lists (ACLs)**:

  * Stateless packet filters at subnet level
  * Control IP and port access across the VPC
* Both are key to **segmenting** and **securing** cloud environments

---

### Compliance and Governance

* Adherence to **legal, industry, and organizational** standards:

  * Examples: GDPR, HIPAA, ISO 27001, SOC 2, PCI DSS
* Features:

  * **Audit logs**, **automated alerts**, **resource tagging**
  * **Policy-as-Code** to enforce security at deployment
* Enables risk management, legal compliance, and trust

---

### Zero Trust Security

* **"Never trust, always verify"** model
* Assumes no internal system is inherently secure
* Requires:

  * Strong identity verification
  * Least privilege access
  * Continuous trust evaluation
  * Micro-segmentation and encrypted communication

---

### Cloud Security Threats

* **Misconfigurations**:

  * Public S3 buckets, wide-open ports, unencrypted data
* **Data Breaches**:

  * Unauthorized access due to poor security practices
* **Account Hijacking**:

  * Credential theft via phishing or keylogging
* **DDoS Attacks**:

  * Overload cloud services causing downtime
* **Insider Threats**:

  * Malicious or negligent behavior from legitimate users
* **Insecure APIs**:

  * Poorly secured endpoints exploited by attackers

---
