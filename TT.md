# SET A Question:

<br>

### **Task A: Compare and Contrast (Any TWO) (2 × 3 = 6 Marks)**  
Compare and contrast the following pairs (Answer any two):

1) OSI Model vs TCP/IP Model  
2) Connection-Oriented vs Connection-Less Communication  
3) CSMA/CD vs CSMA/CA

<br><br>

### **Task B: Explanation (Any FOUR) (4 × 4 = 16 Marks)**  
Explain any four of the following:

1) The OSI Model and the TCP/IP Model  
2) Connection-Oriented and Connection-Less Communication  
3) CSMA/CD  
4) CSMA/CA  
5) Token Passing  
6) Encapsulation in Networking

<br><br>

### **Task C: Justification (2 × 4 = 8 Marks)**  
Answer both of the following:

1) What is the purpose of a MAC address, and how is it different from an IP address?  
2) What is the significance of encapsulation in networking? Explain how it works in the context of the OSI model.

<br>

___

<br>


# SET A Answer:

<br>

### **Task A: Compare and Contrast**

<br>

#### **1) OSI Model vs TCP/IP Model**

| Aspect | OSI Model | TCP/IP Model |
|--------|-----------|--------------|
| **Full Form** | Open Systems Interconnection | Transmission Control Protocol/Internet Protocol |
| **Layers** | 7 Layers | 4 Layers |
| **Design Approach** | Theoretical, reference model for learning and design | Practical model used in real-world networking |
| **Standardization** | Developed by ISO as a standard framework | Developed by the U.S. DoD for internetworking |
| **Layer Separation** | Clear distinction between all layers (especially Presentation and Session) | Combines some OSI layers (e.g., Application, Presentation, and Session into one) |
| **Protocol Dependency** | Protocol-independent | Built around standard protocols like TCP, IP, HTTP, etc. |

<br><br>

#### **2) Connection-Oriented vs Connection-Less Communication**

| Aspect | Connection-Oriented | Connection-Less |
|--------|----------------------|------------------|
| **Setup Required** | Yes, connection must be established first | No setup needed before sending data |
| **Reliability** | Reliable: ensures delivery, order, and error correction | Unreliable: no delivery or order guarantee |
| **Overhead** | Higher overhead due to control packets and acknowledgments | Lower overhead, faster transmission |
| **Examples** | TCP (used in emails, file transfers, web browsing) | UDP (used in video streaming, online gaming) |
| **Flow Control** | Supports flow and congestion control | No flow or congestion control |
| **Suitability** | Suitable for critical data transmission | Suitable for time-sensitive or real-time data |

<br><br>

#### **3) CSMA/CD vs CSMA/CA**

| Aspect | CSMA/CD (Collision Detection) | CSMA/CA (Collision Avoidance) |
|--------|-------------------------------|--------------------------------|
| **Used In** | Wired networks (like Ethernet) | Wireless networks (like Wi-Fi) |
| **How It Works** | Listens, transmits, and checks for collisions; retransmits if collision occurs | Listens and waits; avoids collisions using backoff and acknowledgment |
| **Collision Handling** | Detects collisions after they occur | Tries to prevent collisions before they happen |
| **Performance** | Can suffer in high-traffic environments due to frequent retransmissions | Better in wireless environments where collision detection is difficult |
| **Efficiency** | Less efficient under heavy load | More efficient for shared wireless mediums |
| **Protocol Example** | Ethernet (IEEE 802.3) | Wi-Fi (IEEE 802.11) |

<br>

<br>

<br>

### Task B: Explanation (Any FOUR) 

<br>

### 1. The OSI Model and the TCP/IP Model

The **OSI Model** is a 7-layer conceptual framework developed by ISO to standardize networking processes. It helps understand how data travels from one computer to another through layers:  
1. Physical  
2. Data Link  
3. Network  
4. Transport  
5. Session  
6. Presentation  
7. Application  

The **TCP/IP Model**, used in real-world internet communication, has 4 layers:  
1. Network Access  
2. Internet  
3. Transport  
4. Application  

**Key Points**:  
- OSI is theoretical, used for learning; TCP/IP is practical and widely implemented.  
- TCP/IP combines some OSI layers.  
- Both models define roles of protocols and guide data communication.

<br><br>

### 2. Connection-Oriented and Connection-Less Communication

**Connection-Oriented Communication** requires a setup before actual data transfer. It ensures that data reaches the destination correctly and in order. It uses acknowledgments, flow control, and error correction.  
**Example**: TCP

