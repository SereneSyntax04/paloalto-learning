<h1 align="center">Cloud Computing at a Glance</h1>

## What is Cloud Computing?
- On-demand access to computing resources (servers, storage, apps).
- Managed by provider → no hardware headaches.

## 🚀 Why Use Cloud?
- **Cost Savings**: Shared resources → economies of scale.
- **Agility**: Scale up/down fast.
- **Admin Perks**: Segmented control, easy scaling, less maintenance.

---

## 🧱 Key Cloud Terms

| Term               | Simple Meaning                             |
|--------------------|--------------------------------------------|
| IAM                | Manage user identities & permissions      |
| Technical Debt     | Quick fixes → future rework               |
| Distributed Workforce | Teams work from anywhere               |
| RBAC               | Access based on roles                     |
| DevOps             | Dev + Ops → Faster releases               |
| VM                 | Virtual computer                           |
| SaaS               | Use software online (e.g., Gmail)         |
| PaaS               | Platform to build apps (e.g., Heroku)     |
| IaaS               | Virtual infrastructure (e.g., AWS EC2)    |

---


<h1 align="center">Cloud Computing Ecosystem</h1>

The cloud computing ecosystem is made up of:
- Service Models (IaaS, PaaS, SaaS)
- Deployment Models (Public, Private, Hybrid, Community)
- Responsibilities (shared responsibility between provider & customer)
- Security Challenges (data protection, compliance, access control, etc.)




## Cloud Computing Service Models
1. **IaaS** – Rent infrastructure (VMs, Storage).

- Provides virtualized computing resources (VMs, storage, networks).
- Users manage OS, apps, and data.

Example: AWS EC2, Google Compute Engine, Azure VMs.


2. **PaaS** – Build apps without managing infra.

- Provides a platform to build and deploy apps without worrying about infrastructure.
- Users manage apps and data; provider manages servers, OS, and runtime.

Example: Heroku, Google App Engine, AWS Elastic Beanstalk.


3. **SaaS** – Use software as a service.

- Fully managed software delivered over the internet.
- Users just consume the service; everything else is handled by the provider.

Example: Gmail, Salesforce, Office 365.

> 👉 _IaaS = Rent | PaaS = Build | SaaS = Use_

---

## Cloud Computing Deployment Models

- **Public Cloud** – Open, scalable, cost-effective (AWS, Azure).
- **Private Cloud** – Just your org → more control.
- **Community Cloud** – Shared by similar orgs (gov, uni).
- **Hybrid Cloud** – Mix of public + private → Best of both worlds.

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

| Network               | Cloud                          |
|-----------------------|--------------------------------|
| Fixed, predictable     | Dynamic, distributed          |
| Dedicated servers      | Shared resource pools         |
| Easier control         | Complex (multi-tenancy, scale)|


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
