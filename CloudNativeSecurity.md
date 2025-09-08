<h1 align="center">Cloud Native Security</h1>

## Why Cloud Security Matters
- Cloud tech boosts speed & flexibility in business.
- Hundreds/thousands of app instances → More attack surfaces.
- Requires **new security approaches**.

---

## Key Concepts

### 1. **4 C's of Cloud Native Security**
- **Cloud Infrastructure Security**
- **Container Security**
- **Cluster Security**
- **Code Security**

### 2. **DevOps vs DevSecOps**
- **DevOps**: Dev + Ops → Fast delivery, automation.
- **DevSecOps**: Dev + Sec + Ops → Security integrated from the start.

### 3. **Standards & Compliance**
- Follow frameworks like **ISO 27001**, **NIST**, **GDPR**.

---

## Important Terms

- **Transport Layer Security (TLS)**  
  Encrypts data in transit (e.g., web ↔ server).

- **Software Development Lifecycle (SDLC)**  
  Step-by-step method to build high-quality software.

- **Cloud Native Computing Foundation (CNCF)**  
  Pushes forward containers & cloud-native tech since 2015.

- **Distributed Cloud**  
  Apps run in geographically spread locations for performance.

- **Container**  
  Lightweight, portable unit packing code + runtime + libraries.

- **Kubernetes (K8s)**  
  Automates container deployment, scaling, management across machines.

---

<h1 align="center">Four Cs of Cloud Native Security 🚀</h1>

Defined by CNCF to provide a layered security model for Kubernetes in cloud-native environments.  
👉 Each layer builds the security foundation for the next.

---

<table>
  <tr>
    <td width="30%">
      <img src="https://github.com/SereneSyntax04/paloalto-learning/blob/e81a6eddb30041c97520b3584b59398747b2e1e9/images/cloud.png" alt="Cloud Layer" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">
      
### ✅ 1. Cloud  
- Provides the **trusted computing base** for Kubernetes.  
- Weak foundation = Security risks everywhere.  
- Secure cloud infra & data centers properly.

    </td>
  </tr>
</table>

---

<table>
  <tr>
    <td width="30%">
      <img src="https://github.com/SereneSyntax04/paloalto-learning/blob/e81a6eddb30041c97520b3584b59398747b2e1e9/images/cluster.png" alt="Cluster Layer" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">

### ✅ 2. Clusters  
- Secure both:
  - Configurable cluster components (API server, etcd, controllers).
  - Applications running inside the cluster.

    </td>
  </tr>
</table>

---

<table>
  <tr>
    <td width="30%">
      <img src="https://github.com/SereneSyntax04/paloalto-learning/blob/e81a6eddb30041c97520b3584b59398747b2e1e9/images/container.png" alt="Container Layer" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">

### ✅ 3. Containers  
- Key practices:
  - Vulnerability scanning (images & OS deps).
  - Image signing & enforcement.
  - Apply **least privilege access**.

    </td>
  </tr>
</table>

---

<table>
  <tr>
    <td width="30%">
      <img src="https://github.com/SereneSyntax04/paloalto-learning/blob/e81a6eddb30041c97520b3584b59398747b2e1e9/images/code.png" alt="Code Layer" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">

### ✅ 4. Code  
- Secure the app code by:
  - Requiring **TLS for access**.
  - Limiting port ranges.
  - Scanning third-party libraries for vulnerabilities.
  - Static & dynamic code analysis.

    </td>
  </tr>
</table>

---

<h1 align="center">Prioritizing Software Security in the Cloud ☁️🔐</h1>

👉 In the cloud, **customers are responsible** for securing:
- Data
- Hosts
- Containers
- Serverless instances

Public cloud providers manage hardware, VMs, storage, and baseline security,  
but you must focus on your workload security ✅.

> Customers should follow **three key DevOps models and processes** to better secure their data in the cloud:
> 
> 1. **DevOps Software Development Model**  
> 2. **DevOps CI/CD Pipeline**  
> 3. **DevSecOps Software Development Model**

---

## 1️⃣ DevOps Software Development Model 🚀

Replaces the traditional SDLC by uniting **Dev & Ops teams** from start to finish.

### Traditional Model vs DevOps
| Traditional SDLC | DevOps Model |
|-----------------|-------------|
| Separate dev & ops | Unified dev + ops teams |
| Manual handoffs | Automated & collaborative |
| Slow release cycles | Fast, continuous releases |