**Connection-Less Communication** sends data without any prior connection setup. It’s faster but doesn’t guarantee delivery or order. It is useful for applications that can tolerate data loss.  
**Example**: UDP

**Key Points**:  
- Connection-oriented = reliable but slower.  
- Connection-less = faster but less reliable.  
- Applications choose based on need for reliability vs speed.

<br><br>

### 3. CSMA/CD (Carrier Sense Multiple Access with Collision Detection)

Used in **wired networks** like Ethernet. In CSMA/CD, devices listen to the channel before sending data. If the channel is free, they transmit.  
If two devices send at the same time, a **collision** happens. Both stop, wait a random time (backoff), and try again.

**Key Points**:  
- Detects collisions **after** they occur.  
- Reduces but does not eliminate collisions.  
- Mostly used in older half-duplex Ethernet.  
- Not used in modern full-duplex switched networks.

<br><br>

### 4. CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)

Used in **wireless networks** like Wi-Fi. Devices first sense the channel, then **wait** before transmitting to avoid collisions. They may send a **Request to Send (RTS)** and wait for **Clear to Send (CTS)**.

Because detecting collisions is hard in wireless, CSMA/CA tries to **prevent** them from happening.

**Key Points**:  
- Avoids collisions before they occur.  
- Adds delays and acknowledgments to ensure smooth transmission.  
- Used in IEEE 802.11 (Wi-Fi) networks.  
- Improves wireless efficiency and reduces interference.

<br><br>

### 5. Token Passing

A **token** is a small data packet that circulates in the network. Only the device that holds the token is allowed to send data. After sending, it passes the token to the next device.

**Key Points**:  
- Prevents collisions and ensures fair access.  
- Used in Token Ring and FDDI networks.  
- Ensures orderly transmission without fighting for the medium.  
- Rare today, but concept is important for understanding controlled access.

<br><br>

### 6. Encapsulation in Networking

Encapsulation is the process of **wrapping data with headers** (and sometimes trailers) at each layer of the OSI or TCP/IP model.

**How it works** (during sending):  
- Application data is passed to lower layers.  
- Each layer (like Transport, Network, Data Link) adds its own **header** (e.g., TCP header, IP header, MAC header).  
- At the receiving side, each layer **removes its header** (decapsulation) and passes data up.

**Key Points**:  
- Helps identify and deliver data correctly.  
- Each header contains control info for that layer.  
- Essential for organized and layered communication.

<br><br><br>



### Task C: Justification 

<br>

### 1. What is the purpose of a MAC address, and how is it different from an IP address?

A **MAC address (Media Access Control address)** is a unique identifier assigned to a network device’s **hardware** (like a network card). It is **permanent** and works at the **Data Link Layer (Layer 2)** of the OSI model.

An **IP address (Internet Protocol address)** is a **logical address** assigned to a device for identifying it on a network. It is **changeable** and works at the **Network Layer (Layer 3)**.

**Differences**:
- **MAC** is physical, fixed, and identifies **devices** within a local network (like a home Wi-Fi).
- **IP** is logical, can change, and identifies **location** of devices on a wider network like the internet.

**Purpose**:
- MAC: Helps deliver frames within the same local network.
- IP: Helps route packets between different networks.

**Analogy**:  
MAC is like your **device’s fingerprint**, IP is like its **temporary address on the internet**.

<br><br>

### 2. What is the significance of encapsulation in networking? Explain how it works in the context of the OSI model.**

**Encapsulation** is the process of adding headers (and sometimes trailers) to data as it moves **down the OSI layers** from the application to the physical transmission.

**Significance**:
- Organizes data so each layer knows **how to handle it**.
- Ensures **correct delivery**, **error detection**, and **routing**.
- Allows different layers to work **independently** and communicate properly.

**How it works (in OSI)**:
1. **Application Layer (Layer 7)** generates user data.
2. **Transport Layer (Layer 4)** adds a transport header (e.g., TCP/UDP) for delivery control.
3. **Network Layer (Layer 3)** adds an IP header for routing.
4. **Data Link Layer (Layer 2)** adds MAC addresses in the frame header, and sometimes a trailer.
5. **Physical Layer (Layer 1)** converts the final frame into bits and transmits it.

At the receiving side, the data is **decapsulated** in reverse order — each layer removes its own header and passes the rest up.

**In short**: Encapsulation ensures data is properly packed, tracked, and guided from sender to receiver across a network.


<br>

___

<br>



