
# IPv6 OSPFv3 Dynamic Routing Lab

## Project Overview

This project demonstrates the configuration and implementation of IPv6 OSPFv3 dynamic routing in Cisco Packet Tracer.

The network consists of 9 routers, 2 switches, and 4 end devices distributed across two LAN networks. OSPFv3 is configured to establish dynamic routing between routers and enable end-to-end IPv6 communication.

## Network Topology

- 9 Routers (R1–R9)
- 2 Switches
- 4 Laptops
- 2 LAN Networks
- 9 Router-to-Router Connections
- IPv6 Addressing
- OSPFv3 Process ID: 1
- OSPF Area: 10 (as verified on R1)

## IPv6 Addressing Scheme

| Network | Description |
|---|---|
| FD00::/64 | Left LAN |
| 2001::/64 | R1 – R2 |
| 2002::/64 | R2 – R8 |
| 2003::/64 | R8 – R7 |
| 2004::/64 | R7 – R6 |
| 2005::/64 | R2 – R3 |
| 2006::/64 | R3 – R4 |
| 2007::/64 | R4 – R5 |
| 2008::/64 | R5 – R6 |
| 2009::/64 | R6 – R9 |
| FD01::/64 | Right LAN |

All IPv6 networks use a /64 prefix length.

## Technologies and Concepts Used

- IPv6 Addressing
- OSPFv3 Dynamic Routing
- OSPF Neighbor Adjacency
- Router-to-Router IPv6 Connectivity
- IPv6 Routing Table Verification
- ICMPv6
- Ping Testing
- Traceroute

## Configuration Highlights

1. Configured IPv6 addresses on router interfaces.
2. Enabled IPv6 unicast routing.
3. Configured OSPFv3 using process ID 1.
4. Enabled OSPFv3 on router interfaces.
5. Established OSPF neighbor adjacencies.
6. Verified dynamically learned IPv6 routes.
7. Tested end-to-end communication between LAN devices.

## Verification and Testing

The following commands were used for verification:

### Router Commands

```bash
show ipv6 interface brief
show ipv6 route
show ipv6 ospf neighbor
show ipv6 protocols
```

### End Device Commands

```bash
ping FD01::3
tracert FD01::2
```

## Results

- OSPFv3 successfully established routing between network devices.
- Remote IPv6 networks were dynamically learned.
- Successful ICMPv6 communication was verified between end devices.
- Traceroute confirmed the packet forwarding path across multiple routers.

## Tools Used

- Cisco Packet Tracer
- Cisco IOS CLI

## Project Objective

The objective of this lab was to gain practical experience with IPv6 dynamic routing, OSPFv3 configuration, routing table analysis, and end-to-end network connectivity.

