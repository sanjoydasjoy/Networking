**(1) What do you mean by the term Hacker? Give examples of different types of hackers.**  
→ A **hacker** is someone who uses technical knowledge to gain unauthorized access to systems or networks.  
**Types of Hackers:**  
- **White Hat:** Ethical hackers who help secure systems.  
- **Black Hat:** Malicious hackers who break into systems for harm or gain.  
- **Gray Hat:** Hackers who might break into systems without permission but without harmful intent.  
- **Script Kiddies:** Inexperienced hackers using pre-made tools.  
- **Hacktivists:** Hackers with political or social motivations.

---

**(2) List different types of ICMP messages. State purposes of any two.**  
→ **Types of ICMP Messages:**  
- Echo Request and Echo Reply  
- Destination Unreachable  
- Time Exceeded  
- Redirect Message  
- Source Quench (obsolete)  
**Purposes:**  
- **Echo Request/Reply:** Used in ping to test connectivity.  
- **Destination Unreachable:** Informs the sender that the destination is not reachable.

---

**(3) What are the features of a default gateway? Explain how does a host route to the default gateway.**  
→ A **default gateway** is a router that connects a local network to other networks (like the internet).  
**Features:**  
- Acts as the exit point for traffic leaving the network.  
- Stores routes for external IPs.  
**Routing Process:**  
- If a host wants to communicate with an IP outside its subnet, it sends the packet to the default gateway, which then forwards it appropriately.

---

**(4) What Is NAT? How Does NAT Work?**  
→ **NAT (Network Address Translation)** is used to map **private IP addresses** to a **public IP address** to allow internet communication.  
**How it Works:**  
- A NAT-enabled router replaces the source private IP with its public IP when sending traffic out.  
- It maintains a mapping table to route return traffic to the correct internal host.

---

**(5) Describe the steps of TCP communication process.**  
→ The **TCP communication** process includes:  
1. **Three-way Handshake:**  
   - SYN → Client sends connection request  
   - SYN-ACK → Server acknowledges and responds  
   - ACK → Client confirms and connection is established  
2. **Data Transfer:** Reliable and ordered delivery of data.  
3. **Connection Termination:** Four-step FIN-ACK process to close connection gracefully.

---

**(6) What are the common solutions to mitigate the layer 2 vulnerabilities?**  
→ **Layer 2 (Data Link Layer)** vulnerabilities include MAC spoofing, ARP poisoning, and switch attacks.  
**Solutions:**  
- **Port Security**: Restrict access to switch ports based on MAC addresses  
- **Dynamic ARP Inspection (DAI)**: Protects against ARP spoofing  
- **MAC Address Filtering**  
- **Using VLANs** to segment networks and isolate threats  
- **Disabling unused ports**

---


**(7) Explain the four basic characteristics of a reliable network architecture.**  
→ A **reliable network architecture** should have the following characteristics:  
1. **Fault Tolerance** – The network should be able to continue functioning even if certain components fail (e.g., having redundant paths or backup devices).  
2. **Scalability** – The network should be designed to handle increased load without degradation of performance, allowing for easy expansion.  
3. **Quality of Service (QoS)** – The network should be able to prioritize certain types of traffic (such as voice or video) to ensure optimal performance for high-priority data.  
4. **Security** – The architecture should protect against unauthorized access, cyber threats, and other vulnerabilities by using encryption, access control, and monitoring.

---

**(8) How does the DHCP process work? In which cases is static addressing used?**  
→ **DHCP Process:**  
1. **DHCP Discover:** The client sends a broadcast to find DHCP servers.  
2. **DHCP Offer:** The server responds with an available IP address and other configuration details.  
3. **DHCP Request:** The client responds, confirming the IP offer.  
4. **DHCP Acknowledgment:** The server acknowledges the request, and the client is assigned the IP address.

**Static Addressing is used when:**  
- Devices need a fixed, unchanging IP address (e.g., servers, network printers).  
- It's important for systems to always be reachable at the same IP (e.g., for remote management).

---

**(9) Define risk, vulnerability, and threat, in the context of network security.**  
→ **Risk:** The potential for loss or damage that can result from a threat exploiting a vulnerability.  
**Vulnerability:** A weakness or flaw in a system (e.g., unpatched software, weak password policies) that can be exploited.  
**Threat:** A potential cause of an attack or exploit (e.g., hackers, malware, denial-of-service attacks) that could exploit a vulnerability.

---

**(10) What is ACL used for? Suppose you want to filter traffic coming to a server. In this case, where can you place the network ACL?**  
→ **ACL (Access Control List)** is used to control access to network resources by filtering traffic based on IP addresses, protocols, or ports.  
To filter traffic **coming to a server**, you would place the **network ACL on the router or firewall interface closest to the source** of the incoming traffic. This ensures that only allowed traffic reaches the server.

---

