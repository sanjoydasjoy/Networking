# Networking Study Repository

This repository contains comprehensive networking study materials organized by topics. Each markdown file covers specific networking concepts with detailed explanations and examples.

<br>

___

<br>


## [Address Resolution.md](Address%20Resolution.md)
```
Address Resolution/
├── MAC and IP Addresses/
│   ├── What Are These Two Types of Addresses?
│   ├── 1. MAC Address (Media Access Control)
│   ├── 2. IP Address (Internet Protocol)
├── When Two Devices Are on the Same Network/
├── When the Devices Are on Different Networks/
├── Address Resolution (How Do Devices Find Each Other?)/
├── ARP Table and Its Location/
│   ├── What is an ARP Table?
│   ├── Where Does the ARP Table Reside?
│   ├── Types of Devices and Their ARP Tables
│   ├── How Long Does the ARP Table Last?
│   ├── Why is the ARP Table Important?
├── How ARP Works/
│   ├── Local Communication (Same Network)
│   ├── Remote Communication (Different Network)
├── ARP Table – Where These Mappings Are Stored/
├── ARP Table Timeout and Maintenance/
├── ARP Weaknesses and Risks/
│   ├── Broadcast Overhead
│   ├── ARP Spoofing or Poisoning
│   ├── Protection Measures
```


<br>

___

<br>


## [Application Layer.md](Application%20Layer.md)
```
Application Layer/
├── Application Layer/
│   ├── Role
│   ├── Responsibility
│   ├── Key Protocols (HTTP, FTP, TFTP, IMAP, DNS)
├── Presentation Layer/
│   ├── Role
│   ├── Responsibilities (Formatting/Translation, Compression, Encryption)
├── Session Layer/
│   ├── Role
│   ├── Responsibilities (Session Control, Dialog Management, Recovery)
├── TCP/IP Application Layer Integration/
├── P2P/
│   ├── Peer-to-Peer Networks
│   ├── Common P2P Applications
├── Client-Server vs. Peer-to-Peer Networking/
│   ├── Client-Server Model
│   ├── Peer-to-Peer (P2P) Model
├── Web and Email Protocols/
│   ├── Web Communication: HTTP and HTML
│   ├── HTTP and HTTPS
│   ├── Email Communication
│   ├── Email Protocols (SMTP, POP, IMAP)
├── IP Addressing Services/
│   ├── DNS (Domain Name System)
│   ├── DNS Record Types
│   ├── DNS Message Parts
│   ├── DNS Hierarchy
│   ├── nslookup Command
│   ├── DHCP (Dynamic Host Configuration Protocol)
│   ├── DHCP Process (4 Steps)
```

<br>

___

<br>


## [basics.md](basics.md)
```
Networking Basics/
├── How the Internet All Started/
│   ├── ❏ The Cold War & the Space Race
│   ├── ❏ The Missing Piece: Hyperlinks and the World Wide Web (WWW)
├── Client Server Architecture/
├── Protocols/
│   ├── TCP (Transmission Control Protocol)
│   ├── UDP (User Datagram Protocol)
│   ├── HTTP (Hypertext Transfer Protocol)
├── How Data is Transfered/
│   ├── ❏ How Do Computers Find Each Other?
│   ├── ❏ How Internet Connections Work
│   ├── ❏ How Does the Router Know Which Application to Send Data to?
│   ├── ❏ Private vs. Public IPs
├── Ports/
│   ├── ❏ Port Ranges
│   ├── ❏ IP Address Commands
├── How Countries Connected/
│   ├── ❏ How Do Two Computers Communicate?
│   ├── ❏ How Are Countries Connected to the Internet?
│   ├── ❏ Why Do We Use Undersea Cables Instead of Satellites?
├── LAN MAN WAN/
│   ├── ❏ LAN (Local Area Network)
│   ├── ❏ MAN (Metropolitan Area Network)
│   ├── ❏ WAN (Wide Area Network)
│   ├── ❏ Wide Area Network Technologies
│   ├── ❏ The Internet: A Collection of LANs, MANs, and WANs
├── Modem and Router/
│   ├── ❏ Modem (Modulator-Demodulator)
│   ├── ❏ Router
│   ├── ❏ How They Work Together
├── Topologies/
│   ├── Network Topologies: How Devices Are Connected
```

