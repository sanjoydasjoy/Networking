
### 🔌 What is a Switch?

A **switch** is a device that connects devices (like your phone, laptop, printer, etc.) within a **local network (LAN)** and allows them to **talk to each other**.


<br>

### 📦 What Does It Do?

Think of a switch like a super smart **traffic controller** inside your network. It:
1. **Receives** data (called **frames**) from one device.
2. **Checks** where that data is supposed to go.
3. **Forwards** it only to the right device — not to everyone.

This makes communication faster and more efficient.



<br>

### 🏠 Real-life Example (Home Wi-Fi)

Even if you're using **Wi-Fi** at home, your **Wi-Fi router has a built-in switch** that handles all the wired and wireless devices.

If:
- Your phone sends something to your smart TV,
- The switch makes sure it goes **only to the TV**, not to every other device.



<br>

### ⚙️ Why Not a Hub?

Before switches, there were **hubs** — they sent data to **all** connected devices. Switches are smarter: they send data **only** where it needs to go.

<br>

___

<br>

# **Frame Forwarding** 



### 🧩 Basic Terms

- **Ingress** = Frame **enters** the switch through a port.
- **Egress** = Frame **exits** the switch through a port.
- **MAC Address Table (CAM Table)** = A memory inside the switch that helps it remember which devices (MAC addresses) are connected to which ports.



<br>

### 🧠 How a Switch Learns and Forwards (2 Steps)

#### ✅ Step 1: **Learn**
When a frame enters the switch:
- The switch **looks at the source MAC address**.
- It checks if this MAC is already in its table.
  - If **not**, it **adds** it along with the port it came from.
  - If it **is**, it **refreshes the timer** (usually 5 mins) so it doesn’t expire soon.

#### 🚚 Step 2: **Forward**
Then the switch **looks at the destination MAC address**:
- If it's **already in the MAC address table**, it **forwards** the frame to the correct port (egress).
- If the switch doesn’t know where to send the data, it sends (or floods) the message to all other connected devices — except the one it came from. <br>
👉 It does this to try and find the right device. Once that device responds, the switch learns where it is and remembers it for next time.





<br>

### 📦 Important Notes
- A switch **never sends a frame back** out the same port it came in on.
- It constantly builds and updates the MAC address table as traffic flows.


<br>

### 💡 Analogy
Imagine a **mail sorter** at a post office:
- When someone drops a letter, the sorter checks who sent it and adds that info to the log.
- If the sorter knows where the recipient’s box is, they deliver it there.
- If they **don’t**, they shout the name across the whole office hoping someone replies.

<br>

___

<br>



# 🧠 **What Happens When a Switch Receives Data?**
The switch decides **how to forward it** using one of two methods:

<br>



### 🗃️ **1. Store-and-Forward Switching** (💡 Cisco’s Preferred Way)

- ✅ **Receives the entire data frame first** before sending it.
- 🧪 **Checks for errors** using something called FCS (Frame Check Sequence).
- 💾 **Temporarily stores** the data in memory (buffers it).
- ✅ **If the frame is clean**, then it forwards it.
- 🔄 Great for handling different port speeds (like slow input, fast output).

**✔️ Pros**: Reliable, checks for errors.  
**❌ Cons**: Slightly slower than cut-through.



<br>

### ⚡ **2. Cut-Through Switching**

- 🚀 **Sends the data almost instantly** after reading the destination address.
- 🧪 Doesn't wait to check for errors.
- 🔍 A version called **Fragment-Free** checks if the frame is at least 64 bytes (to avoid tiny, useless packets called "runts").

**✔️ Pros**: Super fast, great for ultra-low latency (under 10 microseconds).  
**❌ Cons**: Might forward bad data → could clog bandwidth with errors.



<br>

### 🆚 Summary:

| Feature                  | Store-and-Forward        | Cut-Through              |
|--------------------------|--------------------------|---------------------------|
| Error checking (FCS)?    | ✅ Yes                   | ❌ No                    |
| Speed                    | 🐢 Slower (more reliable) | ⚡ Faster (less reliable) |
| Suitable for mixed speeds? | ✅ Yes                   | ❌ No                    |
| Used by Cisco?           | ✅ Preferred method       | 🚫 Not default           |

<br>

___

<br>

# Switching Domains

Here's a **simplified explanation** of networking terms like **collision domains**, **broadcast domains**, and **how switches reduce congestion**:

<br>

## 🔄 **1. Collision Domains**

- **Collision domain**: A network area where data packets can **collide** if two devices send data at the same time.
- In **half-duplex mode**, devices can either **send or receive**, not both → **collisions** can happen.
- In **full-duplex mode** (default today), devices can **send and receive at the same time** → **no collisions**.
- Switches **break up** collision domains → each port on a switch is its **own collision domain**.

✅ **Result**: Less congestion, better performance.

<br>

## 📢 **2. Broadcast Domains**

- A **broadcast domain** is where **all devices hear broadcast messages** (like “Hey, is anyone using this IP?”).
- Switches **do NOT break** broadcast domains—they **forward broadcasts** to all devices on the LAN.
- **Routers** are the only devices that **break broadcast domains**.
- Too many devices = too many broadcasts = **slower network**.

📌 More devices = bigger broadcast domain = more traffic = potential congestion.

<br>

## 🚀 **3. How Switches Reduce Congestion**

Switches come with powerful features that help reduce network slowdowns:

| **Feature**             | **What It Does**                                                                 |
|-------------------------|----------------------------------------------------------------------------------|
| ⚡ **Fast Port Speeds** | Modern switches can go up to **100 Gbps** per port.                             |
| 🔁 **Fast Switching**   | Uses fast memory or bus systems to move data quickly.                           |
| 📦 **Frame Buffers**    | Temporarily store lots of data if there's a lot happening at once.              |
| 🧩 **High Port Density**| Connect more devices **directly to the switch** to keep traffic local and fast. |

<br>

## 🎯 In Short:

- **Switches** reduce collisions → each port = 1 collision domain.
- **Switches** expand broadcast domains → broadcasts go to all devices unless a router steps in.
- **Modern features** in switches help avoid slowdowns even with many connected devices.

<br>

___

<br>