**(11) How is a frame processed when a device forwards a message to an Ethernet network?**  
→ When a device forwards a message to an Ethernet network:  
1. The message is encapsulated in a **frame** that contains the destination MAC address and source MAC address.  
2. The frame is then sent to the Ethernet network.  
3. A **switch** on the network checks the **destination MAC address** and forwards the frame to the correct port.  
4. The destination device receives the frame and processes the data.

---

**(12) How can you protect the network perimeter from outside access?**  
→ To protect the network perimeter from outside access:  
- **Firewalls:** Implement firewalls to monitor and filter incoming and outgoing traffic based on security rules.  
- **Intrusion Detection and Prevention Systems (IDS/IPS):** Detect and block suspicious activities.  
- **Strong Authentication:** Use multi-factor authentication for remote access.  
- **Close Unused Ports:** Disable unnecessary ports and services on routers, switches, and firewalls.  
- **Apply Patches and Updates:** Regularly update software and devices to protect against vulnerabilities.  
- **Network Segmentation:** Use VLANs, DMZs, and segmentation to isolate critical network parts.

---


**(13) Why do we need port addressing? State the range of valid port numbers.**  
Port addressing is necessary because it allows the operating system to direct data to the correct application or service running on a device. When data arrives at a device, the IP address identifies the destination system, and the port number identifies the application or service on that system.  

**Port Number Range:**
- **Well-known Ports:** 0 to 1023 (e.g., HTTP uses port 80, HTTPS uses port 443).
- **Registered Ports:** 1024 to 49151 (used by applications and services registered with IANA).
- **Dynamic/Private Ports:** 49152 to 65535 (used by client applications dynamically).

---

**(14) What is ARP? Write its functions.**  
**ARP (Address Resolution Protocol)** is used to map a known **IP address** to its corresponding **MAC address** on a local network. It operates at the Data Link layer and helps devices on the same network communicate with each other.  

**Functions of ARP:**
1. **ARP Request:** When a device needs to communicate with another device on the same local network but doesn't know its MAC address, it broadcasts an ARP request to all devices on the network.
2. **ARP Reply:** The device with the matching IP address replies with its MAC address, allowing the requesting device to establish a communication link.
3. **ARP Cache:** Devices store the IP-MAC address mappings in an ARP cache to avoid sending repeated requests.

---

**(15) Explain why IP is called a connectionless and best-effort delivery service.**  
**IP (Internet Protocol)** is called a **connectionless** protocol because it does not establish a connection between the sender and receiver before transmitting data. It simply sends packets without confirming that the recipient is ready to receive them. 

It is also considered a **best-effort delivery service** because:
- IP makes no guarantees regarding the delivery of packets (no acknowledgments, retransmissions, or error correction).
- If a packet is lost or delayed, it is up to higher-layer protocols (like TCP) to handle retransmission or error recovery.

---

**(16) Create 1100 subnets with a slash 8 prefix.**  
To create **1100 subnets** from a network with a **/8 prefix**, we need to determine how many bits are required for subnetting. The number of subnets is determined by the formula:  

**Number of subnets = 2^n**, where **n** is the number of bits borrowed from the host portion of the address.

1. Start with a **/8 prefix** (i.e., 8 bits are allocated to the network).
2. To find **n**, solve for 2^n ≥ 1100. The smallest **n** where 2^n ≥ 1100 is **11** (because 2^11 = 2048).
3. So, we need to borrow **11 bits** from the host portion, which will make the new subnet mask **/19** (8 bits for the network and 11 bits for subnetting).

Thus, with a **/8** network, using **/19** will allow you to create **2048 subnets**, which is more than sufficient for the required **1100 subnets**.

---



**(18) Briefly describe the layers of the TCP/IP model.**  
The **TCP/IP model** consists of four layers, each responsible for different aspects of networking:

1. **Application Layer:** This layer includes protocols that provide network services directly to end-users or applications, like HTTP, FTP, and DNS. It handles tasks like file transfers and web browsing.
  
2. **Transport Layer:** Responsible for end-to-end communication between hosts, ensuring reliable data transfer. Key protocols include TCP (provides reliable, ordered data delivery) and UDP (provides fast but unreliable data transfer).

3. **Internet Layer:** Handles addressing and routing of data packets across the network using IP (Internet Protocol). It determines the best path for data to travel from the source to the destination.

4. **Network Access Layer:** Deals with the physical transmission of data over a medium (like Ethernet or Wi-Fi). It also includes error detection and correction mechanisms at the data link layer.

---

**(19) What approaches are used to define the end of a variable-size frame? Explain how they are used.**  
There are two main approaches used to define the end of a variable-size frame:

1. **Byte Counting:** In this method, the header contains the number of bytes in the frame. This helps the receiver know when to stop reading the frame. Common in protocols like **PPP** (Point-to-Point Protocol).

2. **Delimiter:** A special character or sequence of characters (e.g., a start-of-frame or end-of-frame marker) is used to mark the end of the frame. This approach is commonly used in protocols like **HDLC** (High-Level Data Link Control).

