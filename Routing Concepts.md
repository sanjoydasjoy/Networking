```
Routing Concepts/
├── Path Determination/
├── Packet Forwarding/
├── Basic Router Configuration/
├── IP Routing Table/
```

# Path Determination


When you send a message over the internet, it has to travel across many networks to reach the other person. Routers help move that data across the networks in the right direction.
<br>

This happens at the **network layer** (layer 3 in the OSI model). The network layer is responsible for finding the best path to send the data using IP addresses.  

It's responsible for figuring out *where* data should go and *how* to get it there. This process is called **path determination**.

<br><br>

### Router's Main Jobs  
When a router gets a packet:  
- It checks its **routing table** to figure out the best path.  
- Then, it sends the packet either:  
  - Directly to the final destination (if it's on the same network), or  
  - To the next router (next hop) that gets it closer to the destination.  

<br><br>

### Path Determination (Choosing the Best Route)  
Routers have a list of possible paths (routes).  
They use a method called **longest match** to pick the best one.  

This means:  
- Each route has a **prefix**, like 172.16.0.0/26.  
- The router compares the destination IP of the packet with these prefixes.  
- The route with the **most matching leftmost bits** (longest match) is chosen.

<br><br>

### Example (IPv4)  
Destination: 172.16.0.10  
Routing table has:  
- 172.16.0.0/12  
- 172.16.0.0/18  
- 172.16.0.0/26 ← this is chosen because it matches the most bits.

<br><br>

### Example (IPv6)  
Destination: 2001:db8:c000::99  
Routing table has:  
- 2001:db8:c000::/40 → match  
- 2001:db8:c000::/48 → better match (chosen)  
- 2001:db8:c000:5555::/64 → no match (too specific)

<br><br>

### How Routes Get Into the Routing Table  
1. Directly Connected Networks  
   - Added when a router interface is given an IP and is active.  

2. Remote Networks  
   - Static routes: manually set by an admin.  
   - Dynamic routes: learned automatically through routing protocols (like RIP, OSPF, EIGRP).  

3. Default Route (/0)  
   - Used when no specific route matches the destination.  
   - It's like saying: “If you don’t know where to send this, send it here.”  
   - Also called the **gateway of last resort**.

<br><br>

<br>

___

<br>


# Packet Forwarding

<br>


A **router** is like a **post office** for the internet. It gets a **letter (packet)** and has to figure out where to send it next.

<br>
<br>

### Part 1: **How the Router Knows Where to Send Things (Path Determination)**

The router keeps an address book called a **routing table**.  
It has three kinds of addresses:

1. **Local (Directly Connected)**  
   - These are neighbors — devices directly plugged into the router.
2. **Static Routes**  
   - Manually added by the network admin.
3. **Dynamic Routes**  
   - Learned from other routers using special “chat” (routing protocols).

And there’s one special one:

4. **Default Route**  
   - Like saying: “If you don’t know where to send it, just send it here.”
   - Used when no better match is found.

<br>
<br>

### Part 2: **How the Router Sends the Packet (Forwarding)**

Once the router knows where to send it, it has 3 options:

#### a) **Send Directly to the Device**  
- If the destination is nearby, send it straight there.
- Like handing a letter to someone in the same room.

#### b) **Send to Another Router (Next-Hop)**  
- If the destination is far, hand the letter to another post office.
- That router will continue the delivery.

#### c) **Drop the Packet**  
- If there’s no info in the address book, and no default route, throw the letter away.

<br>
<br>

### Part 3: **How Fast the Router Sends It (Forwarding Methods)**

The router has three ways to do this job:

1. **Process Switching** (Old way)  
   - Looks up the address every single time. Slow.

2. **Fast Switching** (Better)  
   - Remembers the first letter’s path and reuses it for the next ones.

3. **Cisco Express Forwarding (CEF)** (Best)  
   - Already has a super-fast cheat sheet ready before letters even arrive.

<br>
<br>


### Summary

- Router = post office for the internet  
- Routing table = address book  
- Picks best path = longest matching address  
- Sends it: either direct, to another router, or drops it  
- Uses fast methods to do it quickly (CEF is fastest)

<br>

___

<br>


# Basic Router Configuration


### Router Verification Commands

These commands help verify interface status, IP configuration, routing information, and network connectivity.

| Command | Purpose |
|-------------|-------------|
| show ip interface brief | Displays a quick overview of interface statuses and assigned IPv4 addresses. |
| show running-config interface [type number] | Shows the full configuration for a specific interface (e.g., `gigabitEthernet 0/0`). |
| show interfaces | Provides detailed statistics about an interface (errors, bandwidth, MTU, etc.). |
| show ip interface | Displays detailed IPv4 configuration settings per interface. |
| show ip route | Lists the current IPv4 routing table entries. |
| ping [destination IP] | Tests connectivity to another device to check network reachability. |


<br><br>

For IPv6:
Just replace `ip` with `ipv6` in any of the above commands:
- show ipv6 interface brief
- show ipv6 route
- ping [IPv6 address]

<br><br>

### Filtering Command Output

To narrow down large command outputs, Cisco IOS supports output filtering using the pipe symbol `|`.

#### Syntax:
```bash
show [command] | [filter-type] [keyword]
```

<br><br>

#### Filter Types:

| Filter Type | Description | Example |
|-----------------|------------------|-------------|
| section | Displays the entire section starting from the matched keyword. | show run | section interface |
| include | Shows only lines that contain the keyword. | show run | include ip address |
| exclude | Hides lines that contain the keyword. | show run | exclude shutdown |
| begin | Starts displaying output from the line that matches the keyword onward. | show run | begin line vty |

#### Notes:
- Filters work with any `show` command.
- Ideal for quickly locating configuration blocks, interface IPs, passwords, or other keywords.

<br>

___

<br>



### IP Routing Table 

An **IP routing table** lists all the known networks (prefixes) and specifies how to reach them. Each route has a source, which could be directly connected, static, or dynamically learned.

<br>

#### Route Sources and Their Codes:
- **L**: Local address (assigned to a router interface).
- **C**: Directly connected network.
- **S**: Static route (manually configured).
- **O**: OSPF learned route.
- **\***: Candidate for default route.

<br><br>

### Routing Table Principles

There are three principles for routing tables:
1. **Autonomous Decision-Making**: Each router makes routing decisions based on its own table, unaware of other routers’ tables.
2. **Independent Routing Tables**: A router’s routing table doesn’t necessarily match another router's, even if they share networks.
3. **Return Path Not Guaranteed**: A router can forward packets to a network, but it may not have a route back to the source.

<br><br>

### Routing Table Entries

Each entry contains:
- **Route source**: How the route was learned (e.g., `C`, `S`, `O`).
- **Destination network**: The network's address and prefix.
- **Administrative Distance (AD)**: The trustworthiness of the route (lower AD is more trustworthy).
- **Metric**: The "cost" of reaching the network (lower is better).
- **Next-hop**: The next router to forward packets to.
- **Timestamp**: The time elapsed since the route was learned.
- **Exit interface**: The outgoing interface for forwarding packets.

<br><br>

### Directly Connected Networks

Routers add a route for any **directly connected networks** when an interface has an IP address configured. These routes have the status code **C** (connected), and the local address is denoted by **L** in the routing table.

- **IPv4 local routes**: `/32` prefix length.
- **IPv6 local routes**: `/128` prefix length.

<br><br>

### Static Routes

Static routes are manually configured routes. They are not updated automatically and must be reconfigured if the network topology changes. Common uses for static routes:
1. **Small, stable networks**.
2. **Default routes** (routes to networks not otherwise covered).
3. **Routing to/from stub networks** (networks with a single exit route).

<br><br>

### Dynamic Routing Protocols

Dynamic routing protocols, like **OSPF**, allow routers to automatically share information about network reachability. These protocols manage network discovery and routing table maintenance.

- **OSPF**: An example of a dynamic routing protocol, denoted by **O** in the routing table.

<br><br>

### Default Route

A **default route** forwards traffic to a next-hop router when no specific match is found for a destination IP address. This is indicated in IPv4 as `0.0.0.0/0` and in IPv6 as `::/0`.

<br><br>

### Routing Table Structure

#### IPv4 Routing Table:
The IPv4 routing table still follows a **classful** structure. Entries are indented for **child routes** (subnets) and **parent routes** (classful networks).

#### IPv6 Routing Table:
IPv6 doesn’t use classful addressing, so its routing table is simpler, with each route entry formatted the same way.

<br><br>

### Administrative Distance (AD)

**Administrative Distance (AD)** determines the trustworthiness of a route. When multiple routing protocols learn about the same network, the router uses the AD to decide which route to install. Lower AD values indicate more trusted sources.

| **Route Source** | **Administrative Distance** |
|------------------|-----------------------------|
| Directly connected | 0 |
| Static route | 1 |
| EIGRP summary route | 5 |
| External BGP | 20 |
| Internal EIGRP | 90 |
| OSPF | 110 |
| RIP | 120 |
| External EIGRP | 170 |
| Internal BGP | 200 |

This table shows the relative trustworthiness of different route sources.



<br>

___

<br>