<br>

___

<br>


## [DHCPv4.md](DHCPv4.md)
```
DHCPv4/
├── What is DHCPv4?/
├── How it works/
├── Where is it used?/
├── What is DHCP Lease Time?/
│   ├── Here's how it works
│   ├── What happens when the lease ends?
│   ├── Why is there a time limit?
├── 4 DHCP Steps – DORA/
│   ├── D – Discover
│   ├── O – Offer
│   ├── R – Request
│   ├── A – Acknowledge
├── Summary Table/
├── What about the public IP?/
├── Conclusion/
```

<br>

___

<br>


## [Ethernet.md](Ethernet.md)
```
Ethernet/
├── What Ethernet Is/
│   ├── What It Does
│   ├── How It Works
│   ├── Ethernet vs Wi-Fi
├── Ethernet Frame/
│   ├── Data Link Sublayers
│   ├── A. LLC (Logical Link Control) – IEEE 802.2
│   ├── B. MAC (Media Access Control) – IEEE 802.3
│   ├── MAC Sublayer Responsibilities
│   ├── A. Ethernet Encapsulation
│   ├── B. Media Access Control
│   ├── Summary
├── Ethernet Frame Size/
│   ├── What is counted in frame size?
│   ├── Minimum Frame Size – 64 bytes
│   ├── Maximum Standard Frame Size – 1518 bytes
│   ├── Jumbo and Baby Giant Frames
│   ├── Why frame size limits matter
│   ├── Quick Recap
├── Ethernet MAC Address/
│   ├── What is a MAC Address?
│   ├── Format and Structure
│   ├── Hexadecimal Representation Details
│   ├── Structure of the MAC Address
├── Frame Processing/
│   ├── What Happens When a Frame is Sent?
│   ├── What Happens When a Device Receives a Frame?
│   ├── Special Cases
├── Ethernet MAC Address types (Unicast, Broadcast, and Multicast)/
│   ├── Unicast MAC Address
│   ├── Broadcast MAC Address
│   ├── Multicast MAC Address
├── MAC Address Table/
│   ├── What is the MAC Address Table?
│   ├── How Does the Switch Learn MAC Addresses?
│   ├── How Does the Switch Forward Frames?
│   ├── Visual Example (Simplified)
├── How Switches Send Data/
│   ├── Store-and-Forward vs Cut-Through
│   ├── How Switches Store Messages
│   ├── Duplex and Speed
│   ├── Auto-MDIX (Cable Auto-Detect)
```


<br>

___

<br>


## [ICMP.md](ICMP.md)
```
ICMP/
├── What is ICMP?/
├── Common ICMP Messages/
│   ├── 1. Host Reachability
│   ├── 2. Destination Unreachable
│   ├── 3. Time Exceeded
├── ICMPv6 Extra Features (Neighbor Discovery)/
│   ├── 1. Router Solicitation (RS)
│   ├── 2. Router Advertisement (RA)
│   ├── 3. Neighbor Solicitation (NS)
│   ├── 4. Neighbor Advertisement (NA)
├── Ping and Traceroute Tests/
│   ├── What is Ping?
│   ├── Ping the Loopback Address
│   ├── Ping the Default Gateway
│   ├── Ping a Remote Host
├── What is Traceroute?/
│   ├── How does Traceroute work?
│   ├── What happens to those earlier packets (TTL = 1, 2, etc.)?
│   ├── So when are the real data packets sent?
│   ├── Real-life analogy
```



<br>

___

<br>


## [IP Static Routing.md](IP%20Static%20Routing.md)
```
IP Static Routing/
├── What is Static Routing?/
├── Why Use Static Routing?/
├── Types of Static Routes/
│   ├── 1. Standard static route
│   ├── 2. Default static route
│   ├── 3. Floating static route
│   ├── 4. Summary static route
├── How to Tell the Router Where to Send Data/
│   ├── 1. Next-hop IP address
│   ├── 2. Exit interface
│   ├── 3. Both next-hop and interface
├── The Example Situation/
│   ├── IPv4 Example
│   ├── IPv6 Example
├── Summary/
├── In Short/
```


