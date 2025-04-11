# 📦 What is a **VLAN**?

- **VLAN** stands for **Virtual Local Area Network**.
- It's like **creating mini-networks** inside a physical switch.
- You group similar devices **logically**, not physically.

> 💡 Think of VLANs like rooms in a building: people in one room can talk easily with each other, but they need permission (a door or hallway) to talk to people in another room.

<br>

## 📁 **Why Use VLANs?**

| **Benefit**               | **Explanation** |
|---------------------------|-----------------|
| 🔇 **Smaller Broadcast Domains** | Devices in one VLAN don’t hear broadcasts from another. Less unnecessary traffic. |
| 🔐 **Improved Security** | Only devices in the same VLAN can talk directly—helps separate users (e.g., students vs staff). |
| ⚙️ **Better Organization** | Easier to manage groups like IT, HR, Sales separately. |
| 💸 **Reduced Cost** | No need for multiple switches—**one switch** can support multiple VLANs. |
| 🚀 **Improved Performance** | Less traffic on each VLAN = **faster network**. |
| 🧠 **Simpler Management** | Same type of users/devices grouped together → easy to apply policies and manage apps. |

<br>

## 🧠 Key Concept:

> 🔄 **All devices in the same VLAN can communicate freely. To talk between VLANs, a router or Layer 3 switch is needed.**

<br>

___

<br>


# Types of VLANs



### 🔹 1. **Default VLAN**  
- **VLAN 1** is the default for everything (data, management, native).
- Comes pre-configured on all Cisco switches.
- **You can't delete or rename it.**


```
💡 *Best practice:* Don’t use VLAN 1 for actual traffic—create your own.
By default, all switch ports are part of VLAN 1, and it’s used for everything (data, management, etc.).

But using VLAN 1 for everything is not safe or efficient because:

🔓 Security risk:
If everything runs through VLAN 1, attackers know where to look.

⚠️ Too much traffic:
VLAN 1 can get flooded with unnecessary broadcasts.

🧹 No separation:
You can’t organize devices into groups (like students vs. teachers).


✅ So, what should we do?
Instead of using VLAN 1, we should:
 - Create a new VLAN (e.g., VLAN 10 for users, VLAN 99 for management).
 - Assign ports/devices to these VLANs.
 - Leave VLAN 1 unused or reserve it for special tasks (like switch-to-switch communication).

```

<br>

### 🔹 2. **Data VLAN**  
- Carries **user traffic** like browsing, emails, apps.
- By default, all ports are in VLAN 1 (which is a data VLAN by default).
- 💡 Create your own VLANs (e.g., VLAN 10 for students, VLAN 20 for teachers).

<br>

### 🔹 3. **Native VLAN**  
- Used **only on trunk links** (links that carry multiple VLANs between switches).
- Frames from this VLAN are **not tagged**.
- 💡 Make sure the **Native VLAN matches** on both ends of the trunk.

<br>

### 🔹 4. **Management VLAN**  
- Used for managing the switch via **SSH, Telnet, or SNMP**.
- Should **NOT** be the same as a user/data VLAN.
- 💡 Typically, you'll create a separate VLAN (like VLAN 99) just for switch management.

<br>

### 🔹 5. **Voice VLAN**  
- Special VLAN for **VoIP (Voice over IP)** phones.
- Needs:
  - Guaranteed bandwidth
  - Low delay (less than **150 ms**)
  - High priority traffic (QoS)
- 💡 This helps keep **voice calls smooth** and not laggy.

<br>

___

<br>
