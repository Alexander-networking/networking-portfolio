\## What is Microsoft Azure

\- Azure is a continually expanding collection of cloud services designed to help organizations meet current and future business challenges.

\- It enables you to build, manage, and deploy applications on a massive global network.

\- Supports a wide range of tools, frameworks, and programming languages.

\- Provides flexibility for running existing workloads or building modern, cloud-native solutions.



\### What Does Azure Offer?

\*\*Limitless Innovation\*\*

\- Build intelligent apps and solutions using advanced technologies, tools, and services.

\- Accelerate business growth with integrated AI and cloud capabilities.



\*\*Bring Ideas to Life\*\*

\- Use a trusted platform with industry-leading AI and cloud services.

\- Empower organizations to innovate and modernize.



\*\*Seamlessly Unify\*\*

\- Manage infrastructure, data, analytics, and AI across a single integrated platform.

\- Simplify platform management and streamline operations.



\*\*Innovate on Trust\*\*

\- Rely on secure, responsible, and trusted cloud technology.

\- Backed by Microsoft’s commitment to security and compliance.



\### What Can I Do with Azure?

\- Azure provides more than 100 services for a wide range of scenarios.

\- You can run existing applications on Azure Virtual Machines (VMs).

\- You can also explore new paradigms like intelligent bots, mixed reality, and serverless computing.



\*\*Beyond Virtual Machines\*\*

\- While many teams start by migrating existing apps to VMs, Azure offers far more than VM hosting.

\- Azure includes AI and machine learning services capable of interacting through vision, hearing, and speech.

\- Storage solutions automatically scale to handle massive data growth.

\- Azure enables solutions that would be impractical or impossible without cloud-scale capabilities.



\## Interacting with Azure



Azure provides multiple ways to manage and interact with cloud resources. You can use the graphical Azure Portal or command-line tools like PowerShell, Bash, and Azure CLI.



---



\## Azure Portal

\- A web-based graphical user interface (GUI) for managing Azure services.

\- Access at: https://portal.azure.com

\- Allows you to:

&nbsp; - Navigate services

&nbsp; - Manage subscriptions and accounts

&nbsp; - Search for resources and settings

&nbsp; - Perform administrative tasks without using the command line



---



\## Azure Cloud Shell

\- A browser-based command-line environment built into the Azure Portal.

\- Supports \*\*PowerShell\*\* and \*\*Bash\*\*.

\- Access by selecting the \*\*Cloud Shell\*\* icon in the portal.

\- Automatically authenticates you and provides a ready-to-use environment.



\### Switching Shells

\- Switch to Bash: `bash`

\- Switch to PowerShell: `pwsh`

\- Indicators:

&nbsp; - PowerShell prompt starts with: `PS`

&nbsp; - Bash prompt shows: `username@azure`



---



\## Using PowerShell in Cloud Shell

\- PowerShell-specific commands work here.

\- Example:  

&nbsp; ```powershell

&nbsp; Get-Date

&nbsp; ```

\- Azure CLI commands also work (start with `az`):

&nbsp; ```powershell

&nbsp; az version

&nbsp; ```



---



\## Using Bash in Cloud Shell

\- Bash commands work here.

\- PowerShell commands \*\*do not\*\* work (e.g., `Get-Date` fails).

\- Use the Bash equivalent:

&nbsp; ```bash

&nbsp; date

&nbsp; ```

\- Azure CLI commands still start with `az`:

&nbsp; ```bash

&nbsp; az upgrade

&nbsp; ```



---



\## Azure CLI Interactive Mode

\- A special mode that behaves like an IDE inside the terminal.

\- Provides:

&nbsp; - Autocompletion

&nbsp; - Command descriptions

&nbsp; - Examples

&nbsp; - No need to type `az` before commands



\### Enter interactive mode:

```bash

az interactive

```



\### Exit interactive mode:

```bash

exit

```



---



\## Summary of Interaction Methods

| Method | Best For | Notes |

|--------|----------|-------|

| \*\*Azure Portal\*\* | Visual management | GUI, easiest for beginners |

| \*\*Cloud Shell (PowerShell)\*\* | Admin tasks, scripting | Uses PowerShell cmdlets + Azure CLI |

