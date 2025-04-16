
### **What is DHCPv4?**

- **DHCPv4** stands for **Dynamic Host Configuration Protocol version 4**.
- My Internet Service Provider (ISP) provides a modem/router with a public IP address. Devices in my home connect to this router and are assigned private IP addresses through DHCP (Dynamic Host Configuration Protocol).
- This saves time — especially helpful in networks with **lots of devices**.

<br>

___

<br>

### **How it works:**

- A **DHCP server** has a **pool of IP addresses**.
- When a device (like your laptop) joins the network, the server **"leases"** an IP address to it for a certain amount of time.
- Once the time is up, the device has to **renew** the lease (often it gets the **same address again**).


  <br>
  So, basically, 
  <br>

- Your phone/laptop connects to Wi-Fi.
- Your **router** is running a **DHCP server**.
- The router says: “Here’s your IP address, DNS, and gateway info.”
- Your device is ready to go online.

Unless you turn it off manually, **every home router does this by default** using DHCP.

<br>

___

<br>

### **Where is it used?**

- In **big networks**, there’s usually a **dedicated DHCP server**.
- In **small offices or home networks (SOHO)**, even a **router (like a Cisco router)** can act as a DHCP server.

<br>

___

<br>



### What is **DHCP Lease Time**?

Think of it like **renting an IP address** for a limited time.

<br>

### Here's how it works:

1. Your device joins a network (like Wi-Fi).
2. The router gives it an **IP address** — but not forever!
3. It says:  
   > “You can **use this IP address for 24 hours** (or however long the lease time is).”

<br>

### What happens when the lease ends?

- Your device will **ask for the IP again**.
- Most of the time, it gets **the same IP back**.
- If not, it gets a **new one** from the router.

<br>

### Why is there a time limit?

- So unused IPs don’t get stuck forever.
- Devices come and go — especially on big networks (schools, offices).
- This helps keep the IP system clean and efficient.



<br><br>


### **4 DHCP Steps – DORA:**

1. **D – Discover**  
   - The client (your device) broadcasts a **DHCP Discover** message to find available DHCP servers.

2. **O – Offer**  
   - The DHCP server responds with a **DHCP Offer**, suggesting an available IP address and configuration details.

3. **R – Request**  
   - The client replies with a **DHCP Request**, asking to use the offered IP address.

4. **A – Acknowledge**  
   - The server sends a **DHCP Acknowledgement (ACK)**, confirming that the IP address is leased to the client.

---

### **Summary Table:**

| Step | Name       | Who Sends It | Purpose                              |
|------|------------|--------------|--------------------------------------|
| 1    | Discover   | Client       | Looking for DHCP server              |
| 2    | Offer      | Server       | Offers an IP address                 |
| 3    | Request    | Client       | Requests offered IP                  |
| 4    | Acknowledge| Server       | Confirms and assigns the IP          |



### **What about the public IP?**

- The **router** itself (Wi-Fi access point) gets **one public IP address** from the **ISP (Internet Service Provider)**.
- All your internal devices **share that one public IP** using a process called **NAT (Network Address Translation)**.



### **Conclusion:**
- **The IP from DHCP is a Private IP.**
- **The Public IP is assigned to your router by the ISP.**
- **NAT helps all devices use the internet through that one public IP.**


<br>

___

<br>

