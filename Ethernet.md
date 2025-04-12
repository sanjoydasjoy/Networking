### 🔌 **What Ethernet Is**
- A wired networking technology for connecting devices in a LAN — uses cables (usually Cat5e, Cat6, etc.) 
- Defines rules for how data is transmitted over those cables.
- Technical name for ethernet is 802.3
- If we buy an Ethernet NIC card, it operates up to Layer 2 of the OSI model
- LLC is the part of driver, its 802.2
- MAC (half of data link layer) and physical layer is basically the ethernet and called 802.3

  
<img src="assets/ethernet1.png"  width="400">


<br>

### 🧩 What It Does
- Connects all your devices together on the same network—whether it's computers, printers, routers, etc.
- Shares internet across devices: Simply plug an **Ethernet cable** into your **device** and the **router** or **modem** to get online (just like Wi-Fi, but with a cable).
  - Multiple devices can be connected to the router/modem via Ethernet cables.
  - Each device (PC, laptop, console) plugs into one of the router's Ethernet ports. Most routers have 4 LAN ports, but some may have more.
  - The router's WAN port connects to your modem or incoming internet line.
- If you need more devices connected than the router has ports, you can use a network switch. A switch adds more Ethernet ports, allowing more devices to be connected to the router.
- Transfers files and shares resources between devices: Devices connected via Ethernet can send and receive data (files, etc.) from each other quickly.
- Works with Wi-Fi: Ethernet doesn’t replace Wi-Fi; it just gives wired access instead of wireless. Both can exist in the same network.
- Perfect for gaming, video calls, or large downloads because it’s more stable than Wi-Fi.





<br>

### ⚙️ How It Works
- Each device has a **network interface card (NIC)**, which is a hardware component that allows it to connect to the network. The NIC has a unique **MAC address** (Media Access Control address), which helps identify the device on the network.
- Data is sent in small chunks called **frames**. A frame contains not only the data being sent but also control information (like the sender's MAC address, the receiver's MAC address, and error-checking information).
- Ethernet defines the rules for how these frames are **formatted**, **sent**, and **checked for errors**. This ensures that the data is correctly transmitted, and if there are any issues (like data corruption), the frame can be flagged and sent again if necessary.

<br>



### Ethernet vs Wi-Fi
| Feature       | Ethernet                    | Wi-Fi                       |
|---------------|-----------------------------|-----------------------------|
| Speed         | Faster                      | Slower (in most cases)      |
| Stability     | More stable (less interference) | Can be unstable             |
| Mobility      | Not portable (needs cable)  | Fully wireless              |

<br>

___

<br>