| \*\*Cloud Shell (Bash)\*\* | Linux-style workflows | Uses Bash commands + Azure CLI |

| \*\*Azure CLI Interactive Mode\*\* | Learning commands, exploring | Autocomplete + examples, no `az` prefix needed |





\## Azure Physical Infrastructure



Azure’s architecture is built on two major layers:

\- \*\*Physical infrastructure\*\* (datacenters, regions, availability zones)

\- \*\*Management infrastructure\*\* (how resources are organized and controlled)



This section focuses on the physical layer.



---



\## Azure Datacenters

\- The foundation of Azure’s physical infrastructure.

\- Similar to large corporate datacenters: racks of servers, dedicated power, cooling, and networking.

\- Individual datacenters are \*\*not directly accessible\*\*.

\- Instead, they are grouped into \*\*Regions\*\* and \*\*Availability Zones\*\* for resiliency.



---



\## Azure Regions

\- A \*\*geographical area\*\* containing one or more datacenters connected by low‑latency networks.

\- When deploying resources, you often choose a region.

\- Some services or VM sizes are only available in specific regions.

\- Some services are \*\*global\*\* and don’t require region selection (e.g., Microsoft Entra ID, Azure DNS, Azure Traffic Manager).



---



\## Availability Zones

\- Physically separate datacenters \*\*within the same region\*\*.

\- Each zone has independent:

&nbsp; - Power

&nbsp; - Cooling

&nbsp; - Networking

\- Designed as \*\*isolation boundaries\*\* — if one zone fails, others continue running.

\- Connected with high‑speed, private fiber networks.

\- Availability zone–enabled regions have \*\*at least three zones\*\*.



\### Why Use Availability Zones?

\- To build \*\*highly available\*\* and \*\*mission‑critical\*\* applications.

\- Protects against datacenter-level failures.

\- You can replicate compute, storage, and networking resources across zones.

\- Note: Cross‑zone replication may incur additional cost.



\### Types of Zone Support

1\. \*\*Zonal services\*\*  

&nbsp;  - You pin the resource to a specific zone.  

&nbsp;  - Examples: VMs, managed disks, IP addresses.



2\. \*\*Zone‑redundant services\*\*  

&nbsp;  - Azure automatically replicates across zones.  

&nbsp;  - Examples: Zone‑redundant storage, SQL Database.



3\. \*\*Non‑regional services\*\*  

&nbsp;  - Always available globally and resilient to zone/region outages.  

&nbsp;  - Examples: Azure DNS, Microsoft Entra ID.



---



\## Region Pairs

\- Most Azure regions are paired with another region \*\*at least 300 miles away\*\* within the same geography.

\- Purpose: Improve resilience against large-scale disasters (natural disasters, civil unrest, power failures).



\### Benefits of Region Pairs

\- If a major outage occurs, \*\*one region in the pair is prioritized\*\* for recovery.

\- Planned updates are rolled out \*\*one region at a time\*\* to reduce downtime.

\- Data residency stays within the same geography (except Brazil South).



\### Notes on Pairing

\- Most region pairs are \*\*two‑way\*\* (each backs up the other).

\- Some are \*\*one‑way\*\*:

&nbsp; - West India → South India (but South India → Central India)

&nbsp; - Brazil South → South Central US (unique because it crosses geographies)



---



\## Sovereign Regions

Special isolated Azure instances used for legal or compliance requirements.



\### Types of Sovereign Regions

\- \*\*US Government regions\*\*  

&nbsp; - Examples: US DoD Central, US Gov Virginia, US Gov Iowa  

&nbsp; - Physically and logically isolated  

&nbsp; - Operated by screened U.S. personnel  

&nbsp; - Extra compliance certifications



\- \*\*China regions\*\*  

&nbsp; - Examples: China East, China North  

&nbsp; - Operated by 21Vianet (Microsoft does not directly manage these datacenters)





\## Azure Management Infrastructure



Azure’s management infrastructure defines how resources are organized, grouped, billed, and governed.  

It consists of:

\- \*\*Resources\*\*

\- \*\*Resource Groups\*\*

\- \*\*Subscriptions\*\*

\- \*\*Management Groups\*\*



These form a hierarchy used for structure, access control, and governance.



---



\## Azure Resources