---

### 🔧 Key Characteristics of DevOps

<table>
  <tr>
    <td width="30%">
      <img src="" alt="DevOps Diagram" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">

- ✅ **Collaborative Teams**  
  Development & operations communicate & collaborate constantly.

- ✅ **Culture**  
  Developers, testers, ops work together through the entire delivery lifecycle.

- ✅ **Strategy**  
  DevOps is a **culture & strategy**, not just tools.

- ✅ **More Than Automation**  
  Automation matters, but it's not the whole story.

    </td>
  </tr>
</table>

> ⚡️ DevOps = Faster delivery + Stronger security + Happier teams.

---

## 2️⃣ DevOps CI/CD Pipeline ⚙️

A cycle of **Continuous Integration (CI)** and **Continuous Delivery/Deployment (CD)** that automates development & operations workflows for better productivity, reliability, and faster delivery.

---

### 🚀 What is CI/CD?
- Integrates Dev + Ops to automate infrastructure and workflows.
- Continuously measures app performance.

---

### 🔧 Key Stages

<table>
  <tr>
    <td width="30%">
      <img src="" alt="CI/CD Pipeline Diagram" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">

- ✅ **Continuous Integration (CI)**  
  Developers push code several times per day → Automated builds & tests → Detect problems early.

- ✅ **Continuous Delivery (CD)**  
  CI is automated, but manual checks required before production deployment.

- ✅ **Continuous Deployment (CD)**  
  Fully automated → Code is automatically tested and deployed to production → Instant feature delivery.

    </td>
  </tr>
</table>

---

### ⚡️ Use Case Scenario

1️⃣ **Code is Pushed**  
Developers push code to a repository (e.g., GitHub – used by Airbnb, Netflix, Shopify).

2️⃣ **Pipeline Runs Automatically**  
Tools like **Jenkins** detect changes → Pull code → Build → Test → Deploy to production.


> 💡 Key takeaway:  
> CI/CD Pipeline automates the software delivery process → Faster, safer, and more reliable deployments ✅.

---


## 3️⃣ DevSecOps Software Development Model 🔒

Solves a key problem in DevOps:  
👉 Security often falls through the cracks because speed is prioritized and workflows are automated.

---

### 🚀 What is DevSecOps?  
- Integrates security into the development process from day one.  
- Security becomes part of the **CI/CD pipeline**, not an afterthought.

---

### 🔧 Why DevSecOps Matters

<table>
  <tr>
    <td width="30%">
      <img src="" alt="DevSecOps Diagram" width="100%">
    </td>
    <td width="70%" style="vertical-align: top;">

- ✅ **Early Security Integration**  
  Shift security left → Detect vulnerabilities during code development.

- ✅ **Automated Security Checks**  
  Security tests (SAST, DAST, dependency scanning, secret scanning) run automatically in CI/CD.

- ✅ **Eliminates Silos**  
  Developers, security, and operations collaborate as a single team.

- ✅ **Faster & Secure Releases**  
  Developers maintain speed without compromising security.

    </td>
  </tr>
</table>


> 💡 Key takeaway:  
> DevSecOps = Dev + Sec + Ops → Automated security at every step → Safer, faster, and efficient software delivery ✅.

---

<h1 align="center">Visibility, Governance, and Compliance ✅</h1>

👉 Security standards are key to preventing successful cyber attacks.

---

## 🔒 Why Security Standards Matter  
- Ensure cloud resources & SaaS apps are **properly configured from day one**.  
- Protect collected data & remain compliant → Avoid fines, brand damage, customer trust loss.  
- Enterprise security teams must maintain compliant environments at scale.

---

## ⚡️ Key Compliance Requirements

- ✅ **Real-Time Discovery**  
  Discover & classify resources and data in real time across SaaS, PaaS, and IaaS.

- ✅ **Config Governance**  
  Ensure app/resource configurations follow best practices → Prevent configuration drift.

- ✅ **Access Governance**  
  Apply granular policy definitions to govern access → Implement network segmentation.

- ✅ **Compliance Auditing**  
  Automate compliance checks → Generate audit-ready reports on demand.

- ✅ **Seamless User Experience (UX)**  
  Add new security tools without slowing down workflows or adding extra steps.


> 💡 Key takeaway:  
> Visibility + Governance + Compliance → Strong protection ✅ + Audit-ready ✅ + Smooth user experience ✅.