<br>

___

<br>


## [Network Layer.md](Network%20Layer.md)
```
Network Layer/
├── Network Layer Characteristics/
│   ├── Key Services
│   ├── Basic Operations of the Network Layer
├── Why Can't the Network Layer Use MAC Addresses for Addressing?/
│   ├── What is a MAC Address?
│   ├── Key Characteristics
│   ├── 1. MAC Address is a Flat Address (Not Hierarchical)
│   ├── 2. MAC Addresses Are Vendor-Based
│   ├── 3. IP Address Provides Logical, Hierarchical Addressing
│   ├── 4. MAC Addresses Work Only on Local Networks
├── How a Host Routes/
│   ├── How a Host Sends Data (Routing Basics)
│   ├── Where can a device send data?
│   ├── How does it decide if local or remote?
│   ├── What is a Default Gateway (DGW)?
│   ├── How does a device know its Default Gateway?
│   ├── How to see routing table on Windows
├── What is Routing?/
│   ├── When a router gets a packet, it
│   ├── Types of Routes in Routing Table
│   ├── Static Routing
│   ├── Dynamic Routing
```


<br>

___

<br>


## [Network Security.md](Network%20Security.md)
```
Network Security/
├── Security Threats and Vulnerabilities/
│   ├── Types of Security Threats
│   ├── Types of Vulnerabilities
│   ├── Physical Security Threats
├── Network Attacks/
│   ├── Types of Malware
│   ├── Reconnaissance Attacks
│   ├── Access Attacks
│   ├── Denial of Service (DoS) Attacks
├── Network Attack Mitigations/
│   ├── Defense-in-Depth Approach
│   ├── Keep Backups
│   ├── Upgrade, Update, and Patch
│   ├── Authentication, Authorization, and Accounting (AAA)
│   ├── Firewalls and the DMZ
│   ├── Types of Firewalls
│   ├── Endpoint Security
```



<br>

___

<br>




## [Routing Concepts.md](Routing%20Concepts.md)
```
Routing Concepts/
├── Path Determination/
├── Packet Forwarding/
├── Basic Router Configuration/
├── IP Routing Table/
├── Path Determination/
│   ├── Router's Main Jobs
│   ├── Path Determination (Choosing the Best Route)
│   ├── Example (IPv4)
│   ├── Example (IPv6)
│   ├── How Routes Get Into the Routing Table
├── Packet Forwarding/
│   ├── Part 1: How the Router Knows Where to Send Things (Path Determination)
│   ├── Part 2: How the Router Sends the Packet (Forwarding)
│   ├── Part 3: How Fast the Router Sends It (Forwarding Methods)
│   ├── Summary
├── Basic Router Configuration/
│   ├── Router Verification Commands
│   ├── Filtering Command Output
├── IP Routing Table/
│   ├── Route Sources and Their Codes
│   ├── Routing Table Principles
│   ├── Routing Table Entries
│   ├── Directly Connected Networks
│   ├── Static Routes
│   ├── Dynamic Routing Protocols
│   ├── Default Route
│   ├── Routing Table Structure
│   ├── Administrative Distance (AD)
```


<br>

___

<br>


## [switching-concepts.md](switching-concepts.md)
```
Switching Concepts/
├── What is a Switch?/
│   ├── What Does It Do?
│   ├── Real-life Example (Home Wi-Fi)
│   ├── Why Not a Hub?
├── Frame Forwarding/
│   ├── Basic Terms
│   ├── How a Switch Learns and Forwards (2 Steps)
│   ├── Important Notes
│   ├── Analogy
├── What Happens When a Switch Receives Data?/
│   ├── 1. Store-and-Forward Switching (Cisco's Preferred Way)
│   ├── 2. Cut-Through Switching
│   ├── Summary
├── Switching Domains/
│   ├── 1. Collision Domains
│   ├── 2. Broadcast Domains
│   ├── 3. How Switches Reduce Congestion
│   ├── In Short
```


<br>

___

<br>


