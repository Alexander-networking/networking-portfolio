## Microsoft Azure Overview
- Azure = cloud computing platform with broad service coverage.
- Supports simple (web hosting) to complex (virtualized environments) workloads.
- Core services: storage, compute, databases, identity management.
- Advanced services: AI, ML, IoT.

## Cloud Computing Basics
- Cloud computing = delivery of computing services over the internet.
- Core services: VMs, storage, databases, networking.
- Extends to: IoT, ML, AI.
- Not limited by physical datacenter constraints.
- Enables rapid scaling without hardware investment.

## Shared Responsibility Model
- On-premises: consumer responsible for everything.
- Cloud: responsibilities are split between provider and consumer.

### Cloud Provider Responsibilities
- Physical datacenter
- Physical network
- Physical hosts
- Power, cooling, physical security

### Consumer Responsibilities
- Information and data
- Devices connecting to cloud
- Accounts and identities
- Access security

### Context-Dependent Responsibilities
- Applications
- Operating systems
- Network controls
- Identity and directory infrastructure

### Responsibility by Service Model
**IaaS**
- Consumer manages most layers except physical infrastructure.

**PaaS**
- Shared responsibility.
- Provider manages platform; consumer manages data and access.

**SaaS**
- Provider manages almost everything.
- Consumer manages data and access.

**On-Prem**
- Consumer manages all layers.

## Cloud Deployment Models
### Private Cloud
- Single-organization use.
- Maximum control over resources/security.
- Higher cost; fewer public cloud benefits.
- Hosted on-site or in dedicated offsite datacenter.

### Public Cloud
- Built/maintained by third-party provider.
- Anyone can purchase and use services.
- Key trait: public availability.

### Hybrid Cloud
- Combines public + private cloud.
- Enables scaling private cloud using public cloud.
- Flexible workload placement (security, compliance, performance).

### Cloud Model Comparison
**Public Cloud**
- No CapEx
- Rapid provisioning
- Pay-as-you-go
- Less control

**Private Cloud**
- Full control
- Isolated data
- Hardware purchase/maintenance required

**Hybrid Cloud**
- Maximum flexibility
- Workload placement choice
- Strong compliance control

## Multi-Cloud
- Use of multiple public cloud providers.
- Common for feature differences or migration.
- Requires managing resources/security across providers.

## Azure Arc
- Unified management across public, private, hybrid, and multi-cloud.
- Centralized governance and resource control.

## Azure VMware Solution
- Run VMware workloads natively in Azure.
- Supports migration from private VMware environments.

## Consumption-Based Model
### CapEx vs OpEx
**CapEx**
- Upfront cost for physical assets (datacenter, hardware).

**OpEx**
- Ongoing cost for services (subscriptions, cloud).
- Cloud = OpEx because resources are rented.

### Characteristics
- Pay only for consumed resources.
- No cost for unused resources.
- No physical infrastructure or maintenance costs.

### Benefits
- No upfront investment.
- No unused infrastructure waste.
- Scale up when needed.
- Stop paying when not needed.

### Traditional Datacenter Issues
- Must estimate future resource needs.
- Overestimate → wasted money.
- Underestimate → performance issues + long expansion times.

### Cloud Advantages
- No need to predict exact resource needs.
- Add/remove VMs based on demand.
- Pay only for active resources.

### Cloud Pricing Summary
- Cloud = renting compute/storage from provider datacenter.
- Use resources like your own, return when done.
- Provider maintains infrastructure.
- Enables efficient scaling and cost control.

## High Availability
- High availability ensures applications, services, and resources remain accessible when needed.
- Focuses on maintaining maximum uptime regardless of disruptions or failures.
- Azure provides high availability through service-level agreements (SLAs) with defined uptime guarantees.
- Architecting solutions requires understanding and designing around these SLA commitments.

## Scalability
- Scalability = ability to adjust resources to meet changing demand.
- Allows systems to handle peak traffic by adding more resources when needed.
- Prevents overpaying because cloud uses a consumption-based model: pay only for what you use.
- When demand drops, resources can be reduced to lower costs.

### Vertical Scaling
- Increases or decreases the power of an existing resource.
- Scaling up: add more CPU, RAM, or performance to a VM.
- Scaling down: reduce CPU or RAM if over-provisioned.

### Horizontal Scaling
- Adds or removes the number of resource instances.
- Scaling out: add more VMs, containers, or nodes to handle increased demand.
- Scaling in: remove instances when demand decreases.
- Can be automatic or manual depending on configuration.

## Reliability
- Reliability = ability of a system to recover from failures and continue functioning.
- A core pillar of the Microsoft Azure Well-Architected Framework.
- Cloud environments are decentralized, supporting resilient infrastructure by design.
- Resources can be deployed across multiple global regions.
- If one region experiences a catastrophic event, other regions remain operational.
- Applications can be architected to automatically take advantage of regional redundancy.
- In some cases, Azure can automatically shift workloads to another region without user intervention.

## Predictability
- Predictability allows you to plan and operate with confidence.
- Predictability applies to both performance and cost.
- Both are strongly influenced by the Azure Well-Architected Framework.
- Solutions built around this framework have predictable performance and predictable cost behavior.

### Performance Predictability
- Focuses on ensuring resources meet customer experience expectations.
- Autoscaling can automatically add resources when demand increases and remove them when demand drops.
- Load balancing distributes traffic to prevent overload on any single resource.
- High availability ensures consistent performance even during failures or spikes.

### Cost Predictability
- Focuses on forecasting and managing cloud spending.
- Cloud usage can be tracked in real time.
- Resource monitoring ensures efficient use of services.
- Data analytics can identify usage patterns and trends for better planning.
- Predictive insights help adjust resources proactively.
- Tools like the Total Cost of Ownership (TCO) Calculator and Pricing Calculator help estimate future cloud costs.

## Security and Governance
- Cloud features support governance and compliance across IaaS, PaaS, and SaaS deployments.
- Templates and policies ensure all deployed resources meet corporate standards and regulatory requirements.
- Resources can be updated to new standards as requirements evolve.
- Cloud-based auditing identifies resources that fall out of compliance and provides mitigation guidance.
- Depending on the operating model, software patches and updates may be applied automatically, improving both governance and security.

### Security Options by Cloud Model
**IaaS**
- Maximum control over security.
- You manage OS, software, patches, and maintenance.
- Provider manages physical infrastructure.

**PaaS / SaaS**
- Patches and maintenance handled automatically by the provider.
- Reduces operational overhead.
- Ideal for organizations wanting built-in security management.

### Cloud Security Advantages
- Cloud providers are well equipped to handle large-scale threats such as DDoS attacks.
- Over-the-internet delivery model enables robust, globally distributed protection.
- Built-in security services strengthen network resilience.

### Governance Benefits
- Establishing strong governance early ensures a secure, compliant, and well-managed cloud environment.
- Governance frameworks help maintain consistency across all deployed resources.
- Supports long-term maintainability and operational stability.

## Manageability in the Cloud
- Cloud computing provides strong manageability benefits through two main areas: management **of** the cloud and management **in** the cloud.

### Management of the Cloud
- Focuses on managing deployed cloud resources.
- Automatically scale resource deployment based on demand.
- Deploy resources using preconfigured templates to avoid manual setup.
- Monitor resource health and automatically replace failing components.
- Receive automatic alerts based on configured metrics for real-time performance awareness.

### Management in the Cloud
- Focuses on how you interact with and control your cloud environment.
- Manage resources through a web portal.
- Use a command-line interface for scripting and automation.
- Use APIs to integrate cloud management into applications or workflows.
- Use PowerShell for advanced automation and administrative control.