\- A \*\*resource\*\* is any Azure item you create or manage.

\- Examples:

&nbsp; - Virtual Machines (VMs)

&nbsp; - Virtual Networks

&nbsp; - Databases

&nbsp; - Storage accounts

&nbsp; - Cognitive Services

\- Resources are the smallest unit of Azure management.



---



\## Resource Groups

\- A \*\*resource group\*\* is a logical container for resources.

\- Every resource \*\*must\*\* belong to exactly one resource group.

\- Resource groups \*\*cannot be nested\*\*.

\- Resources can be moved between groups (but only belong to one at a time).



\### Why Resource Groups Matter

\- Actions apply to all resources inside the group:

&nbsp; - Delete the group → all resources deleted

&nbsp; - Assign access → applies to all resources

\- Useful for:

&nbsp; - Temporary environments (delete the group to clean everything)

&nbsp; - Grouping by access requirements

&nbsp; - Grouping by lifecycle (dev/test/prod)



There are no strict rules — structure them based on what makes management easier.



---



\## Azure Subscriptions

\- A \*\*subscription\*\* is a unit of:

&nbsp; - Billing

&nbsp; - Access control

&nbsp; - Resource organization

\- Required to use Azure.

\- A subscription is tied to an \*\*Azure account\*\* (an identity in Microsoft Entra ID).



\### Multiple Subscriptions

An account can have multiple subscriptions. Useful for:

\- Different billing models

\- Different access policies

\- Separating environments or teams



\### Subscription Boundaries

1\. \*\*Billing Boundary\*\*

&nbsp;  - Each subscription generates its own invoice.

&nbsp;  - Useful for cost tracking (e.g., dev vs. prod).



2\. \*\*Access Control Boundary\*\*

&nbsp;  - Azure RBAC can be applied at the subscription level.

&nbsp;  - Different departments can have different permissions.



\### Reasons to Create Additional Subscriptions

\- \*\*Environment separation\*\* (dev, test, prod)

\- \*\*Organizational separation\*\* (different teams)

\- \*\*Billing separation\*\* (track costs independently)



---



\## Azure Management Groups

\- A \*\*management group\*\* is a container above subscriptions.

\- Used for large-scale governance across many subscriptions.

\- Subscriptions inherit:

&nbsp; - Policies

&nbsp; - Access controls

&nbsp; - Compliance rules

\- Management groups \*\*can be nested\*\*.



\### Why Use Management Groups?

\- Apply policies across many subscriptions at once  

&nbsp; (e.g., “VMs must only be deployed in West US”)

\- Assign RBAC roles across multiple subscriptions  

&nbsp; (one assignment → inherited by all child subscriptions and resource groups)



\### Management Group Limits

\- Up to \*\*10,000\*\* management groups per directory

\- Up to \*\*6 levels\*\* of depth (excluding root + subscriptions)

\- Each management group or subscription has \*\*one parent\*\*



---



\## Azure Management Hierarchy Summary



```

Management Group

&nbsp;  └── Subscription

&nbsp;        └── Resource Group

&nbsp;              └── Resources

```



This hierarchy enables:

\- Consistent governance

\- Scalable access control

\- Organized resource management

\- Clear billing separation





\## Azure Virtual Machines (VMs)



Azure Virtual Machines provide \*\*Infrastructure as a Service (IaaS)\*\*, giving you a virtualized server in the cloud with full control over the operating system and software.



\### When to Use VMs

VMs are ideal when you need:

\- Full control over the operating system

\- Ability to run custom software

\- Custom hosting or configuration requirements



VMs give you virtualization flexibility without owning physical hardware, but \*\*you\*\* are responsible for:

\- OS configuration

\- Updates and patching

\- Software installation and maintenance



\### VM Images

\- A \*\*VM image\*\* is a template used to create a VM.

\- Images may include:

&nbsp; - Operating system

&nbsp; - Preinstalled software (web servers, dev tools, etc.)

\- Preconfigured images allow rapid provisioning in minutes.



---



\## Scaling VMs in Azure



You can run:

\- A \*\*single VM\*\* (testing, dev, small workloads)

\- A \*\*group of VMs\*\* for high availability and scalability



Azure provides two major tools for scaling and resiliency:

