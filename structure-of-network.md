# Structure of Network

[OSI Model](#osi-model) <br>
[TCP IP Model](#tcp-ip-model) <br>
[Real World Example](#real-world-example) <br>



## OSI Model

- It stands for Open Systems Interconnection Modal.
- There are 7 layers in this model:

```
Application Layer
Presentation Layer
Session Layer
Transport Layer
Network Layer
Data Link Layer
Physical Layer
```

<br>

### Application Layer

- It is implemented in the application itself.
- This is the only layer the user directly interacts with.
- Some protocols used are HTTP, FTP, etc.
- The application layer will give data to next layer which is Presentation Layer.

<br>

### Presentation Layer

- This layer handles encryption, encoding, translation, etc of the data received by the application layer.
- This layer assumes that the next layer which is Session Layer will convert the data by itself for further processing.
- SSL (Secure Socket Layer) is used for encryption and encoding in this layer.

<br>

### Session Layer

- This layer focuses on setting up the connection and managing it and then enabling processing of data followed by termination of the connected sessions.
- This layer assumes that the next layer which is transport layer will send the data once the connection is established.

<br>

### Transport Layer

- This layer divides the data into segments which have a sequence number attached to them to align them sequentially in the received device.
- This layer has `Flow Control` which manages the upload speed of the sending device according to the receiving device so we do not lose any data packet during the data sending process.

<br>

### Network Layer

- This layer takes data segments from transport layer and then transports it from uploading device to the downloading device.
- Router is a part of network layer.
- The function of this layer is logical addressing.

<br>

### Data Link Layer

- This takes data packet from network layer and does logical address and physical addressing.
- MAC Address is used for physical addressing.
- A frame is the data unit that is has the MAC Address to it added by the data link layer.
- After creating these data frames, all the above layers can access these frames and control how they are placed and received.
- Adds MAC Address to frames or data segments received from network layer.

  
<br>

### Physical Layer

- This is the lowest layer of the OSI model and is responsible for the actual transmission of data over a physical medium.
- It deals with bit transmission through electrical, optical, or radio signals.
- This layer defines hardware components such as cables, switches, and network interface cards (NICs).
- It ensures data is transmitted in the form of bits and is received correctly at the other end.
- Common technologies at this layer include Ethernet, USB, and fiber optics.

<br>

### Flowchart

- This flow shows how a packet goes layer by layer from uploading device to downloading device.

```
- Application -> Message formed by the user and this layer sends it to presentation layer.
- Presentation -> Transports the message by modifying it (encoding, encrypting, decrypting, etc).
- Session -> Creates a connection between devices and sends the message to transport layer.
- Transport -> Makes the message into packets and segments and sends it to network layer.
- Network -> Bundles and assigns IP Addresses to packets and sends it to Data Link layer.
- Data Link -> Adds MAC Address to the received frames and sends it to physical layer.
- Physical -> Sends the data to physical router.
```

<br>

___

<br>


## TCP IP Model

- It stands for Internet Protocol Suite.
- This model has 5 layers:

```
Application Layer
Transport Layer
Network Layer
Data Link Layer
Physical Layer
```

- The working of the layers is same as OSI Model but with few exceptions.
- OSI model's Application, Presentation, Session are merged together into Application.
- This is used practically and OSI is used for theory and concepts.

<br>

___

<br>

## Real World Example
<br>

ME ->A->P->S->T->N->D->P->My Router -> ISP -> ISP -> His Router -> P->D->N->T->S->P->A-> MY FRIEND

<br>

- 1. My device (computer, phone, etc.) is sending data:  
   - The data moves through the OSI layers in my device, reaching the Physical Layer.  
   - The Physical Layer converts the data into signals (electrical for Ethernet, optical for fiber, or radio waves for Wi-Fi).
     
<br>

2. My router receives these signals:  
   - Since the router is physically connected to my device (via cable or Wi-Fi), it receives the signals at its own Physical Layer.  
   - The router processes the data through its OSI layers (moving from the Physical Layer up to the Network Layer).  
   - The router reads the destination IP address in the Network Layer and decides where to send the data next.
  
     
<br>

3. My router sends the data to the internet:  
   - The router converts the data back into signals (like electrical pulses or Wi-Fi signals).  
   - It sends those signals to my ISP (Internet Service Provider).  
   - The ISP routes the data across the internet, through multiple network devices (other routers, servers, etc.).  

<br>

4. My friend's router receives the data:  
   - The router receives incoming data signals from the ISP and converts them back into a stream of bits at the Physical Layer.  
   - The Data Link Layer checks the MAC address and ensures the data is meant for a device in my friend's network.  
   - The Network Layer reads the destination IP address to determine which device in the network should receive the data.  
   - The Transport Layer reassembles packets and ensures error checking before passing the data upwards.  
   - The Session Layer manages the connection and ensures the correct application receives the data.  
   - The Presentation Layer decrypts and decompresses the data if needed.  
   - Finally, the Application Layer delivers the data to the app that requested it, such as a web browser or messaging app.






<br>

___

<br>

