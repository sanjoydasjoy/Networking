
### What is ICMP?

ICMP (Internet Control Message Protocol) is a network protocol used by devices like routers and computers to send error messages and information about what’s happening during the delivery of data.

It doesn’t carry user data like emails or web pages. Instead, it helps the network itself by reporting problems such as:

- A device can’t be reached  
- A route doesn’t exist  
- Data took too long to arrive  
- A service or port is not available  

For example, if you try to visit a website and the server is down, ICMP might send back a message saying "host unreachable." Or if data takes too many hops and doesn’t get to the destination, ICMP sends back a "time exceeded" message.

There are two main types:  
- ICMPv4 for IPv4 networks  
- ICMPv6 for IPv6 networks (with extra features like address detection and router discovery)

<br><br>

### Common ICMP Messages

1. Host Reachability  
- Used to check if a device is working or online.  
- It sends a message (called Echo Request), and if the device replies (Echo Reply), it's working.

2. Destination Unreachable  
- This message means the data couldn’t reach its destination.  
- Some common reasons in ICMPv4:  
  - Code 0: Network is unreachable  
  - Code 1: Host is unreachable  
  - Code 3: Port is unreachable  
- In ICMPv6, there are similar reasons:  
  - Code 1: Blocked by firewall  
  - Code 2: Too far to reach  
  - Code 4: Port is unreachable

3. Time Exceeded  
- If data takes too long to travel through the network, it "expires."  
- IPv4 uses a timer called TTL (Time to Live).  
- IPv6 uses Hop Limit (similar to TTL).  
- This is used by a tool called traceroute to find the path data takes.

<br><br>

### ICMPv6 Extra Features (Neighbor Discovery)

1. Router Solicitation (RS)  
- A device says: "Hey, is there a router? I need an IPv6 address."

2. Router Advertisement (RA)  
- The router replies: "Yes, I’m here. Use this address and I’ll be your gateway."

3. Neighbor Solicitation (NS)  
- A device sends this to:  
  a) Check if an address is already used (to avoid using the same one).  
  b) Ask: "What’s your MAC address?"

4. Neighbor Advertisement (NA)  
- This is the reply to NS. It says:  
  - "Yes, someone is using that address." (for checking)  
  - "Here is my MAC address." (for communication)

<br>

___

<br>

# Ping and Traceroute Tests



### What is Ping?

Ping is a command used to test if one device can talk to another device over a network.

When you run a ping command, your device sends a special message called an ICMP Echo Request to another device. If the other device is working and reachable, it will send back an ICMP Echo Reply.

Ping tells you:
- Whether the destination device is reachable or not
- How long it took for the message to go and come back (called round-trip time)
- How many messages were sent and how many were received

If a reply does not come back, ping shows a timeout message. This usually means the device is not reachable or is blocking ping messages.

Sometimes, the first ping fails because your device needs to find the MAC address of the destination using ARP (for IPv4) or Neighbor Discovery (for IPv6). Once that step is done, the next ping usually works.

<br>

### Ping the Loopback Address

Every computer has a loopback address. This is a special IP address that points back to the device itself.

- The loopback address is 127.0.0.1 for IPv4
- It is ::1 for IPv6

When you ping the loopback address, you are testing if your device's IP protocol is working correctly. If the ping is successful, that means the IP stack is installed and working. If it fails, it usually means something is wrong with the TCP/IP settings on your computer.

<br>

### Ping the Default Gateway

The default gateway is usually your home router or the device that connects your local network to other networks like the internet.

You can use ping to check if your device can talk to the default gateway. If the ping is successful:
- Your computer's network interface is working
- The gateway device (usually the router) is online and reachable

If the gateway doesn't respond, try pinging another device on your local network to see if the issue is just with the gateway.

<br>

### Ping a Remote Host

You can also ping a device that is not on your local network, like a web server.

If the ping is successful:
- Your device is able to talk to the router
- The router is able to send data to the internet
- The remote server is reachable and replying

However, sometimes ping to a remote host will fail even if everything is working fine. This is because some networks block ICMP messages for security reasons. In that case, a failed ping does not always mean a broken connection.

<br><br><br>

# What is Traceroute?

**Traceroute** is a tool used to discover(map) the path (routers/hops) that packets take to reach a destination on a network.

It works by sending packets with small values for the TTL (Time To Live). TTL is a number that limits how many devices (called hops) a packet can pass through. Each router that receives the packet decreases the TTL by 1. If TTL becomes 0, the router drops the packet and sends back an ICMP Time Exceeded message.




<br><br>

### How does Traceroute work?
It uses a trick with the **TTL (Time To Live)** field in IP packets:

1. Traceroute sends a test packet with **TTL = 1**  
   → First router gets it, decreases TTL to 0, drops it, and replies with an **ICMP "Time Exceeded"** message.  
   → Traceroute notes this router.

2. Then it sends another test packet with **TTL = 2**  
   → It reaches the second router, which drops it and replies.

3. This continues with TTL = 3, 4, 5… until it reaches the final destination.  
   → The destination replies with an ICMP "Port Unreachable" or other response.

Each step tells Traceroute **which router** was next in the path and **how long** it took to get there.

<br><br>

### What happens to those earlier packets (TTL = 1, 2, etc.)?
They are **dropped intentionally** by the routers as part of the test.  
Traceroute doesn’t expect them to arrive — it’s using their **failures** to learn the path.

They are like test runners who stop after 1km, 2km, 3km — to see how far they get before being stopped.

<br><br>

### So when are the **real data packets** sent?
- **After** traceroute is done (or separately), your actual data packets are sent.
- These packets **do not use low TTL values** — they are set high enough (like 64 or 128) to reach the destination directly.
- Routers along the way **know where to forward the packets**, using their **routing tables**.

<br><br>

### Real-life analogy:
You want to visit a friend in another city.

- **Traceroute** is like asking:  
  “Hey, which highways and toll booths will I pass through if I go to that city?”

- You get a list:  
  “You’ll pass through Route A, Toll Gate 1, Toll Gate 2…”

- **Then** you actually get in your car and **drive the full route** (that’s your **real packet**).

The **actual drive** doesn’t involve asking anyone again — you just follow the signs.

<br>

So in short:
- Traceroute = **testing and mapping** the route  
- Real data = **uses the path** directly, as defined by routers

<br><br>

Traceroute shows:
- The IP address or hostname of each router in the path
- How long it took to reach each one (round-trip time)
- A star (*) if a router does not reply

This helps in finding where a network problem is happening. If you see stars or long delays at a certain hop, the problem might be there.


<br>

___

<br>
