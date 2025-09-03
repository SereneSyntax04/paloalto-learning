# Cloud Computing Models

## What is Cloud Computing?
- Cloud computing is not about a physical place. Instead, it is a collection of computing resources (like servers, storage, and applications) that you can quickly use whenever needed. 
- These resources are provided on-demand and are managed automatically(by cloud service provider).

## Benefits of Cloud Computing
1. Resource Pooling & Cost Savings
- Resources (like servers, storage, etc.) are shared.
- This lowers costs → economies of scale.
- Works for both private and public clouds.

2. Agility & Flexibility
- No need for many separate, under-used servers.
- Resources are combined, shared, and flexible.
- Scale up or down quickly based on your organization’s needs.

## 🌟 Other Benefits of Cloud / Virtual Systems
1. Segmented Administration : Separate control for each org. 
2. Scalability : Easy to add or remove customers/units
3. Reduced Expenses : Saves money on hardware, electricity, rack space, and maintenance.
4. Sharing Mappings : Shared mappings = simpler management.

## Cloud  Terminology

| **Term** | **Definition (Simplified)** |  
|----------|-----------------------------|  
| **IAM** | Manage digital identities and access. |  
| **Technical Debt** | Future rework cost from quick but not optimal decisions. |  
| **Distributed Workforce** | Team spread across locations. |  
| **Cloud Cybersecurity** | Security tools for cloud products. |  
| **On-Premises** | Hosted in-house, managed locally. |  
| **RBAC** | Access control based on roles. |  

| **Term** | **Definition (Simplified)** |  
|----------|-----------------------------|  
| **DevOps** | Combines Dev + Ops for faster delivery. |  
| **OS** | Software managing hardware & resources. |  
| **VM** | Software-based computer running OS + apps. |  
| **App Software** | Programs to help users perform tasks. |  
| **Runtime** | Where a program executes. |  
| **Shift-Left** | Security earlier in development. |  

---

# Cloud Computing Ecosystem
The cloud computing ecosystem is made up of:
- Service Models (IaaS, PaaS, SaaS)
- Deployment Models (Public, Private, Hybrid, Community)
- Responsibilities (shared responsibility between provider & customer)
- Security Challenges (data protection, compliance, access control, etc.)

⚙️ Service Models, Deployment Models & Responsibilities

1. Virtualization is the backbone of cloud computing.

2. It creates virtual versions of servers, storage, or networks.

3. Combined with orchestration & management tools, it enables:

- Automation
- Easy replication
- On-demand resource delivery


## Cloud Computing Service Models
With more mobile users and a distributed workforce, organizations are depending on cloud apps and infrastructure. This shift makes cloud cybersecurity even more critical.

According to NIST, there are three main service models:
🔹 1. Infrastructure as a Service (IaaS)

- Provides virtualized computing resources (VMs, storage, networks).
- Users manage OS, apps, and data.

Example: AWS EC2, Google Compute Engine, Azure VMs.

🔹 2. Platform as a Service (PaaS)

- Provides a platform to build and deploy apps without worrying about infrastructure.
- Users manage apps and data; provider manages servers, OS, and runtime.

Example: Heroku, Google App Engine, AWS Elastic Beanstalk.

🔹 3. Software as a Service (SaaS)

- Fully managed software delivered over the internet.
- Users just consume the service; everything else is handled by the provider.

Example: Gmail, Salesforce, Office 365.


|IaaS = Rent infrastructure.|
|PaaS = Build on platform.|
|SaaS = Use software.|

---

## Cloud Computing Deployment Models
Modern organizations use a mix of public, private, community, and hybrid cloud environments. Each model comes with unique benefits and security challenges.

🔹 1. Public Cloud

- Open for public use.
- Owned/operated by a third-party provider.
- Located on provider’s premises.

Examples: AWS, Azure, GCP.

👉 Best for scalability and cost efficiency.

<br>

