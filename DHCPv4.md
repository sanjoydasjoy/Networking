
### 🌐 **What is DHCPv4?**

- **DHCPv4** stands for **Dynamic Host Configuration Protocol version 4**.
- My Internet Service Provider (ISP) provides a modem/router with a public IP address. Devices in my home connect to this router and are assigned private IP addresses through DHCP (Dynamic Host Configuration Protocol).
- This saves time — especially helpful in networks with **lots of devices**.

<br>

___

<br>

### 🖥️ **How it works:**

- A **DHCP server** has a **pool of IP addresses**.
- When a device (like your laptop) joins the network, the server **"leases"** an IP address to it for a certain amount of time.
- Once the time is up, the device has to **renew** the lease (often it gets the **same address again**).


  <br>
  So, basically, 
  <br>

- ✅ Your phone/laptop connects to Wi-Fi.
- ✅ Your **router** is running a **DHCP server**.
- ✅ The router says: “Here’s your IP address, DNS, and gateway info.”
- ✅ Your device is ready to go online.

Unless you turn it off manually, **every home router does this by default** using DHCP.

<br>

___

<br>

### 🛠️ **Where is it used?**

- In **big networks**, there’s usually a **dedicated DHCP server**.
- In **small offices or home networks (SOHO)**, even a **router (like a Cisco router)** can act as a DHCP server.

<br>

___

<br>



### ⏱️ What is **DHCP Lease Time**?

Think of it like **renting an IP address** for a limited time.

<br>

### 📱 Here's how it works:

1. Your device joins a network (like Wi-Fi).
2. The router gives it an **IP address** — but not forever!
3. It says:  
   > “You can **use this IP address for 24 hours** (or however long the lease time is).”

<br>

### 🔁 What happens when the lease ends?

- Your device will **ask for the IP again**.
- Most of the time, it gets **the same IP back**.
- If not, it gets a **new one** from the router.

<br>

### ⏳ Why is there a time limit?

- So unused IPs don’t get stuck forever.
- Devices come and go — especially on big networks (schools, offices).
- This helps keep the IP system clean and efficient.



<br>

___

<br>

