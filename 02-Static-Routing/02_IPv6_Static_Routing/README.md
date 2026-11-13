# IPv6 Static Routing – Cisco Packet Tracer

## Project Overview
This lab demonstrates the configuration of IPv6 static routing between multiple networks using Cisco routers.

I created a three-router topology connecting three different LAN networks. Static routes were configured manually on each router to enable communication between remote IPv6 networks.

## Network Topology
- 3 Routers (R1, R2, R3)
- 3 Switches
- 9 PCs
- 3 LAN Networks
- 2 Router-to-Router Connections

## Technologies & Concepts Practiced
- IPv6 Addressing
- IPv6 Static Routing
- IPv6 Prefix Length (/64)
- Global Unicast Addressing
- Unique Local Addressing (ULA)
- Next-Hop IPv6 Address
- IPv6 Routing Table Verification

## IPv6 Addressing Scheme

| Network | IPv6 Prefix |
|---|---|
| R1 LAN | FD00::/64 |
| R2 LAN | FD01::/64 |
| R3 LAN | FD02::/64 |
| R1 – R2 | 2001::/64 |
| R2 – R3 | 2002::/64 |

## Static Routing Configuration

**R1:**
```bash
ipv6 route FD01::/64 2001::2
ipv6 route FD02::/64 2001::2
```

**R2:**
```bash
ipv6 route FD00::/64 2001::1
ipv6 route FD02::/64 2002::2
```

**R3:**
```bash
ipv6 route FD01::/64 2002::1
ipv6 route FD00::/64 2002::1
```

## Verification Commands

```bash
show ipv6 route
show ipv6 interface brief
ping <destination-ipv6-address>
```

## Learning Outcome
Gained practical experience configuring IPv6 static routes using next-hop IPv6 addresses, understanding routing tables, and connecting multiple IPv6 networks through routers.

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI
