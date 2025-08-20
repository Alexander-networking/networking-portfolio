## What is a Computer Network?
- A network is a system of connected elements that operate together
- A network connects devices such as PCs, printers, servers, phones, cameras etc and allows these devices to exchange data with each other
- LAN (Local Area Network) These are all our devices in close proximity to each other such as routers and switches and end-user devices (Pcs, printers, Phones etc). Example being university campus networks
- WAN (Wide Area Network) Which cover a broad geographic area and are managed by service providers examples being a telecommunication provider's network that interconnects multiple cities and states.
- MAN (Metropolitan area networks) which span a physical area larger than LAN but smaller than WAN for instance a city
- SOHO (Small Office/Home Office) has a small number of devices and uses the internet to connect to a main office
- WLC (Wireless LAN Controllers) used to centralize the management of wireless deployments
  
![Components of a network](Images/Components-of-a-Network.png)

- End point devices are the devices being connected to the network such as PCs, laptops, Phones, servers, virtual servers etc
- Intermediary Devices include switches and routers
- Media is the way devices are connected to the internet, devices using WIFI connect wirelessly where else others use Ethernet or serial links
- Ethernet links mainly used for within LAN network whereas Serial links are how we connect our LANS to a WAN wide area network
- Users who wish to connect their networks to the internet need to connect through a service provider's access network some ways this is done is using different technologies such as dialup or a broadbands telephony network such as ADSL networks, cable networks, mobile, radio or fiber-optic networks
- Small networks usually have fewer than 10 devices, medium to large networks consisting of tens to hundreds of devices and very large global networks such as the internet which connects thousands of devices across the world
-Medium to large enterprise networks can span multiple locations, Usually they have a main office or an enterprise campus which holds most of the corporate resources and remote sites such as branch offices or home offices SOHO which use the internet or WAN (serial links) to connect back to the main office.
-Branch and home offices usually have their own LAN networks with their own servers but mainly rely on the branch office's resources hence the network connection


![Cisco Enterprise Architecture Model](Images/Cisco-Enterprise-Architecture-Model.png)

-The words internet and web are often used interchangeably, but they do not share the same meaning. The internet is a global network that interconnects many networks and therefore provides a worldwide communication infrastructure. The World Wide Web describes one way to provide and access information over the internet using a web browser. It is a service that relies on connections provided by the internet for its function.

## Protocols
-Protocols are a detailed set of rules that govern successful network communication
-The rules define various situations, methods and behaviors that every communicating device should follow
-Examples of protocols used include the voltage to use for an electrical signal, which messages are allowed in communication, what are the building blocks of the messages etc
-Protocols define how data is transmitted between devices in networks and how it allows the devices to communicate with each other
-A set of documents called RFCs defines the protocols and processes of the internet

[Exploring RFC Standards PDF question sheet](PDFS/Exploring-RFC-Standards.pdf)


## Common Usage of Computer Network
- Computer networks are built to communicate, communication methods include:
- Communication before human beings
- Communication between network machines e.g a humidity sensor communicating with a database to send the latest data
- Communication between humans and machines e.g when someone purchases movie tickets online

- When sending data over a network when communicating the data gets transformed into bits to digitalize it and allow it to be sent over the network, the transformation must happen because the rules of communication requires that to happen.

- Over a computer network the communication application and the computer's OS breaks down the large series of bits into smaller groups and prepares them for transmission over the network, once prepared the user's computer transmits them as a digital signal.
- On the path to their destination, the groups of bits encounter different network devices that help them steer and navigate through the network most commonly being a network switch first then onto the network router
- Last step is the data being reassembled in the same order as it was before crossing the computer network. The reason for this is so protocols can convert bits back to original data, that is displayed by the application

EXAMPLE SCENARIO:

In the scenario, the desired destination is Bob’s computer, wherever Bob is located. More specifically, the destination is the chat application on Bob’s computer. For Alice to have a successful, real-time chat with Bob, many things must happen. Bob’s computer has to be powered on, connected to the network, and it must have the chat application running. Also, the complete voyage of the series of bits that Alice’s application created, must happen without issues. The computer network is resilient and the protocols that govern its functioning foresee many issues and provide solutions. All with the goal for the communication to succeed. As evident from our daily activities, network communication is successful most of the time.

## Components of a Network

![Network Device Layout](Images/Network-Devices.png)

## Endpoint Devices
- Called end-user devices and include PCS, laptops, mobile phones, game consoles, file servers, printers, cameras, smart home components etc.
- Many end devices are virtualized
-In virtualization one physical device is used to emulate multiple end devices, the emulated computer system operates as a separate physical unit and has its own operating system and other required software using its host's resources. Virtualization is commonly applied to servers to optimize resource utilization because server resources are often underutilized when they are implemented as separate physical units.

## Intermediary devices
- Devices which interconnect end devices or interconnect networks
- Different functions such as regernerating and retransmitting signals, choosing the best path between networks, classifying and forwarding data according to priorities, filtering traffic to allow or deny it based on security settings.
- Intermediary devices can also be virtualized just like end point devices

## Switches
- Allows multiple end points to connect to the network
- Switches allow devices to communicate on the same network
- All devices connected to a single switch can communicate to each other, to communicate to a different network it needs to pass through a router to do so

## Routers
- Device which connects networks and intelligently chooses the best paths between networks
- Main function is to route traffic from one network to another e.g being you need your router to connect your office network to the internet
- Certain switches combine functionalities of routers and switches and they are called Layer 3 switches

## APs (access points)
- APs are nodes on a wireless network that allows other wireless devices to connect to a wired network
- usually connected to a switch as a standalone device but also can be an integral component of the router itself

## WLCs (Wireless LAN controllers)
- Centralized network device which are used by network administrators or operation centers to facilitate the management of many APs
- Automatically manages the configuration of wireless APs

## Cisco Secure Firewalls
- Firewalls are network security systems that monitor and control the incoming and outgoing network traffic based on predetermined security rules
- Establishes a barrier between a trusted, secure internal network and another outside network such as the internet that is assumed to not be trusted

## Intrusion Protection System (IPS)
- IPS is a system that performs a deep analysis of network traffic while searching for signs that behavior is suspicious or malicious
- Can take action immediately if finding a threat
- IPS and Firewall can work in conjunction to defend a network

## Management Services
- A modern management service offers centralized management that facilitates designing, provisioning, and applying policies across a network
- includes features for discovery and management of network inventory, management of software images, device configuration automation, network diagnostics, and policy configuration.
- It provides end-to-end network visibility and uses network insights to optimize the network.
- example of a centralized management service is Cisco Catalyst Center

- In homes you can often find Wireless routers which has characteristics of a switch, a router that enables users to access other networks and the internet and a WLAN AP allowing wireless devices to connect to it.

- A file server is another network device which runs software that implements standardized protocls to support file transfer from one device to another over a network 

![Components of a network](Images/Components-of-a-Network.png)

## Media
- Media are the physical elements that connect network devices
- Media carry electromagnetic signals that represent data
- Electromagnetic signals can be guided in wires and fiver-optic cables or through wireless transmissions such as WI-FI, mobile or satellite
- Type of media used can be based on a few factors such as budget or the environment used, example being a film crew in the desert might only have access to satellite connected (air medium)
- Wires have connectors on each end which is a plug, the most common type of connector on a LAN is the plug that looks like an analog phone connector, it is called an RJ-45 connector
- Devices use Network Interface Cards NIT to connect devices to a network
- NICs on LANs are called LAN adapters which translate the data created by the device into a format that can be transmitted over the media
- NICs on a LAN are uniquely identified by a MAC address. The MAC address is hardcoded or "burned in" by the NIC manufacturer. NICs used to interface with WANs are called WAN interface cards (WICs), and they use serial links to connect to a WAN network.

## Network Services

- Services in a network comprise software and processes that implement common network applications, such as email and web. These generate data and determine how data is moved through the network
- Companies typically centralize business-critical data and applications into central locations called data centers
- Data centers can include routers, switches, firewalls, storage systems, servers and application delivery controllers.
- Computing resources can also be centralized off-premises in the form of a cloud
- Clouds can be private, public or hybrid and they aggregate the computing, storage, network and application resources in central locations
- Cloud computing resources are configurable and shared among many end users and are transparently available regardless of the user's point of entry
- Data stored by the user is available whenever the user is connected to the cloud

## Topology
- Refers to the arrangement of network elements (devices, links).
- Determines physical connections and logical data flows.
- A well-designed topology optimizes data flow and overall network performance

## Bitrate / Bandwidth
- Bitrate = data rate of a link, measured in bits per second (bps).
- Often called bandwidth or speed in device configs.
- Represents how many bits are transmitted per second—not how fast a single bit travels.
- Transmission speed depends on the physical medium (e.g., copper, fiber).
- Common link speeds:
- 1 Gbps (1 billion bits/sec)
- 10 Gbps
- 100 Gbps (in high-performance networks)

## Availability 
- Measures how often the network is accessible and operational.
- High availability requires:
- Redundant design (backup links, devices, components)
- Fast recovery from failures
- Goal: Minimize downtime and service disruption.

