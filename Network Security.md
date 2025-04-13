# Security Threats and Vulnerabilities

### Types of Security Threats  
After a threat actor gains access to a network, they can cause the following types of damage:

1. Information theft – Stealing sensitive or confidential data  
2. Data loss and manipulation – Deleting or altering critical information  
3. Identity theft – Using stolen credentials to impersonate someone else  
4. Disruption of service – Preventing legitimate users from accessing network services (e.g., through DDoS attacks)  

<br><br>

### Types of Vulnerabilities  
A vulnerability is a weakness in a network or device that can be exploited. There are three main categories:

1. Technological vulnerabilities  
   - Weaknesses in protocols like TCP/IP  
   - Operating system flaws  
   - Weaknesses in networking hardware  

2. Configuration vulnerabilities  
   - Default or easily guessed passwords  
   - Poorly configured services or devices  
   - Unsecure default settings  

3. Security policy vulnerabilities  
   - Lack of formal policies  
   - Inadequate authentication and access controls  
   - No disaster recovery plan  

These weaknesses can lead to various attacks such as malware infections or unauthorized access.  

<br><br>

### Physical Security Threats  
Physical threats can also compromise network resources. They are categorized into:

1. Hardware threats – Physical damage to equipment like routers, switches, or servers  
2. Environmental threats – Issues like extreme temperature or humidity  
3. Electrical threats – Power issues such as spikes, noise, or outages  
4. Maintenance threats – Mishandling equipment, lack of spares, or poor labeling and cabling  

To protect against these, a physical security plan should be developed and enforced.  

<br>

___

<br>

# Network Attacks


### Types of Malware  
Malware is software designed to harm data, hosts, or networks. Common types include:

1. Viruses – Malicious code that inserts itself into other programs and spreads between computers.
2. Worms – Similar to viruses but don't need a host file or human help; they are standalone and self-replicating.
3. Trojan horses – Harmful programs that appear legitimate; they require user interaction to spread.

<br><br>

### Reconnaissance Attacks  
These attacks focus on discovering systems, services, or vulnerabilities.

- Threat actors use tools like `nslookup` or `whois` to gather information about IP address space.
- They may use `ping` to check which IP addresses are active and identify targets.

<br><br>

### Access Attacks  
Access attacks aim to gain unauthorized access to data or systems. Types include:

1. Password attacks – Use brute force, Trojan horses, or packet sniffers to steal credentials.
2. Trust exploitation – Abuse of trusted relationships between systems to gain access.
3. Port redirection – Use of a compromised host as a stepping stone to attack another trusted system.
4. Man-in-the-middle – Interception and possible modification of communication between two parties.

<br><br>

### Denial of Service (DoS) Attacks  
These attacks aim to disrupt services by overwhelming systems with traffic or resource demands.

- DoS attacks prevent authorized users from accessing services.
- They are easy to perform but hard to prevent completely.
- DDoS (Distributed Denial of Service) is a type of DoS attack from multiple sources.
  - A threat actor uses a network of infected devices (zombies) controlled through a botnet.
  - A command and control program directs the botnet to launch the attack.


<br>

___

<br>


# Network Attack Mitigations

Mitigation: Actions taken to reduce the risk, stop the attack, or limit the damage caused by the attack. "Network Attack Mitigations" means the methods and strategies used to protect a network from attacks or reduce the impact of those attacks.



### Defense-in-Depth Approach  
Also known as a layered security model, this approach uses multiple defense layers to protect networks and data. It includes:

- VPN (Virtual Private Network)  
- ASA Firewall (Adaptive Security Appliance)  
- IPS (Intrusion Prevention System)  
- ESA/WSA (Email/Web Security Appliances)  
- AAA Server (Authentication, Authorization, Accounting)

These tools work together to defend against TCP/IP-based threats.

<br><br>

### Keep Backups  
Regular backups are critical for protecting against data loss.

- Frequency – Perform full backups weekly or monthly, with partial (incremental) backups more often.  
- Storage – Store backups offsite and regularly test them.  
- Security – Protect backups with strong passwords.  
- Validation – Ensure backups can be restored properly.

<br><br>

### Upgrade, Update, and Patch  
Keeping systems up to date is one of the best defenses against malware.

- Regularly update operating systems and antivirus software.  
- Enable automatic updates where possible to reduce risk.  
- Patching systems helps prevent worm attacks and exploits.

<br><br>

### Authentication, Authorization, and Accounting (AAA)  
AAA is the core framework for managing user access.

- Authentication – Verifies who is accessing the network.  
- Authorization – Defines what the user is allowed to do.  
- Accounting – Logs user activity.

This is similar to using a credit card: who can use it, what they can spend, and tracking purchases.

<br><br>

### Firewalls and the DMZ  
Firewalls manage traffic between networks and prevent unauthorized access.

- Public-facing servers are often placed in a DMZ (Demilitarized Zone).  
- DMZs allow specific external access while isolating internal networks.

<br><br>

### Types of Firewalls  
Firewalls can use different methods to control access:

1. Packet filtering – Based on IP or MAC addresses.  
2. Application filtering – Based on application types and port numbers.  
3. URL filtering – Based on web addresses or keywords.  
4. Stateful Packet Inspection (SPI) – Allows only responses to internal requests; blocks unsolicited traffic and detects DoS attacks.

<br><br>

### Endpoint Security  
Endpoints (devices like laptops, phones, desktops) are frequent targets.

- Endpoint security involves enforcing policies like antivirus use and host intrusion prevention.  
- User training and behavior play a key role.  
- Advanced systems use Network Access Control (NAC) to ensure only compliant devices can connect.

<br>

___

<br>
