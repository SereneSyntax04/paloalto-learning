# Cloud Native Technologies

Cloud Native Technologies → Tools & resources built for the cloud environment, making apps scalable, portable, and efficient.

VMs = full apartment 🏠 (you manage everything) [Traditional, stateful]

Containers = shared flat 🏢 (light, efficient, some shared resources) [Lightweight, share host OS kernel.]

Serverless = hotel room 🛎️ (you just show up, provider handles the rest) [Stateless bundles of app code.]

---

## Three Core Properties of Cloud Native Technologies

1️⃣ Container Packaged

- Apps run inside containers → isolated, lightweight units.
- Benefits:

1. Better resource isolation.
2. Easier code reuse & simplified operations.
3. Improved developer experience.


2️⃣ Dynamically Managed

- Apps/resources are centrally managed by an orchestrator (e.g., Kubernetes).
- Benefits:

1. Better resource utilization.
2. Lower maintenance cost.
3. Improves efficiency of workloads.


3️⃣ Microserviced

- Apps are built as loosely coupled microservices.
- Dependencies defined via service endpoints/APIs.
- Benefits:

1. More agile development.
2. Easier to scale & maintain apps.


---

## Cloud Native Technologies Hypervisor Terminology

Hypervisor
- Software that lets multiple virtual OS (guests) run on one physical machine (host).

1. Native Hypervisor (Type 1 / Bare Metal)
- Runs directly on hardware (no host OS in between).
- Faster, more efficient, common in data centers.

Example: VMware ESXi, Microsoft Hyper-V.

2. Hosted Hypervisor (Type 2)
- Runs on top of a host OS.
- Easier to set up but less efficient.

Example: VirtualBox, VMware Workstation.



## Virtualization and Hypervisors

1. What is Virtualization?

Virtualization = foundation of cloud computing.

Lets you run multiple Virtual Machines (VMs) on a single physical host.

2. 🖥️ Virtual Machines (VMs)

Act like separate computers.

Can run different operating systems at the same time.

Also called “virtual guest operating systems.”

3. 📦 Shared Resources (from Host → to Guests)

CPU (processors)

Memory (DRAM)

Storage (HDD/SSD)

Network connections

> One physical machine = many virtual computers sharing the same resources.

4. Hypervisor

A hypervisor is software that lets multiple virtual guest OSes run on a single physical host.

It acts as a middle layer between:

the hardware (kernel), and the operating systems running on top.


## Security Considerations in Virtualization

Virtualization improves efficiency, but it also introduces new security risks:

💤 Dormant VMs

Inactive/shut down for weeks or months.

May miss updates (patches, anti-malware).

Become easy targets if reactivated unprotected.

⚠️ Hypervisor Vulnerabilities

Hypervisor = core layer managing VMs.

If compromised → all hosted VMs/resources are exposed.

🔄 Intra-VM Communications

Traffic between VMs on the same physical host may not pass through physical switches.

Results: less visibility, weak monitoring, harder troubleshooting.

📈 VM Sprawl

Rapid growth of virtual environments.

Leads to poor change management.

Makes issues like dormant VMs, hypervisor risks, and hidden VM traffic worse.


---


# Containers

- A container is a lightweight, portable package that includes an application and everything it needs (libraries, dependencies).

- Runs on a shared host OS kernel, making it faster and more efficient than VMs.

- Commonly used with Kubernetes/Docker for scaling and orchestration.

Containers are efficient but come with security risks.  <br>
Since they share the host kernel, a compromise can impact all containers. <br>
Using outdated or insecure images may introduce malware, while weak isolation can allow attackers to break out of a container and access the host system. <br>
Misconfigurations, such as open ports or excessive privileges, further widen the attack surface. To reduce these risks, always scan container images, apply patches, and follow least-privilege practices.

## ⚙️ Container Orchestration

1. Kubernetes is the most widely used open-source orchestration platform.

2. It lets developers manage containers using Infrastructure as Code (IaC) → resources are defined declaratively instead of manually.

3. Enables scaling, self-healing, load balancing, and automation for containers & microservices.

> 👉 Think of Kubernetes as the conductor of an orchestra 🎼 — making sure all containers (instruments) play together in sync.

1. Kubernetes

- Open-source orchestration platform.

- Helps organizations publish, maintain, and update containerized applications.

- Enables rapid scaling and efficient management of cloud native apps.

2. Microservices

- Breaks a large application into smaller, independent services.

- Each microservice runs in its own container.

- Kubernetes orchestrates these containers to make the full app work together.


# Containers as a Service (CaaS)

- CaaS = Cloud service model optimized for running containers at scale.

- Built on orchestrators like Kubernetes, OpenShift, Mesos, Docker Swarm.

- Manages compute, storage, and networking underneath → making container workloads easier to deploy.

### Challenges with Orchestrators

1. Complex to Set Up & Maintain → Even though they simplify microservices management, initial setup and ongoing maintenance remain difficult.

2. Difficult to Manage Hosts → Focus is on containers, not underlying hosts. Organizations still must manage compute, storage, and networking (often via automation or thin VMs).


# 🖥️ Micro-VMs  

### 🔑 What are Micro-VMs?  <br>
- **Micro-VMs** = **scaled-down, lightweight virtual machines** that run on hypervisor software.
- Contain only the **Linux kernel features** needed to run a container.  


### ❓ Why Micro-VMs?  

- **Containers** = fast & efficient, but weaker in **isolation/security**. 
- **VMs** = stronger **isolation**, but more **complex & heavy**.  
- **Micro-VMs** (e.g., **Kata Containers, VMware vSphere Integrated Containers, Amazon Firecracker**) → combine **best of both worlds**: <br>  
  - Developer-friendly like containers. 
  - Stronger **isolation** like VMs.  


### ⚙️ What Do Micro-VMs Provide?  

- Users run containers as usual (e.g., `docker run`).  

- Behind the scenes:  
  - A new **VM** is created.  
  - A container runtime starts inside it.
  - The container executes in an **isolated OS instance**. 

- Each micro-VM typically runs **one container** (or a pod-like set of related containers).  


---

# ☁️ Serverless Computing and Function as a Service (FaaS)  

**Serverless architectures** (also called **Function as a Service, FaaS**) allow organizations to build and deploy applications **without managing physical or virtual servers**.  <br>
- Applications scale **elastically** with cloud workloads.  
- Ideal for a wide range of **services and rapid deployments**.  

<p align="center">
  <img src="" alt="Serverless Computing" width="600"/>
</p>


## 🌟 Benefits of Serverless Computing & FaaS  

### 🔹 Focus on Core Product Functionality  
- Developers focus only on **business logic & product features**.  
- No need to worry about OS, runtimes, or infrastructure setup.  

### 🔹 Not Responsible for Security Patches  
- The **serverless provider** handles **OS & application server patches**.  
- Reduces DevOps burden and ensures **continuous security updates**.  

### 🔹 Secure Data Center, Network, and Servers  
- Provider secures: **data centers, networks, servers, OS, configs**.  
- Application owners are still responsible for:  
  - **Application logic & code**  
  - **Data security**  
  - **App-layer configurations**  

> 👉 **Summary:** Serverless = focus on building apps while the provider manages infrastructure & security basics.  