\- \*\*Virtual Machine Scale Sets\*\*

\- \*\*Availability Sets\*\*



---



\## Virtual Machine Scale Sets (VMSS)

Scale sets allow you to deploy and manage a group of \*\*identical, load‑balanced VMs\*\*.



\### Benefits

\- Centralized configuration and updates

\- Automatic scaling based on:

&nbsp; - Demand (CPU, memory, load)

&nbsp; - Schedule

\- Built‑in load balancer deployment

\- Ideal for:

&nbsp; - Compute-heavy workloads

&nbsp; - Big data

&nbsp; - Container workloads

&nbsp; - Large-scale services



Azure handles:

\- Instance creation

\- Load balancing

\- Scaling up/down



---



\## Virtual Machine Availability Sets

Availability sets improve \*\*resiliency\*\* by distributing VMs across multiple isolated hardware groups.



Two key concepts:



\### 1. Update Domains

\- Group of VMs that can be rebooted together during maintenance.

\- Ensures only one update domain is offline at a time.

\- Azure waits up to 30 minutes for recovery before updating the next domain.



\### 2. Fault Domains

\- Group of VMs sharing a common power source and network switch.

\- Availability sets spread VMs across \*\*up to three fault domains\*\*.

\- Protects against physical hardware failures.



\### Cost

\- No extra cost for availability sets.

\- You only pay for the VMs.



---



\## Common VM Use Cases



\### Testing \& Development

\- Quickly create different OS/app configurations.

\- Easy cleanup by deleting the VM or resource group.



\### Running Applications in the Cloud

\- Handle fluctuating demand by scaling VMs up/down.

\- Pay only for what you use.



\### Extending On‑Premises Datacenters

\- Create a virtual network in Azure and add VMs.

\- Run apps like SharePoint in Azure instead of on-prem.

\- Reduces deployment complexity and cost.



\### Disaster Recovery

\- Spin up VMs in Azure if your primary datacenter fails.

\- Shut them down once normal operations resume.

\- Cost-effective alternative to maintaining a secondary site.



\### Lift and Shift

\- Move physical servers to Azure with minimal changes.

\- Create an image of the physical server and host it as a VM.

\- You still maintain OS and software.



---



\## VM Resource Configuration



When provisioning a VM, you choose:



\### Size

\- Determines CPU cores, RAM, and performance tier.



\### Storage

\- HDD or SSD options

\- Managed disks for reliability



\### Networking

\- Virtual network (VNet)

\- Public IP address (optional)

\- Port and firewall configuration





\## Azure Virtual Desktop (AVD)



Azure Virtual Desktop is a \*\*desktop and application virtualization service\*\* that runs entirely in the cloud. It allows users to access a cloud‑hosted Windows desktop from virtually any device or location.



\### Key Capabilities

\- Provides a full Windows desktop experience hosted in Azure.

\- Accessible through:

&nbsp; - Remote Desktop apps

&nbsp; - Modern web browsers

&nbsp; - Multiple device types (Windows, macOS, Linux, iOS, Android)

\- Ideal for remote work, secure access, and centralized desktop management.



---



\## Security Benefits

Azure Virtual Desktop enhances security through centralized identity and access control.



\### Security Features

\- \*\*Microsoft Entra ID integration\*\* for centralized authentication.

\- \*\*Multifactor authentication (MFA)\*\* to secure user sign‑ins.

\- \*\*Role-Based Access Control (RBAC)\*\* for granular permissions.

\- Data and apps run in the cloud, not on the local device:

&nbsp; - Reduces risk of data leakage

&nbsp; - Protects confidential information

\- User sessions are isolated in both:

&nbsp; - Single‑session environments

&nbsp; - Multi‑session environments



---



\## Multi‑Session Windows 10/11

Azure Virtual Desktop supports \*\*Windows 10/11 Enterprise multi‑session\*\*, a unique capability not available on traditional Windows client OS.



\### Benefits of Multi‑Session

\- Multiple users can connect to the \*\*same VM\*\* simultaneously.

\- More cost‑efficient than giving each user their own VM.

\- Better application compatibility and user experience than Windows Server‑based desktops.



---



\## Summary

Azure Virtual Desktop provides:

\- Cloud‑hosted Windows desktops

