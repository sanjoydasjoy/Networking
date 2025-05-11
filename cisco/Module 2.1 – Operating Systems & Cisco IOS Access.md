## **Module 2.1 – Operating Systems (Summary)**

### **2.1.1 OS Basics**

* **Operating System (OS)** manages hardware and software.
* **Kernel**: Core part of OS that controls hardware and system resources.
* **Shell**: Interface between user and OS. Two types:

  * **CLI (Command-Line Interface)**: Uses typed commands.
  * **GUI (Graphical User Interface)**: Uses icons, windows, and menus.

<br>

___

<br>

### **2.1.2 GUI vs CLI**

* **GUI** (Windows, macOS, Android, etc.): Easy to use, no need to know commands.
* **CLI** (used in Cisco devices): Requires command knowledge but is faster, more stable, and uses fewer system resources.
* Network devices (e.g. routers/switches) are mostly configured using **CLI**.
* Cisco OS types: **IOS, IOS XE, IOS XR, NX-OS**.
* Home routers: Use **firmware** and typically have a **browser-based GUI**.

<br>

___

<br>

### **2.1.3 Purpose of an OS**

* On **PCs (GUI)**: Use mouse, view output, type commands.
* On **Network devices (CLI)**: Type commands to configure/view output.
* Cisco devices come with a default IOS version, but it can be upgraded for more features.

<br>

___

<br>

### **2.1.4 Access Methods**


* **Console**:

  * Connect directly using a cable.
  * Use when the device is new or has no settings.
  * Works even without network.

* **Telnet/SSH**:

  * Connect over the internet or LAN.
  * SSH = Secure, Telnet = Not secure.
  * Needs network to be set up first.

* **AUX (Auxiliary)**:

  * Old method using phone line and modem.
  * Used when you can't access over the internet.




<br>

___

<br>

### **2.1.5 Terminal Emulation Programs**

Tools for CLI access:

* **PuTTY**
* **Tera Term**
* **SecureCRT**

These tools let you connect via console or SSH/Telnet, and customize the interface.

<br>

___

<br>


## **2.1.6 Check Your Understanding – Cisco IOS Access**

### **Question 1:**

**Which access method would be most appropriate if you were in the equipment room with a new switch that needs to be configured?**
→ **Answer: Console**
*Because you're physically near the device and it has no initial config.*



### **Question 2:**

**Which access method would be most appropriate if your manager gave you a special cable and told you to use it to configure the switch?**
→ **Answer: Console**
*That special cable is likely a console cable (RJ-45 to USB or serial).*



### **Question 3:**

**Which access method would be the most appropriate in-band access to the IOS over a network connection?**
→ **Answer: Telnet/SSH**
*These use the network itself to connect remotely. SSH is preferred for security.*



### **Question 4:**

**Which access method would be the most appropriate if you call your manager to tell him you cannot access your router in another city over the internet and he provides you with the information to access the router through a telephone connection?**
→ **Answer: Aux**
*Auxiliary (AUX) port allows dial-up access through a modem.*

<br>

___

<br>