Both methods help the receiver know where the frame ends and avoid confusion during transmission.

---

**(20) How do routers build their routing tables? Explain with an example.**  
Routers build their **routing tables** using the following methods:

1. **Static Routing:** The network administrator manually configures routes. For example, a router might have a static route specifying that all traffic for the 10.0.0.0 network should go to a next-hop address of 192.168.1.1.

2. **Dynamic Routing:** Routers use **routing protocols** (e.g., OSPF, RIP, BGP) to automatically learn routes. For example, if Router A knows that the 192.168.1.0 network is reachable through Router B, it adds this information to its routing table. These routes are constantly updated as network conditions change.

---

**(21) How does the DHCP process work? In which cases is static addressing used?**  
The **DHCP process** involves the following steps:

1. **DHCP Discover:** A client sends a broadcast message to find DHCP servers.
2. **DHCP Offer:** The DHCP server replies with an offer, including an IP address and other network information.
3. **DHCP Request:** The client accepts the offer by sending a request message.
4. **DHCP Acknowledgment:** The DHCP server confirms the assignment of the IP address to the client.

**Static addressing** is used when devices need a fixed IP address, such as for servers, printers, and network infrastructure devices that must always be reachable at the same address, or in environments where DHCP is not desired for security or control reasons.

---

**(22) Explain the collision handle technique in CSMA/CD used by IEEE 802.**  
**CSMA/CD (Carrier Sense Multiple Access with Collision Detection)** is a method used to manage access to a shared communication medium, such as Ethernet, to avoid data collisions. Here’s how the collision handling technique works in **IEEE 802** (Ethernet):

1. **Carrier Sense (CS):** Before transmitting, the sender listens to the channel to check if it is idle (no transmission is occurring). If the channel is busy, the sender waits for it to become idle.
2. **Transmit (Multiple Access):** Once the channel is idle, the sender transmits its data.
3. **Collision Detection (CD):** While transmitting, the sender continues to listen to the channel. If a collision is detected (due to two devices transmitting at the same time), both devices stop transmitting immediately.
4. **Backoff Mechanism:** After detecting a collision, each sender waits for a random amount of time before attempting to retransmit. This random backoff is meant to reduce the chance of another collision occurring immediately after.

This technique ensures that all devices have fair access to the communication medium while minimizing data collisions.

---

**(23) What is the broadcast and network address for host 222.129.199.222/21?**  
Given the IP address **222.129.199.222** and the subnet mask **/21**, let's calculate the **network address** and the **broadcast address**.

- **Subnet Mask (/21):**  
  A **/21** subnet mask corresponds to a **255.255.248.0** mask in decimal.

- **Network Address:**  
  To calculate the network address, we perform a bitwise AND operation between the IP address and the subnet mask.  

  IP: **222.129.199.222**  
  Subnet Mask: **255.255.248.0**  
  Network Address: **222.129.192.0**

- **Broadcast Address:**  
  The broadcast address is calculated by setting all host bits (the bits that are 0 in the subnet mask) to 1. The **/21** subnet mask gives us the first 21 bits for the network, and the remaining 11 bits are for the host. The broadcast address for this subnet would be:

  Broadcast Address: **222.129.199.255**

---

**(24) Contrast between the client-service and P2P service model. Name some common applications.**  
The **client-service** model and the **peer-to-peer (P2P)** model are two common network communication models:

1. **Client-Service Model:**  
   - In this model, a **client** sends requests to a **server**, which processes the request and sends a response back to the client.
   - The server typically has more resources and controls the network services.
   - **Examples of Applications:**  
     - Web browsing (HTTP)
     - Email (SMTP, IMAP)
     - File sharing (FTP)
   
2. **Peer-to-Peer (P2P) Model:**  
   - In this model, each device (peer) can act as both a **client** and a **server**. Peers can share resources and communicate directly with one another.
   - There is no central server, and resources are distributed among the peers.
   - **Examples of Applications:**  
     - File sharing (BitTorrent)
     - Voice over IP (VoIP) services (Skype)
     - Online gaming (e.g., peer-to-peer matchmaking in games)

---

**(25) Why is it said that FTP sends control information “out-of-band”?**  
**FTP (File Transfer Protocol)** is said to send control information **"out-of-band"** because it uses separate channels for data transfer and control commands:

1. **Control Channel:** FTP establishes a control connection over **port 21** for sending commands like **USER**, **PASS**, **LIST**, and other FTP commands. This channel is used exclusively for managing the session.
2. **Data Channel:** Data transfer (such as file uploads or downloads) occurs over a separate channel, which can either be **port 20** (for active mode) or a random port (for passive mode).

By using separate channels for control and data, FTP ensures that control information (e.g., commands, status messages) does not interfere with the actual file transfer, which is why it's considered "out-of-band."

---
