[How the Internet All Started](#how-the-internet-all-started)  <br>
[Client Server Architecture](#client-server-architecture) <br>
[Protocols](#protocols) <br>
[How Data is Transfered](#how-data-is-transfered) <br>
[Ports](#ports) <br>
[How Countries Connected](#how-countries-connected) <br>
[LAN MAN WAN](#lan-man-wan) <br>
[Modem and Router](#modem-and-router) <br>
[Topologies](#topologies) <br>


<br>

___

<br>


## How the Internet All Started:

#### ❏ The Cold War & the Space Race
- During the **Cold War**, the **USA** and **USSR** were competing for **technological superiority**. The **USSR** took the lead by launching **Sputnik**, the first artificial satellite, into orbit.  
- In response, the **USA** wanted to stay competitive and began a research program called **ARPA** (Advanced Research Projects Agency). ARPA’s goal was to enhance the USA’s technological capabilities, especially in **defense and communication**.



<br><br><br>



#### ❏ ARPA and the Birth of ARPANET  
- **ARPA** developed a system that allowed **researchers** to **communicate** and share information with each other across different locations.  
- However, there was a challenge: How could they communicate **effectively** between different buildings?  
- To solve this, ARPA developed **ARPANET** in **1969**, which was the **first version of the internet**.  
- Initially, it connected just **four research centers**:  
  - **MIT (Massachusetts Institute of Technology)**  
  - **Stanford University**  
  - **UCLA (University of California, Los Angeles)**  
  - **University of Utah**  
- ARPANET was **research-focused**, not for public use, and used a set of **protocols** (rules) for communication.



<br><br><br>



#### ❏ The Missing Piece: Hyperlinks and the World Wide Web (WWW)  
- Early systems like ARPANET lacked an **easy way** to navigate between documents. For example, **clicking a link** in one document to move to another document was missing—an essential feature for research papers.



<br><br><br>



#### ❏ The World Wide Web (WWW) and Tim Berners-Lee
- In **1989**, **Tim Berners-Lee**, a British computer scientist at CERN, developed the **World Wide Web (WWW)** as a solution to this problem.  
- The WWW allowed researchers to create **hyperlinked documents**—so that anyone could **click on a link** in a document and immediately access related information.  
- The **first website** ever was created at **CERN**:  
  - Website: [https://info.cern.ch/](https://info.cern.ch/)  
  - This website provided a way to access documents stored on the **World Wide Web**, marking the beginning of **hypertext and hyperlinking** on the internet.



<br><br><br>



#### ❏ Search Engines: The Next Step
- Initially, the World Wide Web was not **searchable**. To find documents or resources, you had to know their **exact URL**.  
- This led to the creation of the first **search engines** to index the growing amount of web pages.
  - The **first search engine** was **Yahoo!**, which started as a **web directory** and later evolved into a search engine.
  - Over time, more powerful search engines emerged, such as **Google**, which revolutionized the way we search and access information online.


<br><br><br>



#### ❏ Key Takeways:
- **ARPANET**, funded by ARPA, was the first **research-focused network** that allowed communication between different universities.  
- **Tim Berners-Lee** introduced the **World Wide Web** to solve the problem of easy document navigation, enabling the creation of **hyperlinks**.  
- The **first website** was launched at **CERN** in 1991, and soon after, **search engines** like **Yahoo!** helped people find documents more easily.  
- All these developments together laid the foundation for what we now know as the **internet**.

<br><br><br>

---


<br><br><br>


## Client Server Architecture

❏ Client-server architecture is a network model where a **client** (like your computer or browser) sends a request to a **server** (a system that processes and responds to the request). For example, when you visit **google.com**, your browser (the client) sends a request to Google’s server, which then returns the webpage. Your computer can act as both a **client** and a **server**; for instance, when using **localhost**, your computer hosts a local server (acting as the server) while your browser (acting as the client) sends requests to it and displays the response.


<br><br><br>

---

<br><br><br>


## Protocols


❏ Protocols are a set of rules defined by organizations like the **Internet Society** to standardize communication over the internet. These rules are documented in **RFCs** (Request for Comments), which anyone can contribute to.

- **TCP (Transmission Control Protocol)**: TCP ensures reliable data transmission by establishing a connection between the sender and receiver, ensuring that the data reaches its destination without corruption and in the correct order. It is used for critical applications like web browsing, email, and file transfer.

- **UDP (User Datagram Protocol)**: Unlike TCP, UDP does not guarantee delivery or order of data, making it faster but less reliable. It’s often used for applications where speed is more important than complete accuracy, such as **video conferencing** or **online gaming**.

- **HTTP (Hypertext Transfer Protocol)**: HTTP is used by **web browsers** to transfer data between clients (like your computer) and servers. When a client makes a request (e.g., to load a webpage), the server responds using HTTP, formatting the data for transfer.


<br><br><br>

---

<br><br><br>


## How Data is Transfered

<br>

Everything online is ultimately represented as 0s and 1s. To efficiently transfer large files or data, we don’t send everything at once. Instead, data is broken down into smaller units, called **packets**, which are sent across the network. Whether it's websites, movies, or any other data, it all comes in these packets. <br>

When inspecting network activity (e.g., using the **Network tab** in browser developer tools), you can see these **data packets** for each request.

<br><br>

#### **How Do Computers Find Each Other?**
When you search **google.com**, the system must determine which server to connect to. This is done via **IP addresses**. Each device, whether a computer, server, or router, is identified using an IP address, which can either be public or private.

<br><br>

#### **How Internet Connections Work:**

- **ISP and IP Address**: My **Internet Service Provider (ISP)** provides a **modem/router** with a **public IP address**. Devices in my home connect to this router and are assigned **private IP addresses** through **DHCP (Dynamic Host Configuration Protocol)**.
  
- **Router and NAT**: When I make a request, such as accessing **Google**, the request appears to come from the **public IP address** assigned by the ISP, not from the individual device's private IP. Google then sends its response to the public IP address. The router uses **NAT (Network Address Translation)** to forward the response to the correct device within my local network.


<br><br><br>

#### **How Does the Router Know Which Application to Send Data to?**
While all devices within a network share the same **public IP address**, the router needs to direct incoming data to the correct application on the right device. This is done using **port numbers**. Each application that communicates over the network is assigned a unique **port number**, which helps the router identify which application should receive the data.

- For example, when my friend and I are communicating over an application, both of us have an **IP address** and a **port number**. 
  - **IP address**: Identifies the location of the device.
  - **Port number**: Identifies which application on the device should handle the communication.
  
When I send a message, the application uses a specific port number to send the data. The data travels across the internet, and when it reaches my friend's device, their router uses the port number to forward it to the correct application.

<br><br>


#### **Private vs. Public IPs:**
1. **Private IP (Local Communication)**:
   - Devices within the same local network (e.g., home or office) use private IP addresses (e.g., **192.168.x.x** or **10.x.x.x**).
   - The data stays within the local network and doesn’t require internet communication.
  
2. **Public IP (Over the Internet)**:
   - When devices are in different locations, the data passes over the internet, and public IP addresses are used to identify each device. 
   - The router translates between the **public** and **private IPs** using NAT.

3. **Ports**:
   - Regardless of whether the communication is over a private or public IP, **ports** are crucial in determining which application receives the data. For example, a video call app might use **port 3478 (STUN)** or another designated port.
  
So, when you're talking to your friend over the internet, your devices first use **public IPs** to locate each other, and then **private IPs** within each local network to communicate. The **port number** ensures the data reaches the correct application.



<br><br><br>

---

<br><br><br>


## Ports


Ports are **16-bit numbers**, meaning they can range from **0 to 65,535** (2^16). A **port number** helps a computer determine which application should receive incoming network data.

<br>

For example, when you visit a website using **HTTP**, your request is sent to **port 80** on the web server. Other services also have well-known ports, such as:

- HTTP** (Web Browsing) → **Port 80**
- HTTPS** (Secure Web Browsing) → **Port 443**
- **FTP** (File Transfer Protocol) → **Port 21**
- SSH** (Secure Shell for remote login) → **Port 22**
- **DNS** (Domain Name System) → **Port 53**
- **SMTP** (Email Sending) → **Port 25**
- **MongoDB** (Database) → **Port 27017**
- **MySQL** (Database) → **Port 3306**
- **PostgreSQL** (Database) → **Port 5432**
- **Microsoft SQL Server (MSSQL)** → **Port 1433**

<br><br>

#### **Port Ranges:**
Port numbers are divided into three categories:

1. **Well-Known Ports (0–1023)**:
   - Reserved for essential system services such as **HTTP (80)**, **HTTPS (443)**, and **SSH (22)**.

2. **Registered Ports (1024–49,151)**:
   - Assigned to specific applications like **MongoDB (27017)**, **MySQL (3306)**, and others.

3. **Dynamic (Ephemeral) Ports (49,152–65,535)**:
   - These ports can be used freely for temporary connections, such as when a browser opens a new tab.

<br><br>

#### **IP Address Commands:**
- **Private IP** (Local Network):
   - Windows: `ipconfig`
   - Linux/macOS: `ifconfig`

- **Public IP** (Internet-facing):
   - Command: `curl ifconfig.me`
   - Visit: [What Is My ISP](https://www.whatismyisp.com/)
     

<br><br><br>

---

<br><br><br>



## How Countries Connected




### **How Do Two Computers Communicate?**  

<br>


There are **two main ways** computers communicate:  

1️. **Guided Communication (Wired)**
   - A **fixed physical path** is used for communication.  
   - Examples: **Ethernet cables, fiber optic cables, coaxial cables.**  

2.  **Unguided Communication (Wireless)**
   - Data is transmitted **without a fixed path**, through airwaves.  
   - Examples: **Wi-Fi, Bluetooth, 3G, 4G, LTE, 5G, satellites.**  

<br><br>

### **How Are Countries Connected to the Internet?**  

#### **1️. Physically (Wired Communication)**  
- **Optical Fiber Cables** – Used for high-speed internet connections.  
- **Coaxial Cables** – Used for cable internet and TV connections.  
- **Submarine Cables** – Undersea fiber optic cables that connect different countries.  
  - 🌍 **See the global submarine cable map here:**  
    [https://www.submarinecablemap.com/](https://www.submarinecablemap.com/)  

#### **2️. Wirelessly (Wireless Communication)**  
- **Wi-Fi** – Short-range wireless internet.  
- **Bluetooth** – Short-range communication between devices.  
- **3G, 4G, LTE, 5G** – Mobile internet provided by cellular networks.  
- **Satellites** – Used for remote areas but slower than fiber optics.  

<br><br>

### **Why Do We Use Undersea Cables Instead of Satellites?**  

**Undersea cables are used because they are much faster and more reliable than satellites.**  
- **Lower latency** – Data travels through fiber optic cables faster than through satellites.  
- **Higher bandwidth** – Cables can carry **much more data** than satellites.  
- **More stable** – Unlike satellites, cables aren’t affected by weather conditions.  

 
 **Satellites are still useful** for remote areas, disaster recovery, and military communication, but **undersea cables handle most of the world's internet traffic**.  



<br><br><br>

---

<br><br><br>


## LAN MAN WAN



### **LAN, MAN, WAN: Types of Networks**  

#### **1️⃣ LAN (Local Area Network)**  
- A **LAN** connects devices in a **small area**, like a **home** or **office**.  
- It can support **many devices** (not just 5 or 10, but thousands if needed).  
- Devices in a LAN communicate using **Ethernet cables**, **Wi-Fi**, or **Bluetooth**.  
- **Network adapters and switches** are used to connect and manage devices.  
- **LANs can also work with wireless networks (Wi-Fi)** for convenient device connections.  

<br><br>

#### **2️⃣ MAN (Metropolitan Area Network)**  
- A **MAN** spans a **larger geographic area**, typically across a **city** or **large campus**.  
- It connects multiple LANs within a city, providing high-speed communication across urban areas.  

<br><br>

#### **3️⃣ WAN (Wide Area Network)**  
- A **WAN** connects networks over **large distances**, such as between **different countries** or across continents.  
- The **internet** is an example of a global WAN, connecting millions of LANs and MANs worldwide.  
- **WANs** are commonly connected using **optical fiber cables**, providing high-speed communication over long distances.  

<br><br>

### **Wide Area Network Technologies**  
- **SONET (Synchronous Optical Networking)** – A technology used for high-speed **optical fiber networks**, providing reliable and fast data transmission over long distances.  
- **Frame Relay** – An older **WAN technology** that uses packet-switched networks to provide efficient and cost-effective data transfer across wide areas, though it’s being phased out in favor of newer technologies like **MPLS**.  

<br><br><br>

### **The Internet: A Collection of LANs, MANs, and WANs**  
- The **internet** is essentially a **global network** made up of many interconnected LANs, MANs, and WANs.  
- These networks are connected to each other through various technologies, allowing communication between devices worldwide.



<br><br><br>

---

<br><br><br>



## Modem and Router

### Modem vs. Router

#### **1️⃣ Modem (Modulator-Demodulator)**  
- Converts **digital signals** from a computer into **analog signals** for transmission over telephone lines, and vice versa.  
- Example: When you send data (like an image) over an old **DSL connection**, the modem **modulates** it into electrical signals. At the receiving end, another modem **demodulates** it back into digital form.  
- Essential for **connecting to the internet** if using DSL or cable internet.  

<br><br>


#### **2️⃣ Router**  
- A device that **routes data packets** between devices and networks based on **IP addresses**.  
- It **distributes** the internet connection from the modem to multiple devices in a network (Wi-Fi or wired).  
- Helps different devices in a network **communicate** with each other.  

<br><br>

### **How They Work Together:**  
- The **modem connects to the ISP** (Internet Service Provider) and brings internet to your home.  
- The **router distributes** that internet to multiple devices via **Wi-Fi or Ethernet cables**.  
- Modern devices often combine both into a **single modem-router**.  



<br><br><br>

---

<br><br><br>


## Topologies

### **Network Topologies: How Devices Are Connected**  

1️⃣ **Bus Topology** – All devices share a **single central cable**; data travels in both directions.  

2️⃣ **Ring Topology** – Devices are connected in a **closed loop**, and data moves in **one direction** (or both in dual-ring).  

3️⃣ **Star Topology** – All devices connect to a **central hub/switch**, making it **easy to manage** but dependent on the hub.  

4️⃣ **Tree Topology (Bus-Star Hybrid)** – A **hierarchical structure** combining multiple **star networks** connected by a **bus**.  

5️⃣ **Mesh Topology** – Every device connects to **every other device**, providing **high reliability** but requiring more cables.  


<br><br><br>

---

<br><br><br>


