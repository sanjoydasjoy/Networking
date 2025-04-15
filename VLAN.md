** What is VLAN?**  
VLAN stands for *Virtual Local Area Network*.  
It is a technology that allows us to divide a single physical network into multiple logical (virtual) networks. Devices in the same VLAN can communicate with each other as if they were on the same physical LAN, even if they are in different locations.

<br>

**Why do we use VLANs?**  
VLANs are used to:
- **Improve security**: Devices in different VLANs cannot communicate directly unless allowed.
- **Reduce broadcast traffic**: Each VLAN has its own broadcast domain.
- **Better network management**: Group users based on departments or functions, not physical location.
- **Flexibility and scalability**: Easily move devices between VLANs without changing cables.

<br>

## Key Concept:

> **All devices in the same VLAN can communicate freely. To talk between VLANs, a router or Layer 3 switch is needed.**

<br>

___

<br>


# Types of VLANs



1. **Default VLAN**  
   - The VLAN all switch ports are in when the switch is powered on.  
   - Usually VLAN 1.  
   - Used by control protocols like CDP, VTP.  
   - Cannot be deleted or renamed on most switches.


```
*Best practice:* Don’t use VLAN 1 for actual traffic—create your own.
By default, all switch ports are part of VLAN 1, and it’s used for everything (data, management, etc.).

But using VLAN 1 for everything is not safe or efficient because:

Security risk:
If everything runs through VLAN 1, attackers know where to look.

Too much traffic:
VLAN 1 can get flooded with unnecessary broadcasts.

No separation:
You can’t organize devices into groups (like students vs. teachers).


So, what should we do?
Instead of using VLAN 1, we should:
 - Create a new VLAN (e.g., VLAN 10 for users, VLAN 99 for management).
 - Assign ports/devices to these VLANs.
 - Leave VLAN 1 unused or reserve it for special tasks (like switch-to-switch communication).

```

<br>





2. **Data VLAN (User VLAN)**  
   - Used to carry regular user-generated data (emails, browsing, etc.).  
   - Typically assigned based on departments (e.g., VLAN 10 for HR, VLAN 20 for IT).  
   - Helps in segmenting and securing traffic.

3. **Voice VLAN**  
   - Special VLAN for **VoIP (Voice over IP)** traffic.  
   - Ensures good call quality by reducing delay (latency).  
   - Configured on ports connected to IP phones.

4. **Management VLAN**  
   - Used for managing network devices (e.g., SSH, Telnet, SNMP).  
   - Provides a secure path to manage switches, routers, etc.  
   - Best practice is to assign a separate VLAN (not VLAN 1) for management.

5. **Native VLAN**  
   - Used to carry **untagged traffic** across a trunk link.  
   - Only one native VLAN is allowed per trunk port.  
   - By default, it's VLAN 1, but it can be changed.  
   - Used for backward compatibility with older non-VLAN-aware devices.



<br>

___

<br>
