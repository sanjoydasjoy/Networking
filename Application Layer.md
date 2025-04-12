

### 🟩 Application Layer
- Role: Interfaces directly with user applications and the network.  
- Responsibility: Facilitates communication between software applications and lower network layers.  
- Key Protocols:  
  - HTTP – Web browsing (TCP port 80, 8080)  
  - FTP – File transfers  
  - TFTP – Simple file transfers  
  - IMAP – Email retrieval  
  - DNS – Translates domain names to IP addresses (TCP/UDP port 53)  

<br>

### 🟧 Presentation Layer
- Role: Ensures data is readable for the receiving system.  
- Responsibilities:  
  - Formatting/Translation: Converts data to a format understood by the destination (e.g., .docx to readable bytes)  
  - Compression: Reduces data size for efficient transmission  
  - Encryption: Secures data during transit and decrypts it upon arrival  

<br>

### 🟨 Session Layer
- Role: Manages sessions between applications.  
- Responsibilities:  
  - Session Control: Starts, manages, and ends communication sessions  
  - Dialog Management: Keeps sessions active and synchronizes communication  
  - Recovery: Restarts sessions if disconnected or idle too long  

<br>

### 🔌 TCP/IP Application Layer Integration
- In the TCP/IP model, these three OSI layers (Application, Presentation, Session) are grouped into one Application Layer.  
- Both devices (sender and receiver) must use compatible protocols at this layer for communication to succeed.
- TCP/IP Application Layer Protocols: DNS , HTTP, DHCP
  
<br><br>
DNS (Domain Name System), DHCP (Dynamic Host Configuration Protocol), and HTTP (Hypertext Transfer Protocol) are TCP/IP application layer protocols with different purposes. DNS resolves domain names like cisco.com into IP addresses, using UDP on port 53 for quick lookups and TCP for zone transfers. DHCP dynamically assigns IP addresses, using UDP with client requests on port 68 and server responses on port 67. HTTP transfers web content (text, images, videos) and relies on TCP (ports 80, 8080) for reliable data delivery. These protocols operate at the application layer but depend on TCP or UDP at the transport layer to move data across the network.


<br><br>




<br>

___

<br>


# P2P

Peer-to-Peer Networks-

## Peer-to-Peer (P2P) Networks
- In a client-server model, a client requests information, and a server responds. Both client and server processes are in the application layer.
- In P2P networks, two or more computers share resources (like printers or files) without a dedicated server. Each device, known as a peer, can act as both a server and a client, depending on the request.
- P2P applications let a device act as both client and server in the same session, handling both requests and responses. Some use a hybrid model, where peers first contact an index server to locate a resource, then connect directly to the peer that has it.

### Common P2P Applications
- BitTorrent, Direct Connect, eDonkey, and Freenet are examples of P2P applications where each computer in the network can function as both a client and a server.





<br>

___

<br>


# Client-Server vs. Peer-to-Peer Networking

The client-server model and peer-to-peer (P2P) model are different in how devices communicate and share resources.

<br>

### 🖥️ Client-Server Model
- Structure: Centralized  
- Roles: Devices have fixed roles — clients request, servers respond  
- Example: When you access a website, your browser (client) sends a request to a web server, which responds with the page  
- Resource control: Managed centrally by the server  
- Scalability: Scales well with proper infrastructure  
- Security: Easier to secure and manage  
- Examples of applications:  
  - Web browsing (HTTP)  
  - Email (IMAP, SMTP)  
  - Online banking  
  - Cloud storage (Google Drive, Dropbox)

<br>

### 🔄 Peer-to-Peer (P2P) Model
- Structure: Decentralized  
- Roles: Devices act as both client and server depending on the transaction  
- Example: In file sharing via BitTorrent, your computer can download (client role) and upload (server role) files at the same time  
- Resource control: Distributed among peers  
- Scalability: Grows easily with more users but harder to manage  
- Security: More difficult to secure due to lack of central control  
- Examples of applications:  
  - File sharing (BitTorrent, eDonkey)  
  - Blockchain and cryptocurrency networks  
  - Collaborative tools (Skype, older versions of Zoom)



<img src="assets/client-server-vs-p2p.png"  width="600">


<br>

___

<br>

# Web and Email Protocols

<br>

### Web Communication: HTTP and HTML

When you enter a web address (URL) in a browser:

1. The browser interprets the URL parts:  
   - Protocol: http  
   - Server name: www.cisco.com  
   - File name: index.html

2. The browser checks with a DNS server to convert the name into an IP address.

3. A GET request is sent to the web server asking for the index.html page.

4. The server responds with the HTML code, which the browser reads and displays.

<br>

### HTTP and HTTPS

HTTP is a request/response protocol using the following message types:

- GET: Requests data (like web pages) from a server  
- POST: Sends form data or files to a server  
- PUT: Uploads files or resources to a server  

Note: HTTP is not secure, as data is transmitted in plain text, making it vulnerable to interception; HTTPS (Hypertext Transfer Protocol Secure) encrypts the data using SSL/TLS, ensuring secure communication and verifying the server's identity to protect against attacks like man-in-the-middle.



<br>

### Email Communication

Email is a store-and-forward service. Messages are stored on mail servers and retrieved by clients using specific protocols.

<br>

### Email Protocols

- SMTP (Simple Mail Transfer Protocol):  
  Used to send emails between client and server or from one server to another  
  - Works over port 25  
  - Requires a message header and body  

- POP (Post Office Protocol):  
  - Used to receive emails  
  - Downloads emails and deletes them from the server  
  - Uses port 110  
  - Not ideal for centralized backups  

- IMAP (Internet Message Access Protocol):  
  - Also used to retrieve emails  
  - Keeps original messages on the server  
  - Allows syncing across multiple devices  
  - Messages are only deleted when the user chooses to  

<br>

___

<br>


#  IP Addressing Services


### **DNS (Domain Name System)**  
- Turns website names (like `www.google.com`) into IP addresses (like `142.250.195.36`).  
- Helps your computer find websites using names instead of numbers.  
- If one DNS server doesn’t know the answer, it asks another one.  

<br>

#### DNS Record Types:  
- **A** – IPv4 address  
- **AAAA** – IPv6 address  
- **MX** – Mail server info  
- **NS** – Name server info  

<br>

### **DNS Message Parts**  
When your device talks to a DNS server, it sends a message with:  
- **Question** – What name you’re asking about  
- **Answer** – The IP address  
- **Authority** – Who gave the answer  
- **Additional** – Any extra help info  

<br>

### **DNS Hierarchy**  
- DNS is like a big family tree – each server is in charge of a small part.  
- If one can’t answer, it passes the question up the tree.  
- Top-level examples: `.com`, `.org`, `.uk`

<br>

### **nslookup Command**  
- Tool to check if DNS is working.  
- You can type a name like `google.com` and it shows the IP address.

<br>

### **DHCP (Dynamic Host Configuration Protocol)**  
- Gives your device an IP address automatically when you connect to a network.  
- No need to set the IP manually.  

<br>

#### DHCP Process (4 Steps):  
1. **Discover** – Device asks for an IP  
2. **Offer** – Server offers an IP  
3. **Request** – Device says “I’ll take it”  
4. **Acknowledge** – Server confirms  



<br>

___

<br>
