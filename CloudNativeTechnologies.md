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


---

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