🔹 2. Community Cloud

- Used by a specific group of organizations with common needs.
- Example: Government agencies or universities sharing infrastructure.

👉 Best for collaboration across similar organizations.

<br>

🔹 3. Private Cloud

- Used by one organization only.
- Can be on-premises or hosted by a third party.
- Offers more control and security.

👉 Best for sensitive workloads.

<br>

🔹 4. Hybrid Cloud

- Mix of two or more models (e.g., private + public).
- Combines security of private with scalability of public.

Example: Use private for core apps, public for new apps.

👉 Best for flexibility and balance.

|Public = Anyone can use.|
|Community = Group of orgs.|
|Private = One org only.|
|Hybrid = Mix & match.|

---

## Shared Responsibility Model
When moving from on-premises → cloud, most security risks still exist. The difference is who handles what.

1. Cloud Provider → Responsible for security of the cloud (infrastructure, data centers, physical security, networking, storage, compute, virtualization).

2. Cloud Customer → Responsible for security in the cloud (data, apps, identity, configs, access).

---

## Multi-Tenancy in Cloud Environments

- One system, many users.
- Provider controls resources, customer controls usage.
- Great for cost savings, but comes with shared security challenges.

---

## Network Security vs. Cloud Security
Traditional Network Security

- Fixed environment.
- Applications run on dedicated servers.
- Security controls are stable and predictable.

Cloud Security

- Dynamic & automated environment.
- Applications run on shared resource pools.
- Accessible anytime, anywhere, from any device.
- Security becomes more complex due to:
1. Multi-tenancy
2. Broader attack surface
3. Less direct control over infrastructure

> Network Security = Protecting a fixed, controlled environment. <br>
> Cloud Security = Protecting a moving target (scalable, distributed, user-accessible from anywhere).

---

## Securing the Cloud
As organizations move from traditional data centers to public, private, or hybrid cloud, security strategies must adapt.

1️⃣ Consistent Security

- Apply the same application control & threat prevention in cloud and physical networks.
- Confirm app identity → enforce standard ports only.
- Block rogue or misconfigured apps.
- Use app-specific threat prevention to stop known + unknown malware.

2️⃣ Zero Trust Principles

- Mixed trust levels on one compute resource = efficiency ⚡ but risk ⚠️.
- Use Zero Trust policies → assume no workload is trusted.
- Prevent lateral movement of threats between workloads.

3️⃣ Centralized Management

- Organizations still use physical + virtual security.
- Manage both from one centralized interface.
- Automate policy updates → reduce manual work & human error.

4️⃣ Shift-Left Security

- Move security earlier in the CI/CD pipeline, not just runtime.
- Open source packages = fast dev 🚀 but risky ⚠️.
- Use Software Composition Analysis (SCA) to safely check OSS dependencies for vulnerabilities, compliance, and licensing issues.

5️⃣ Identity Management

- IAM = Authentication + Authorization + Access control.
- Controls provisioning, maintenance, and operation of identities.
- Ensures correct access levels for users across network, data center, and cloud resources.


---

## Cloud Security Best Practices

No matter the model (IaaS, PaaS, SaaS), you are responsible for securing parts of your workloads.
Here’s how to maximize cloud security:

| **Best Practice** | **What It Ensures**                              |
| ----------------- | ------------------------------------------------ |
| Review Defaults   | Don’t rely on vendor; enforce your own policies. |
| Storage & Auth    | Protect uploads, enforce strong password rules.  |
| Data Safety       | Encrypt in transit + at rest with own keys.      |
| Data Retention    | Understand vendor policy; keep backups.          |
| RBAC Privileges   | Limit access to only what’s needed.              |
| Updates           | Keep OS/apps patched; automate updates.          |
| Secure Images     | Pre-build hardened templates for consistency.    |

> In-Transit → Data that is moving from one place to another <br>
> At-Rest → Data that is stored somewhere