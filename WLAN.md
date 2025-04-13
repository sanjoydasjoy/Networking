# WLAN 

A WLAN (Wireless Local Area Network) is designed for short-range wireless communication—typically within a home, office, or campus. It allows devices like laptops and phones to connect to a local network without physical cables, using radio waves.

- WLANs enable wireless access in homes, offices, and campuses  
- Support mobility for users and devices  
- Easy to adapt and scale as needs change  
- Reduce reliance on physical cables and wiring  


### LAN vs WLAN

A LAN (Local Area Network) connects devices within a small area like a home, office, or campus. It can use wired cables, wireless connections, or both.

A WLAN (Wireless LAN) is a type of LAN that uses only wireless connections, typically over Wi-Fi.

| Type    | Medium            | Example                           |
|---------|-------------------|-----------------------------------|
| LAN     | Wired or Wireless | Office network with desktops and printers |
| WLAN    | Wireless only     | Home Wi-Fi connecting phones and laptops  |

<br><br>
- All WLANs are LANs  
- Not all LANs are WLANs  
- WLAN is useful for mobility and flexibility without physical cables
<br><br>

### Types of Wireless Networks  
- WPAN – Short-range (6–9 meters), low power. Uses Bluetooth and Zigbee (IEEE 802.15, 2.4 GHz)  
- WLAN – Medium-range (up to 300 feet). Used in homes/offices. Based on IEEE 802.11 (2.4/5 GHz)  
- WMAN – Covers cities or districts. Uses licensed frequencies  
- WWAN – Covers large areas like countries. Uses licensed frequencies (e.g. cellular networks)

<br><br>

### Wireless Technologies  
- Bluetooth – Used for short-distance device pairing (up to 100m)  
  - BLE: Supports mesh networks for IoT  
  - BR/EDR: Suited for audio and point-to-point links  
- WiMAX – Wireless broadband (IEEE 802.16), up to 50 km range  
- Cellular Broadband – Used in phones, tablets, cars  
  - GSM: Global standard  
  - CDMA: Used mostly in the US  
- Satellite – Internet via geostationary satellites. Good for remote areas. Needs line of sight

<br><br>

### Frequency Bands Used in WLAN  
- 2.4 GHz (UHF) – Used by 802.11b/g/n/ax  
- 5 GHz (SHF) – Used by 802.11a/n/ac/ax  

<br>

___

<br>


### WLAN Components 

- Wireless NICs (Network Cards)  
  - Devices like phones, laptops, and tablets have built-in wireless cards to connect to Wi-Fi  
  - If a device doesn’t have one, a USB Wi-Fi adapter can be plugged in to connect  

- Wireless Home Router  
  - A small box used in homes to connect devices  
  - Works as:  
    - an access point to give Wi-Fi  
    - a switch to connect wired devices  
    - a router to connect to the internet  

- Wireless Access Point (AP)  
  - A device that sends out Wi-Fi signals  
  - Devices like phones or laptops connect to it  
  - After logging in, users can use the network or internet  

- Types of Access Points  
  - Autonomous APs  
    - Work alone  
    - Set up one by one by someone manually  
  - Controller-based APs (also called lightweight APs)  
    - Controlled by a central device called a wireless LAN controller (WLC)  
    - Set up and managed automatically  

- Wireless Antennas  
  - Omnidirectional  
    - Sends signal in all directions  
    - Good for homes and offices  
  - Directional  
    - Sends signal in one direction like a beam  
    - Good for long-distance connections  
  - MIMO (multiple antennas)  
    - Uses more than one antenna  
    - Helps give faster and better Wi-Fi  

<br>

___

<br>


### WLAN Operation

Wireless networks can work in different ways and follow certain steps to connect devices.

<br>

#### Types of Wireless Modes
- Ad hoc mode  
  Devices connect directly to each other without using any router or access point  
- Infrastructure mode  
  Devices connect through a wireless access point (AP)  
- Tethering  
  A phone or tablet with mobile data creates a Wi-Fi hotspot for other devices

<br>

#### BSS and ESS
- Basic Service Set (BSS)  
  All wireless devices connect to one access point. Devices in different BSSs cannot talk to each other  
- Extended Service Set (ESS)  
  Combines multiple BSSs using wired connections. Devices in different BSSs can communicate through the ESS

<br>

#### 802.11 Frame Structure
- Similar to Ethernet frames but has more fields for wireless-specific information

<br>

#### CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)
Wi-Fi networks can't detect if two devices send data at the same time (collision), so they try to avoid it:
1. Device listens to the channel  
2. Sends a "ready to send" (RTS) message  
3. Waits for a "clear to send" (CTS) reply  
4. If no reply, waits and tries again  
5. Sends the data  
6. Waits for a reply. If no reply, assumes a collision and tries again

<br>

#### Wireless Device and AP Connection Steps
To connect to Wi-Fi, a device must:
1. Find the access point  
2. Prove its identity (authenticate)  
3. Join the network (associate)

To make this work, the device and AP must match on:
- SSID (network name)  
- Password  
- Wi-Fi standard (like 802.11n)  
- Security settings (like WPA2)  
- Channel or frequency

<br>

#### Passive and Active Discovery
- Passive mode  
  The AP sends out signals with its details like name, frequency, and security type  
- Active mode  
  The device searches for a known network by sending out requests on different channels

<br>

___

<br>


# Channel Management in WLAN

Channel management is a key aspect of WLAN operation, particularly when dealing with multiple wireless access points (APs) or devices on the same frequency band. It helps ensure optimal network performance by efficiently managing how wireless channels are selected and utilized.

<br><br>

#### Channel Saturation
- Problem: If too many devices use the same wireless channel, the network can slow down.
- How to Fix:  
  - DSSS: Spreads the signal over a wider frequency band, reducing interference (used by older WLANs like 802.11b).
  - FHSS: Quickly switches between different channels to avoid interference (used in the original 802.11).
  - OFDM: Splits one channel into smaller parts to use the frequency more efficiently (used in newer WLANs like 802.11a/g/n/ac).

<br><br>

#### Channel Selection in WLAN
- 2.4 GHz Band:  
  - Channels are 22 MHz wide, and they are spaced 5 MHz apart.
  - Tip: Use channels 1, 6, and 11 for best performance in crowded areas with multiple access points.
- 5 GHz Band:  
  - Offers 24 channels, each 20 MHz wide.
  - Tip: Use channels 36, 48, and 60 for better performance and less interference.

<br><br>

#### Planning WLAN Deployment
When setting up a WLAN, consider:
- Space Layout: Make sure to place APs where they provide good coverage.
- Number of Users: The more people and devices, the more APs you'll need.
- Data Needs: Higher data usage requires more APs and better placement.
- AP Placement: Choose non-overlapping channels for each AP to avoid interference.

<br>

___

<br>

# WLAN Threats

#### Common Threats
- Data Interception: Attackers can listen in on unprotected data.
- Unauthorized Access: Hackers or intruders can connect to the network.
- Denial of Service (DoS) Attacks: This disrupts the network, making it unavailable.
- Rogue Access Points: Unauthorized devices can join the network and cause harm.

<br><br>

#### DoS Attacks
- Causes: Misconfigured devices or malicious interference.
- Prevention: Secure devices, use strong passwords, and update settings during off-hours.

<br><br>

#### Rogue Access Points
- Definition: A device connected to the network without permission.
- Risks: It can steal data or allow hackers in.
- Prevention: Set rules on network controllers and monitor for unknown devices.

<br><br>

#### Man-in-the-Middle (MITM) Attack
- How It Works: An attacker secretly intercepts or alters data between two devices.
- Prevention: Make sure devices are properly authenticated and watch for unusual activity.

<br>

___

<br>

# Secure WLANs

Secure WLANs protect networks from unauthorized access and attacks by using methods like SSID cloaking, MAC address filtering, and strong authentication and encryption. These measures help ensure that only authorized users can connect and data remains safe.
<br>

- SSID Cloaking: Hides the network name (SSID) to prevent easy discovery by unauthorized users.
- MAC Address Filtering: Allows only specific devices, identified by their MAC addresses, to connect.

<br><br>

#### Authentication Methods:
- Open Authentication: No password required; commonly used for public networks.
- Shared Key Authentication: Requires a pre-shared password (WEP, WPA, WPA2, WPA3).

<br><br>

#### Encryption Protocols:
- WEP: Old and insecure. Should not be used.
- WPA/WPA2: Stronger encryption (WPA2 uses AES).
- WPA3: Latest and most secure, with protections like SAE for brute-force attacks and OWE for open networks.

<br><br>

#### Enterprise Security:
- WPA2 Enterprise: Uses a RADIUS server for centralized authentication.
- WPA3 Enterprise: Includes 192-bit encryption and more robust security for enterprises.


<br>

___

<br>
