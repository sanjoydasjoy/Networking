# **Cisco Packet Tracer Basic Configuration Lab**




## Enter Router CLI and Basic Configuration

> The router always needs to be configured through **CLI**.

### Commands:

```bash
Router> enable
Router# configure terminal
Router(config)# hostname R1          # Rename router

# Configure interface connected to Switch
R1(config)# interface fastEthernet 1/0
R1(config-if)# ip address 172.10.5.126 255.255.255.128
R1(config-if)# no shutdown           # Activate the port
R1(config-if)# exit

# Configure interface connected to Server
R1(config)# interface fastEthernet 0/0
R1(config-if)# ip address 172.10.10.1 255.255.255.128
R1(config-if)# no shutdown
R1(config-if)# exit
```

**Check interfaces are up:**

```bash
R1# show ip interface brief
```

> You should see both FastEthernet interfaces showing **“up/up”** (green lights in Packet Tracer).

<br>

___

<br>



## Verify Connections (Switch ↔ Router ↔ Server)

* Check **switch lights** — should all be green.
* You can test by **sending a packet (PDU)** or using **ping**.

### Example Ping:

```bash
PC> ping 172.10.10.126
```

If replies are successful → network is configured correctly.

<br>

___

<br>




## Optional Troubleshooting Commands

If ping fails, check:

```bash
R1# show ip interface brief       # Verify interface status
R1# show running-config           # Review configuration
R1# ping 172.10.10.126            # Test directly from router
```

<br>

___

<br>