## Reliability
- Indicates how consistently the network performs as expected.
- Focuses on failure-free operation over a defined time period.
- Reliability ≠ Availability:
- A network can be available but not reliable (e.g., degraded performance).
- Reliable networks use high-quality, redundant components to boost both reliability and availability.

![Availability Percentage](Images/Availability-Percentage.png)

## Scalability
- Measures how well a network can grow (users, traffic) without degrading performance.
- A scalable network adapts to increased demand with minimal redesign.
- Designing only for current needs can lead to costly upgrades later.
- Key for future-proofing and long-term efficiency

## Security
- Refers to protection of both:
- Network infrastructure (devices, links)
- Transmitted data (confidentiality, integrity)
- Threats evolve constantly—security must be proactive and adaptive.
- Should be considered in every network-related decision or configuration.
- Includes physical security, access control, encryption, firewalls, etc

## Quality of Service (QoS)
- Set of tools and mechanisms to manage network traffic.
- Prioritizes critical applications during congestion (e.g., VoIP, video).
- Helps ensure consistent performance for latency-sensitive services.
- Can be configured via policies, traffic shaping, and queuing strategies

## Cost
- Covers:
- Initial hardware/software purchases
- Installation and setup
- Ongoing maintenance and upgrades
- Budget constraints often influence design choices and scalability.
- Cost-effective design balances performance, reliability, and future growth

## Virtualization
- Emulates network services/functions in software (vs. traditional hardware).
- Enables centralized management, automation, and provisioning.
- Solves modern challenges like scalability, flexibility, and rapid deployment.
- Examples: virtual switches, routers, firewalls, SDN (Software-Defined Networking)

## Topologies

- Every network has both a physical topology and a logical topology  
- Physical topology refers to the actual layout of devices and cabling in a network  
- The term "node" is commonly used in topology diagrams to represent a device  
- Two networks may share the same physical topology but differ in:  
  - Distance between nodes  
  - Physical interconnections  
  - Transmission rates  
  - Signal types  
- Implementing a physical topology requires using media appropriate to that topology  
- In wired networks, identifying the type of cabling is essential for describing the physical topology  
- Diagrams often illustrate common physical topologies encountered in networking

![Physical Topologies](Images/Physical-Topologies.png)

## Bus Topology

- All workstations are connected to a single cable called the bus or backbone.
- Each device shares the same communication line.
- Earlier setups used coaxial cable with connectors to link devices.
- Signals travel in both directions along the cable.
- Terminators are placed at both ends to prevent signal bounce.

## Ring Topology

- Devices are cabled in succession, forming a closed loop or ring.
- Each device connects to exactly two neighboring devices.
- There is no direct connection to any third device.
- Data sent from one node travels through intermediate nodes until it reaches the destination.
- The ring structure allows data to circulate in one direction (or both, in dual-ring setups).

## Star Topology

- The most common physical topology used in networks
- All devices connect to a central device via point-to-point links
- Also referred to as the hub and spoke topology
- Spoke devices do not have direct physical connections to each other
- Includes both star and extended star topologies
- In an extended star topology:
  - One or more spoke devices are replaced by a device with its own spokes
  - Effectively creates multiple interconnected star topologies

## Mesh Topology

- Devices can be connected to more than one other device
- Multiple paths exist for data to travel between nodes
- Redundant links improve reliability and enable self-healing
- In a full mesh topology:
  - Every node is connected to every other node
- In a partial mesh topology:
  - Some nodes are not connected to all other nodes

## Logical Topologies

- The logical topology is the path which data travels from one point in the network to another.
- The logical topology requires data to also travel through the router for the two devices to communicate. hence in the example why the data does not take the shortest path theough both switches
- Same is true for all other end devices
- Logical topology would then be a star, where the router is a central device

![Logical Topology](Images/Logical-Topologies.png)

## Logical vs Physical Topology

- Logical and physical topologies can be the same, but often differ
- Physical topology refers to the actual layout of devices and cabling
- Logical topology describes how data flows through the network

- Example: Ethernet hub
  - Devices connect in a physical star layout
  - The hub copies signals from one port to all others
  - Data is received by all nodes, behaving like a bus topology
  - Therefore, the logical topology is a bus

- Logical topology is influenced by:
  - Intermediary devices (e.g. hubs, switches, routers)
  - Network protocols used

- Example: Ethernet switch
  - Devices connect in a physical star layout
  - Data is sent only to the intended destination
  - Both physical and logical topologies are star

- Switch-based star topology is the most common LAN implementation today