## [Transport Layer.md](Transport%20Layer.md)
```
Transport Layer/
├── Transport Layer/
│   ├── Role of the Transport Layer
│   ├── Responsibilities of the Transport Layer
│   ├── Why Transport Protocols Are Needed
├── TCP Overview (Transmission Control Protocol)/
│   ├── Key Features of TCP
│   ├── TCP Header Fields
│   ├── Applications That Use TCP
├── UDP Overview/
│   ├── What is UDP?
│   ├── Key Features of UDP
│   ├── UDP Header
│   ├── Applications That Use UDP
├── Port Numbers/
│   ├── Socket Pairs
│   ├── Port Number Ranges
│   ├── Examples of Well-Known Ports
│   ├── Checking Connections with netstat
├── TCP Communication Process/
│   ├── TCP Server Processes
│   ├── TCP Connection Establishment (Three-Way Handshake)
│   ├── ACK SYN numbers in Three Way HandShake
│   ├── Session Termination
│   ├── Purpose of the Three-Way Handshake
│   ├── TCP Control Flags
```


<br>

___

<br>


## [VLAN.md](VLAN.md)
```
VLAN/
├── What is VLAN?/
│   ├── Why do we use VLANs?
│   ├── Key Concept
├── Types of VLANs/
│   ├── 1. Default VLAN
│   ├── 2. Data VLAN (User VLAN)
│   ├── 3. Voice VLAN
│   ├── 4. Management VLAN
│   ├── 5. Native VLAN
```


<br>

___

<br>


## [WAN.md](WAN.md)
```
WAN/
├── LAN vs. WAN/
├── Private vs. Public WAN/
│   ├── Private WAN
│   ├── Public WAN
├── WAN Topologies/
│   ├── 1. Point-to-Point Topology
│   ├── 2. Hub-and-Spoke Topology
│   ├── 3. Dual-Homed Topology
│   ├── 4. Fully Meshed Topology
│   ├── 5. Partially Meshed Topology
├── Carrier Connections/
│   ├── What is a carrier?
│   ├── Types of connections
├── Evolving networks/
│   ├── Small network
│   ├── Campus network
│   ├── Branch network
│   ├── Distributed network
```


<br>

___

<br>


## [WLAN.md](WLAN.md)
```
WLAN/
├── WLAN/
│   ├── LAN vs WLAN
│   ├── Types of Wireless Networks
│   ├── Wireless Technologies
│   ├── Frequency Bands Used in WLAN
├── WLAN Components/
│   ├── Wireless NICs (Network Cards)
│   ├── Wireless Home Router
│   ├── Wireless Access Point (AP)
│   ├── Types of Access Points
│   ├── Wireless Antennas
├── WLAN Operation/
│   ├── Types of Wireless Modes
│   ├── BSS and ESS
│   ├── 802.11 Frame Structure
│   ├── CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)
│   ├── Wireless Device and AP Connection Steps
│   ├── Passive and Active Discovery
├── Channel Management in WLAN/
│   ├── Channel Saturation
│   ├── Channel Selection in WLAN
│   ├── Planning WLAN Deployment
├── WLAN Threats/
│   ├── Common Threats
│   ├── DoS Attacks
│   ├── Rogue Access Points
│   ├── Man-in-the-Middle (MITM) Attack
├── Secure WLANs/
│   ├── Authentication Methods
│   ├── Encryption Protocols
│   ├── Enterprise Security
```

<br>

___

<br>

## Documentation
All markdown files in this networking study repository have been documented with their hierarchical content structures. This README provides a comprehensive navigation guide for easy reference and study.

## Study Notes
- Each file contains detailed explanations with examples
- Visual aids and diagrams are included where applicable
- Files are structured for easy navigation and reference
- Topics build upon each other for comprehensive understanding
- Complete coverage from basics to advanced networking concepts

## Repository Structure
This repository now contains **16 comprehensive networking study files** covering:
- **Fundamentals**: Basics, protocols, addressing
- **Data Link Layer**: Ethernet, switching, VLANs
- **Network Layer**: IP routing, ICMP, static routing
- **Transport Layer**: TCP/UDP, port numbers
- **Application Layer**: DNS, DHCP, web protocols
- **Network Infrastructure**: WAN topologies, WLAN management
- **Network Security**: Threats, vulnerabilities, mitigations

<br>

___

<br>