\- Strong security and centralized management

\- Multi‑session Windows 10/11 support

\- Broad device and browser compatibility



It’s a powerful solution for remote work, secure access, and scalable desktop environments.





\## Azure Containers



Containers provide a lightweight, efficient way to run applications without the overhead of managing a full operating system. They allow multiple isolated application environments to run on a single physical or virtual host.



---



\## What Are Containers?

\- A \*\*virtualization environment\*\* that packages an application and its dependencies.

\- Multiple containers can run on a single host (physical or virtual).

\- Unlike VMs:

&nbsp; - You \*\*don’t\*\* manage a full OS inside the container.

&nbsp; - Containers are \*\*lightweight\*\*, \*\*fast\*\*, and \*\*highly portable\*\*.

\- Designed for:

&nbsp; - Rapid creation and scaling

&nbsp; - Quick restarts after crashes

&nbsp; - Dynamic response to demand

\- Docker is the most common container engine, and Azure fully supports Docker-based containers.



---



\## Containers vs Virtual Machines



| Virtual Machines | Containers |

|------------------|------------|

| Full OS per VM | Share host OS kernel |

| Heavyweight | Lightweight |

| Slower to start | Start in seconds |

| Strong isolation | Process-level isolation |

| Good for legacy apps or full OS needs | Good for microservices and scalable apps |

| More resource-intensive | Highly efficient |



---



\## Azure Container Services



\### \*\*Azure Container Instances (ACI)\*\*

\- Fastest, simplest way to run containers in Azure.

\- Fully managed \*\*PaaS\*\* offering.

\- No need to manage VMs or orchestration.

\- Upload your container → Azure runs it.



\### \*\*Azure Container Apps\*\*

\- Also a \*\*PaaS\*\* container service.

\- Similar to ACI but with additional features:

&nbsp; - Built‑in load balancing

&nbsp; - Automatic scaling

&nbsp; - Event-driven execution

\- More elastic and suitable for small-to-medium microservice architectures.



\### \*\*Azure Kubernetes Service (AKS)\*\*

\- A \*\*container orchestration\*\* platform.

\- Manages the lifecycle of large fleets of containers.

\- Handles:

&nbsp; - Scaling

&nbsp; - Load balancing

&nbsp; - Self‑healing

&nbsp; - Rolling updates

\- Ideal for enterprise-grade microservices and large distributed systems.



---



\## Containers in Microservice Architectures

Containers are commonly used to build \*\*microservices\*\*, where an application is split into smaller, independent components.



\### Example Architecture

\- \*\*Frontend\*\* → container  

\- \*\*Backend/API\*\* → container  

\- \*\*Storage or database layer\*\* → container  



\### Benefits

\- Each component can be:

&nbsp; - Updated independently

&nbsp; - Scaled independently

&nbsp; - Replaced without affecting others

\- Example:

&nbsp; - If backend traffic spikes, scale only the backend containers.

&nbsp; - Frontend and storage remain unchanged.



---



\## Summary

Containers provide:

\- Lightweight, fast, portable application environments  

\- Efficient scaling and deployment  

\- Strong alignment with microservice architectures  

\- Multiple Azure services to run them (ACI, Container Apps, AKS)





\## Azure Functions



Azure Functions is an \*\*event‑driven, serverless compute service\*\* that runs your code without requiring you to manage virtual machines or containers. Instead of keeping infrastructure running, a function is triggered by an event and executes only when needed.



---



\## Why Azure Functions?

\- No need to maintain servers, VMs, or containers.

\- Code runs \*\*only when triggered\*\*, reducing cost and overhead.

\- Ideal for small, quick tasks that respond to events.



---



\## Benefits of Azure Functions



\### \*\*1. Event‑Driven Execution\*\*

Functions run in response to:

\- REST API calls  

\- Timers (scheduled tasks)  

\- Messages from other Azure services (queues, event hubs, etc.)



\### \*\*2. Automatic Scaling\*\*

\- Functions scale automatically based on demand.

\- Perfect for workloads with unpredictable or spiky traffic.



\### \*\*3. Pay‑Per‑Execution\*\*

\- You only pay for the \*\*CPU time\*\* used while the function runs.

\- No cost when the function is idle.



