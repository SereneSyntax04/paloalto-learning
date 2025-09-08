# Cloud Native Security

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

# Four Cs of Cloud Native Security 🚀

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
