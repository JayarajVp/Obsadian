# INDEX
[[1 OSI model]]
[[2 TCP vs UDP]]
[[3 ICMP (ping, traceroute)]]
[[4 MTU & fragmentation]]
[[5 MAC vs IP vs Port]]
[[6 ARP & ARP cache]]
[[7 Physical NICs]]
[[8 Virtual NICs (veth, tap)]]
[[9 Link states (UP-DOWN-NO-CARRIER)]]
[[10 Multiple IPs on one NIC]]
[[11 Secondary IPs]]
[[12 Default route]]
[[13 Static routes]]
[[14 Metric & priority]]
[[15 Source-based routing (intro)]]
[[16. NetworkManager (nmcli, nmtui)]]
[[17 etc-resolv.conf]]
[[18 systemd-resolved]]
[[19 search domains]]
[[20 split DNS]]
[[21 traceroute]]
[[22 tcpdump]]
[[23 nmap basics]]
[[24 Path MTU discovery]]
[[25 End-to-end MTU issues]]
[[26 VM  to host MTU mismatch]]

----
### Level 1 – Foundations (Week 1–2)

> _You must think in packets, not commands_
- OSI model (but **Linux mapping**, not textbook)
    
- MAC vs IP vs Port (very important)
    
- TCP vs UDP (real traffic behavior)
    
- ICMP (ping, traceroute, PMTU)
    
- MTU & fragmentation
    
- ARP & ARP cache
### Level 2 – Linux Networking Internals (Week 3–4)

> _This is where juniors become engineers_

- Physical NICs vs Virtual NICs
    
- veth, tap, bridge (containers & VMs)
    
- Link states (UP / DOWN / NO-CARRIER)
    
- Multiple IPs on one NIC
    
- Secondary IPs
    
- Default route
    
- Static routes
    
- Metrics & priority
    
- Source-based routing (intro)
### Level 3 – Name Resolution & Routing Reality (Week 5)

> _“Network is fine” but app still broken? This is why._

- `/etc/resolv.conf`
    
- `systemd-resolved`
    
- search domains
    
- split DNS
    
- DNS failures in prod
### Level 4 – Debugging Like a Pro (Week 6+)

> _This is where senior respect comes from_

- `tcpdump` (deep, not basic)
    
- `traceroute` internals
    
- `nmap` basics (what ops actually uses)
    
- Path MTU discovery
    
- End-to-end MTU issues
    
- VM ↔ host MTU mismatch
    
- “Works on host, fails in VM/container” cases