\### \*\*4. Stateless or Stateful\*\*

\- \*\*Stateless (default):\*\*  

&nbsp; Each execution behaves like a fresh start.

\- \*\*Stateful (Durable Functions):\*\*  

&nbsp; Maintains context between executions to support workflows, chaining, and long‑running processes.



---



\## Serverless Computing Context

Azure Functions is a core part of Azure’s serverless ecosystem:

\- No infrastructure management  

\- Automatic scaling  

\- Event‑driven architecture  

\- Cost‑efficient execution  



Functions can also be deployed in non‑serverless environments if needed, giving developers flexibility to:

\- Control scaling manually  

\- Run inside virtual networks  

\- Isolate workloads  



---



\## When to Use Azure Functions

\- Processing events or messages  

\- Running background jobs  

\- Lightweight APIs  

\- Scheduled tasks  

\- Workflow automation (with Durable Functions)  



---



\## Summary

Azure Functions provides:

\- Event‑driven, serverless compute  

\- Automatic scaling  

\- Pay‑only‑for‑execution pricing  

\- Stateless or stateful execution models  

\- Flexibility to run serverless or in managed environments  





\## Azure Virtual Networking



Azure Virtual Networks (VNets) allow Azure resources—such as VMs, web apps, databases, and containers—to communicate with each other, with the internet, and with on‑premises networks.  

A VNet acts like an extension of your on‑premises network, but in the cloud.



---



\## Key Capabilities of Azure Virtual Networks

\- \*\*Isolation and segmentation\*\*

\- \*\*Internet communications\*\*

\- \*\*Communication between Azure resources\*\*

\- \*\*Communication with on‑premises networks\*\*

\- \*\*Routing network traffic\*\*

\- \*\*Filtering network traffic\*\*

\- \*\*Connecting virtual networks\*\*



Azure supports both \*\*public\*\* and \*\*private\*\* endpoints:

\- \*\*Public endpoint:\*\* Has a public IP; accessible from the internet.

\- \*\*Private endpoint:\*\* Uses a private IP inside the VNet; internal‑only.



---



\## Isolation and Segmentation

\- You can create multiple isolated VNets.

\- Each VNet has its own \*\*private IP address space\*\* (not internet‑routable).

\- You divide the address space into \*\*subnets\*\* for organization and security.

\- For DNS, you can use:

&nbsp; - Azure‑provided DNS  

&nbsp; - Your own internal or external DNS servers  



---



\## Internet Communications

To allow inbound internet access:

\- Assign a \*\*public IP\*\* to a resource, or  

\- Place the resource behind a \*\*public load balancer\*\*



Without this, resources remain private.



---



\## Communication Between Azure Resources



\### \*\*1. Within a VNet\*\*

VNets can connect:

\- VMs  

\- App Service Environment  

\- Azure Kubernetes Service (AKS)  

\- VM Scale Sets  



\### \*\*2. Using Service Endpoints\*\*

Service endpoints allow secure, optimized access to Azure services such as:

\- Azure SQL Database  

\- Storage accounts  



Traffic stays on Microsoft’s backbone network.



---



\## Communication With On‑Premises Networks

Azure VNets can extend your on‑prem network using three methods:



\### \*\*1. Point‑to‑Site VPN\*\*

\- Individual client computer → Azure  

\- Encrypted VPN connection  

\- Good for remote workers



\### \*\*2. Site‑to‑Site VPN\*\*

\- On‑prem VPN device → Azure VPN Gateway  

\- Azure resources appear as part of the local network  

\- Encrypted over the internet



\### \*\*3. ExpressRoute\*\*

\- Private, dedicated connection  

\- Does \*\*not\*\* use the public internet  

\- Higher bandwidth and security  

\- Enterprise‑grade option



---



\## Routing Network Traffic

Azure automatically routes traffic between:

\- Subnets  

\- VNets  

\- On‑prem networks  

\- The internet  



You can override routing using:



\### \*\*Route Tables\*\*

\- Custom rules that control how packets move between subnets.



\### \*\*BGP (Border Gateway Protocol)\*\*

\- Used with VPN gateways, Route Server, or ExpressRoute  

\- Propagates on‑prem routes into Azure



---



\## Filtering Network Traffic



