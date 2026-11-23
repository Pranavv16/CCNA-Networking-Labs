# IPv6 Inter-Area OSPFv3 Routing – Cisco Packet Tracer

## Project Overview

This project demonstrates the implementation of IPv6 Inter-Area OSPFv3 routing using Cisco Packet Tracer.

I designed a multi-area network consisting of 9 routers, multiple switches, and end devices. The network is divided into three OSPF areas: Area 0 (Backbone Area), Area 200, and Area 400.

The main objective was to establish communication between different IPv6 networks using OSPFv3 and understand how Area Border Routers (ABRs) facilitate routing between multiple OSPF areas.

## Network Topology

- 9 Routers
- 4 Switches
- 8 End Devices
- 3 OSPF Areas
- IPv6 Addressing
- OSPFv3 Dynamic Routing

## OSPF Area Distribution

| Area | Routers | Description |
|---|---|---|
| Area 0 | R3, R6, R7 | Backbone Area |
| Area 200 | R1, R2, R3, R4, R5 | Left-side network |
| Area 400 | R7, R8, R9 | Right-side network |

## Area Border Routers (ABRs)

- R3: Connects Area 200 with Area 0.
- R7: Connects Area 0 with Area 400.

R6 operates as a backbone router within Area 0.

## IPv6 Addressing Plan

### Area 200

| Network | Purpose |
|---|---|
| 2001::/64 | R1 – R2 |
| 2002::/64 | R2 – R3 |
| 2003::/64 | R3 – R4 |
| 2004::/64 | R4 – R5 |
| 2005::/64 | R5 – R1 |
| FD00::/64 | R1 LAN |
| FD01::/64 | R3 LAN |

### Area 0

| Network | Purpose |
|---|---|
| 3001::/64 | R3 – R6 |
| 3002::/64 | R6 – R7 |

### Area 400

| Network | Purpose |
|---|---|
| 2011::/64 | R7 – R8 |
| 2012::/64 | R8 – R9 |
| FD02::/64 | R7 LAN |
| FD03::/64 | R9 LAN |

## Technologies and Concepts Practiced

- IPv6 Addressing
- OSPFv3 Configuration
- Inter-Area Routing
- OSPF Backbone Area (Area 0)
- Area Border Router (ABR)
- Router ID Configuration using Loopback Interfaces
- OSPF Neighbor Adjacency
- IPv6 Dynamic Routing
- End-to-End Connectivity Testing

## Configuration Highlights

1. Enabled IPv6 routing using `ipv6 unicast-routing`.
2. Configured unique OSPF router IDs using loopback interfaces.
3. Created OSPFv3 routing processes on all routers.
4. Assigned interfaces to their respective OSPF areas.
5. Established Area 0 as the backbone area.
6. Configured R3 and R7 as Area Border Routers.
7. Verified OSPFv3 neighbor relationships.
8. Tested IPv6 connectivity between different network segments.

## Verification Commands

```cisco
show ipv6 interface brief
show ipv6 ospf neighbor
show ipv6 ospf database
show ipv6 route
show running-config
```

## Learning Outcome

Through this lab, I gained practical experience in configuring IPv6 Inter-Area OSPFv3 routing, understanding the role of the backbone area, configuring ABRs, and establishing communication between multiple IPv6 networks.

## Simulation Software

Cisco Packet Tracer 9.0.1

## Project Files

- Packet Tracer topology file (.pkt)
- Individual router configuration commands (.txt)
- Network topology, configuration screenshots and connectivity video

---

**Author:** Pranav Mahangare

**Field:** Networking | CCNA 200-301 Practical Labs
