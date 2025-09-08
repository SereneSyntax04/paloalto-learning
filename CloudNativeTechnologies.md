<h1 align="center"> Cloud Native Technologies </h1>

Cloud Native Technologies → Tools & resources built for the cloud environment, making apps scalable, portable, and efficient.

| Type       | Analogy                             | Characteristics                    |
|------------|-------------------------------------|------------------------------------|
| VMs        | Full apartment 🏠                  | Stateful, full OS, heavier        |
| Containers | Shared flat 🏢                     | Lightweight, share host OS kernel |
| Serverless | Hotel room 🛎️                     | Stateless, provider-managed       |

---

## Core Properties

1️⃣ Container Packaged

- Apps run inside containers → isolated, lightweight units.
- Benefits: Better isolation, easier reuse, improved dev experience.


2️⃣ Dynamically Managed

- Apps/resources are centrally managed by an orchestrator (e.g., Kubernetes).
- Benefits: Efficient scaling, self-healing, lower maintenance.

3️⃣ Microserviced

- Apps are built as loosely coupled microservices.
- Dependencies defined via service endpoints/APIs.
- Benefits: Agile dev, easy scaling & maintenance.


---

<h1 align="center"> Virtualization & Hypervisors </h1>

### Hypervisor
- Software that lets multiple virtual OS (guests) run on one physical machine (host).
- It acts as a middle layer between:
the hardware (kernel), and the operating systems running on top.

1. Native Hypervisor (Type 1 / Bare Metal)
- Runs directly on hardware (no host OS in between).
- Faster, more efficient, common in data centers.

Example: VMware ESXi, Microsoft Hyper-V.

2. Hosted Hypervisor (Type 2)
- Runs on top of a host OS.
- Easier to set up but less efficient.

Example: VirtualBox, VMware Workstation.


### Virtualization

1. What is Virtualization?

Virtualization = foundation of cloud computing.

Lets you run multiple Virtual Machines (VMs) on a single physical host.

2. 🖥️ Virtual Machines (VMs)

Act like separate computers, can run different operating systems at the same time.

Also called “virtual guest operating systems.”

> One physical machine = many virtual computers sharing the same resources.


<h1 align="center"> Security Considerations in Virtualization (Risks) </h1>

Virtualization improves efficiency, but it also introduces new security risks:

### 💤 Dormant VMs

Inactive/shut down for weeks or months.

May miss updates (patches, anti-malware).

Become easy targets if reactivated unprotected.

### ⚠️ Hypervisor Vulnerabilities

Hypervisor = core layer managing VMs.

If compromised → all hosted VMs/resources are exposed.

### 🔄 Intra-VM Communications

Traffic between VMs on the same physical host may not pass through physical switches.

Results: less visibility, weak monitoring, harder troubleshooting.

### 📈 VM Sprawl

Rapid growth of virtual environments.

Leads to poor change management.

Makes issues like dormant VMs, hypervisor risks, and hidden VM traffic worse.


---


<h1 align="center">Containers</h1>

- A container is a lightweight, portable package that includes an application and everything it needs (libraries, dependencies).

- Runs on a shared host OS kernel, making it faster and more efficient than VMs.

- Commonly used with Kubernetes/Docker for scaling and orchestration.

Containers are efficient but come with security risks.  <br>
Since they share the host kernel, a compromise can impact all containers. <br>
Using outdated or insecure images may introduce malware, while weak isolation can allow attackers to break out of a container and access the host system. <br>
Misconfigurations, such as open ports or excessive privileges, further widen the attack surface. To reduce these risks, always scan container images, apply patches, and follow least-privilege practices.

> Security Risks:
>  - Shared kernel → breakout risks.
>  - Insecure images, misconfigurations.


## ⚙️ Container Orchestration

1. Kubernetes is the most widely used open-source orchestration platform.

2. It lets developers manage containers using Infrastructure as Code (IaC) → resources are defined declaratively instead of manually.

3. Enables scaling, self-healing, load balancing, and automation for containers & microservices.

> 👉 Think of Kubernetes as the conductor of an orchestra 🎼 — making sure all containers (instruments) play together in sync.

1. Kubernetes

- Open-source orchestration platform.

- Helps organizations publish, maintain, and update containerized applications.

- Enables rapid scaling and efficient management of cloud native apps.

2. Microservices (One micro-VM = one container in isolated OS instance.)

- Breaks a large application into smaller, independent services.

- Each microservice runs in its own container.

- Kubernetes orchestrates these containers to make the full app work together.


# Containers as a Service (CaaS)

- Cloud model for running containers at scale.
- Built on Kubernetes, OpenShift, Docker Swarm.
- Handles compute, storage, networking → simplifies container deployment.

### Challenges with Orchestrators

1. Complex to Set Up & Maintain → initial setup and ongoing maintenance remain difficult.

2. Difficult to Manage Hosts → Focus is on containers, not underlying hosts. Organizations still must manage compute, storage, and networking (often via automation or thin VMs).


<h1 align="center"> 🖥️ Micro-VMs  </h1>

### 🔑 What are Micro-VMs?  <br>
- **Micro-VMs** = Lightweight VMs with just enough Linux kernel to run a container.


### ❓ Why Micro-VMs?  

- Containers → Fast but weaker isolation.
- VMs → Strong isolation but heavy.
- Micro-VMs (e.g., Kata Containers, Firecracker) → Combine both: light like containers + strong isolation like VMs.


### 🚀 How It Works
- User runs `docker run` as usual.
- Behind the scenes:
  - A micro-VM is created.
  - Container runs inside isolated OS instance.
- Usually, one micro-VM runs one container or related pod.

---

# ☁️ Serverless Computing & FaaS

**Serverless architectures** (also called **Function as a Service, FaaS**) allow organizations to build and deploy applications **without managing physical or virtual servers**.  <br>
- Scales elastically → Ideal for rapid, on-demand deployments.
- Example: AWS Lambda, Azure Functions.

<p align="center">
  <img src="https://github.com/SereneSyntax04/paloalto-learning/blob/fed05a1d01410ed88a7ab790d5b842abb1297594/images/owner-and-FAAS-provider.png" alt="Serverless Computing" width="600"/>
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


## 🚀 How It Works

- Upload app code/package.
- Platform auto-packages, runs in container.
- Developer doesn’t manage infra.

👉 Behind the scenes → Containers used, but abstracted away.


# 🚀 Adopting a Serverless Model  

### ✅ Reduced Operational Overhead  
- No servers to manage → no worries about scaling infrastructure, installing agents, or maintaining servers.  
- Frees up developers and DevOps to focus on code.  

### ⚡ Increased Agility  
- Heavy reliance on **managed services** (databases, auth, etc.).  
- Developers can focus purely on **business logic** deployed as functions (FaaS) like **AWS Lambda** or **Google Cloud Functions**.  

### 💸 Reduced Costs  
- Pay only for actual usage.  
  - Example: AWS Lambda charges based on function execution time.  
- No need to pay for idle VM capacity → saves money.  

> 👉 **Key Takeaway:**  <br>
> Serverless simplifies deployment, boosts speed, and cuts costs by offloading infrastructure management to the cloud provider.


#  Serverless App Package and Environment  

###  App Package  
- In **serverless apps**, developers only upload the **app code/package**.  
- No need to build full container images or include OS components.  
- The platform automatically:  
  - Packages the code into a container image.  
  - Runs the image in a container.  
  - Sets up the underlying OS, VM, and hardware as needed.  
- Focused on **simplicity and efficiency** over full compatibility or control.  


### ☁️ Serverless Environment Examples  
- **Amazon Lambda**  
- **Azure Functions**  
- Some **PaaS offerings** (e.g., Pivotal Cloud Foundry) are effectively serverless, even if not marketed that way.  

👉 Behind the scenes, **containers are extensively used**, though developers don’t interact with them directly.  


> **Key Point:**  
> Serverless abstracts away infrastructure and focuses on **just your code**, letting the provider handle all complexity.  



# ⚠️ Issues with Serverless Architecture  

### 🔺 Increased Attack Surface  
- Serverless functions consume data from many sources:  
  - HTTP APIs, message queues, cloud storage, IoT devices, etc.  
- This creates a **much larger attack surface**.  
- Many messages are complex and can’t be inspected by standard protections like **Web Application Firewalls (WAFs)**.  

### 🧩 Attack Surface Complexity  
- Hard to fully understand and map out attack vectors.  
- Serverless is relatively new → many developers and architects are still learning how to secure it.  


### 🌐 Overall System Complexity  
- Visualizing and monitoring serverless applications is **more complex than traditional apps**.  
- Lack of visibility makes troubleshooting and securing harder.  


### 🔍 Inadequate Security Testing  
- Security testing is complicated when apps:  
  - Talk to third-party services.  
  - Use cloud services like NoSQL DBs, cloud storage, stream processors.  
- Automated security scanning tools aren’t fully adapted for serverless environments yet.  


### 🚫 Traditional Security Protections Don’t Apply  
- No access to underlying OS or servers →  
  - Cannot use endpoint protection, host-based IPS, WAFs, etc.  
- Existing security rules and detection logic don’t easily translate to serverless apps.  

> 👉 **Key Takeaway:**  
> Serverless offers simplicity and scalability but introduces **new security challenges** that require fresh strategies.  


# 🛠️ Common Scanning Tools for Serverless Applications  

### 🔍 Dynamic Application Security Testing (DAST)  
- Tests only **HTTP interfaces**.  
- Problematic for serverless apps consuming non-HTTP inputs or talking to cloud services.  
- Poor at testing **RESTful APIs** that don’t follow classic HTML/HTTP request-response patterns.  


### 📝 Static Application Security Testing (SAST)  
- Analyzes source code using:  
  - Data flow  
  - Control flow  
  - Semantic analysis  
- Serverless apps = many small functions + event triggers →  
  - High chance of **false positives** and **false negatives**.  
  - Existing rulesets don’t fully support FaaS patterns → need evolution.  


### ⚡ Interactive Application Security Testing (IAST)  
- Better at detecting vulnerabilities vs DAST/SAST.  
- Still limited by non-HTTP interfaces.  
- Requires **local instrumentation agents**, which aren’t practical in serverless environments.  

👉 **Key Insight:**  
Traditional scanning tools aren’t fully adapted for serverless.  
Serverless needs **new specialized security testing solutions** that understand event-driven and FaaS architectures.  