\### \*\*Network Security Groups (NSGs)\*\*

\- Contain inbound/outbound rules  

\- Allow or block traffic based on:

&nbsp; - IP address  

&nbsp; - Port  

&nbsp; - Protocol  



\### \*\*Network Virtual Appliances (NVAs)\*\*

\- Specialized VMs acting as:

&nbsp; - Firewalls  

&nbsp; - WAN optimizers  

&nbsp; - Advanced security appliances  



---



\## Connecting Virtual Networks



\### \*\*VNet Peering\*\*

\- Directly connects two VNets  

\- Traffic stays on Microsoft’s private backbone  

\- Never touches the public internet  

\- Works across regions  

\- Enables global private networks



\### \*\*User‑Defined Routes (UDRs)\*\*

\- Custom routing between subnets or VNets  

\- Gives fine‑grained control over traffic flow



---



\## Summary

Azure Virtual Networking provides:

\- Private, isolated cloud networks  

\- Secure communication between Azure and on‑prem resources  

\- Public and private endpoints  

\- Custom routing and traffic filtering  

\- Global connectivity through VNet peering  





\## Azure Virtual Private Networks (VPNs)



A \*\*virtual private network (VPN)\*\* creates an encrypted tunnel over an untrusted network (usually the public internet).  

VPNs securely connect trusted private networks and protect data from eavesdropping or attacks.



---



\## VPN Gateways



A \*\*VPN gateway\*\* is a special type of virtual network gateway deployed in its own subnet.  

It enables secure, encrypted connectivity between:



\- \*\*On‑premises datacenters ↔ Azure VNets\*\* (Site‑to‑Site VPN)

\- \*\*Individual devices ↔ Azure VNets\*\* (Point‑to‑Site VPN)

\- \*\*Azure VNets ↔ Azure VNets\*\* (Network‑to‑Network VPN)



Key points:

\- Only \*\*one VPN gateway per VNet\*\*, but it can connect to multiple locations.

\- All traffic is encrypted inside the VPN tunnel.



---



\## VPN Types: Policy‑Based vs Route‑Based



\### \*\*Policy‑Based VPN\*\*

\- Uses \*\*static rules\*\* to decide which IP ranges are encrypted.

\- Each packet is checked against a defined policy.

\- Less flexible; not ideal for dynamic or complex networks.



\### \*\*Route‑Based VPN\*\*

\- Treats VPN tunnels as \*\*virtual interfaces\*\*.

\- Standard IP routing (static or dynamic) decides which tunnel to use.

\- More resilient to network changes (e.g., new subnets).

\- \*\*Preferred option\*\* for on‑prem devices.



\### Use Route‑Based VPN for:

\- VNet‑to‑VNet connections  

\- Point‑to‑Site connections  

\- Multisite connections  

\- Coexistence with ExpressRoute  

\- High‑availability scenarios  



\*\*Authentication:\*\* Both VPN types use a \*\*preshared key\*\*.



---



\## High Availability Options for VPN Gateways



\### \*\*1. Active/Standby (Default)\*\*

\- Two gateway instances deployed automatically.

\- Standby takes over during maintenance or failure.

\- Failover:

&nbsp; - Planned: a few seconds  

&nbsp; - Unplanned: up to ~90 seconds  



\### \*\*2. Active/Active\*\*

\- Requires BGP support.

\- Each gateway instance gets its own public IP.

\- On‑premises device creates \*\*two tunnels\*\*, one to each instance.

\- Can be extended with multiple on‑prem VPN devices.



\### \*\*3. ExpressRoute Failover\*\*

\- VPN gateway acts as a backup path if ExpressRoute fails.

\- Ensures continuous connectivity even if the private circuit is disrupted.



\### \*\*4. Zone‑Redundant Gateways\*\*

\- Deploys gateway instances across \*\*Availability Zones\*\*.

\- Protects against zone‑level failures.

\- Requires specific gateway SKUs and \*\*Standard\*\* public IPs.



---



\## Summary

Azure VPNs provide secure, encrypted connectivity between:

\- On‑premises networks  

\- Individual devices  

\- Azure virtual networks  



VPN gateways support multiple connection types, high‑availability configurations, and integration with ExpressRoute for enterprise‑grade resiliency.



