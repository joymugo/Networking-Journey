# Networking-Journey
A cup off coffee at hand lets get to work!

# My Networking Journey

## Day 1 — Basic Network Connectivity (Packet Tracer)

### Topology
- 1 Router (Cisco 2911)
- 1 Switch (Cisco 2960)
- 3 PCs

### IP Addressing Scheme
| Device | IP Address     | Subnet Mask     | Gateway      |
|--------|----------------|-----------------|--------------|
| Router | 192.168.1.1    | 255.255.255.0   | -            |
| PC0    | 192.168.1.10   | 255.255.255.0   | 192.168.1.1  |
| PC1    | 192.168.1.11   | 255.255.255.0   | 192.168.1.1  |
| PC2    | 192.168.1.12   | 255.255.255.0   | 192.168.1.1  |

### What I Did
- Connected 3 PCs to a switch and switch to a router
- Configured IP addresses manually on all PCs
- Enabled the router interface using `no shutdown`
- Verified connectivity using ping

### Issue I Hit
- Router interface GigabitEthernet0/0 was red after cabling
- Fixed it by running `no shutdown` on the interface

### What I Learned
- Router interfaces are shutdown by default and must be manually enabled
- All devices need an IP, subnet mask and default gateway to communicate
- Ping with 0% packet loss confirms successful connectivity

### Commands Used
- `enable` — enters privileged mode
- `configure terminal` — enters config mode
- `interface GigabitEthernet0/0` — selects the interface
- `ip address 192.168.1.1 255.255.255.0` — assigns IP
- `no shutdown` — turns the interface on
- `show ip interface brief` — verifies interface status
