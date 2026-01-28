### Wrong way (textbook)
> “OSI has 7 layers: Physical, Data Link…”

### Correct way to think 

| OSI Layer      | Linux Reality      |
| -------------- | ------------------ |
| L1 – Physical  | Cable, NIC, driver |
| L2 – Data Link | MAC, ARP, bridge   |
| L3 – Network   | IP, routing table  |
| L4 – Transport | TCP/UDP ports      |
| L5–7           | App protocols      |
Linux doesn’t care about “presentation/session” layers.
### Key insight 
**Each layer can fail independently**
Example:

- NIC is UP (L1 OK)
- ARP fails (L2 broken)
- Route missing (L3 broken)
- Firewall blocks port (L4 broken)
Ping works 
Application fails 
This is **normal** in real systems.
### Commands mapped to OSI layers
#### Physical / Link

 
`ethtool eth0` 

#### L2 (ARP)

`ip neigh arp -n`
`ip link`

#### L3 (IP & routing)

`ip addr ip route`

#### L4 (TCP/UDP)

`ss -lntup`
### Real-world failure example

> “Server is reachable by ping, but SSH fails”
**Layer analysis**:
- L1: OK
- L2: OK
- L3: OK
- L4: TCP port 22 blocked 
### Interview trap (important)

**Question:**

> Ping works but application doesn’t. What could be wrong?

**Bad answer:**

> Firewall maybe

**Good answer:**

> ICMP uses a different protocol than TCP/UDP, so L3 connectivity exists but L4 may be blocked or misrouted.

## Task
On your Linux system, run:

`ip link 
`ip addr
`ip route
`ip neigh 
`ss -lntup`

Just **observe**, don’t memorize.

`ip link`
###### Output
`1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000 
`link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
`2: ens5: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP mode DEFAULT group default qlen 1000 
`link/ether 16:ff:c7:3f:74:d1 brd ff:ff:ff:ff:ff:ff altname enp0s5`
#### Explanation 
##### first line
Loopback interface (`lo`)
`1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
##### What this means
`1`: Interface index (internal kernel number)
`lo` : Interface name → **loopback**
Flags: `<LOOPBACK,UP,LOWER_UP>`
- **LOOPBACK** → Special virtual interface for local communication
- **UP** → Enabled by admin
- **LOWER_UP** → Kernel considers it operational
`mtu 65536` (**Maximum Transmission Unit**)
- Very large MTU 
- Loopback never hits physical hardware, so no fragmentation issues
`qdisc noqueue`
- No packet queueing
- Loopback traffic is delivered immediately
`state UNKNOWN`
- Loopback doesn’t have a physical carrier
- `UP/DOWN` doesn’t make sense here
##### Second line
`link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00`
- **link/loopback** → Interface type
- MAC address is all zeros (not real hardware)
- Broadcast also zeros (not used)
**Purpose of `lo`:**
- `127.0.0.1` communication
- Local services (databases, web servers, IPC)
- Never leaves the machine
##### Ethernet interface (`eth0`)
`2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 9001 qdisc mq state UP mode DEFAULT group default qlen 1000
##### `eth0`
Primary Ethernet interface
##### Flags: `<BROADCAST,MULTICAST,UP,LOWER_UP>`

- **BROADCAST** → Can send broadcast frames
- **MULTICAST** → Supports multicast (important for routing, discovery)
- **UP** → Enabled
    
- **LOWER_UP** → Physical link detected (cable / virtual link OK)

