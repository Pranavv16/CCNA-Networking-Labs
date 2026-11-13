# IPv6 Interface Configuration – Cisco Packet Tracer

## Project Overview
This lab focuses on configuring IPv6 addresses on router interfaces using Cisco IOS commands.

I created a network topology consisting of:
- 3 Routers (R1, R2, R3)
- 3 Switches
- 9 PCs
- 2 Router-to-Router connections
- 3 LAN networks

## Technologies & Concepts Practiced
- IPv6 Addressing
- IPv6 Interface Configuration
- IPv6 Prefix Length (/64)
- Global Unicast Addressing
- Unique Local Addressing (ULA)
- Enabling IPv6 Routing

## IPv6 Addressing Scheme

| Network | IPv6 Prefix |
|---|---|
| R1 LAN | FD00::/64 |
| R2 LAN | FD01::/64 |
| R3 LAN | FD02::/64 |
| R1 – R2 | 2001::/64 |
| R2 – R3 | 2002::/64 |

## Configuration Commands

```bash
# Enable IPv6 routing
ipv6 unicast-routing

# Configure IPv6 on router interfaces
interface fastethernet 0/0
ipv6 address 2001::1/64
no shutdown

interface fastethernet 0/1
ipv6 address FD00::1/64
no shutdown
```

*Note: Interface addresses differ on each router. Refer to the Router-Configurations folder for individual configurations.*

## Learning Outcome
Practiced assigning IPv6 addresses to router interfaces, working with /64 prefixes, and understanding IPv6 addressing across multiple LANs and router-to-router connections.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI
