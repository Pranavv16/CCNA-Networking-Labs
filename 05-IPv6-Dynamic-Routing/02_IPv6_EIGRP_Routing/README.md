# IPv6 EIGRP Dynamic Routing Lab

## Project Overview
This project demonstrates the configuration and implementation of IPv6 EIGRP (Enhanced Interior Gateway Routing Protocol) using Cisco Packet Tracer.

The lab consists of 7 routers connected through multiple network segments, with IPv6 addressing configured on router interfaces. EIGRP is configured to establish neighbor relationships and exchange IPv6 routing information dynamically.

## Network Topology
- 7 Cisco Routers (R1–R7)
- 2 Switches
- 6 End Devices (PCs/Laptops)
- IPv6 addressing
- EIGRP Autonomous System: 500

## IPv6 Addressing Scheme

The topology uses separate IPv6 /64 prefixes for each router-to-router connection and LAN segment.

### Router-to-Router Networks

| Connection | Router Interfaces | IPv6 Network |
|---|---|---|
| R1 ↔ R2 | R1 Fa0/1 – R2 Fa0/0 | 2001::/64 |
| R2 ↔ R3 | R2 Fa0/1 – R3 Fa0/0 | 2002::/64 |
| R3 ↔ R4 | R3 Fa0/1 – R4 Fa0/0 | 2003::/64 |
| R4 ↔ R5 | R4 Fa0/1 – R5 Fa0/0 | 2004::/64 |
| R5 ↔ R6 | R5 Fa0/1 – R6 Fa0/0 | 2005::/64 |
| R2 ↔ R6 | R2 Fa1/0 – R6 Fa0/1 | 2006::/64 |
| R4 ↔ R7 | R4 Fa1/0 – R7 Fa0/1 | 2007::/64 |

### LAN Networks

| LAN | Connected Router | IPv6 Network |
|---|---|---|
| LAN 1 | R1 | FD00::/64 |
| LAN 2 | R7 | FD01::/64 |

Each router-to-router link has its own IPv6 network, with individual IPv6 addresses assigned to both connected router interfaces.
The LAN prefixes are used for end-device connectivity through R1 and R7.

## Technologies and Concepts Practiced
- IPv6 Address Configuration
- IPv6 EIGRP Routing
- EIGRP Autonomous System Configuration
- EIGRP Router ID Configuration
- IPv6 EIGRP Interface Activation
- EIGRP Neighbor Adjacency
- IPv6 Routing Table Verification
- EIGRP Topology Table Verification
- End-to-End IPv6 Connectivity Testing
- Traceroute Verification

## EIGRP Configuration

EIGRP was configured using Autonomous System number 500.

Each router was assigned a unique EIGRP Router ID.

The following commands were used as part of the configuration:

```cisco
ipv6 unicast-routing

ipv6 router eigrp 500
 eigrp router-id 1.1.1.1
 no shutdown

interface fastethernet 0/0
 ipv6 eigrp 500

interface fastethernet 0/1
 ipv6 eigrp 500
```

Note: The Router ID must be unique on each router. The example above shows R1; other routers use their respective Router IDs.

## Verification Commands

```cisco
show ipv6 interface brief
show ipv6 eigrp neighbors
show ipv6 eigrp topology
show ipv6 route
```

## Connectivity Testing

Connectivity was verified using:

```text
ping fd00::2
ping fd01::4
tracert fd01::3
```

Successful ping responses confirmed IPv6 connectivity between the end devices.

Traceroute was used to observe the path taken by IPv6 packets across the network.

## Project Outcome

Successfully configured IPv6 EIGRP across a 7-router topology and verified dynamic IPv6 route learning, EIGRP neighbor adjacency, routing information, and end-to-end connectivity.

## Tools Used
- Cisco Packet Tracer

## Project Files
- `ipv6-eigrp-lab.pkt` – Packet Tracer project file
- `Configuration-Commands.txt` – Router configuration commands
- `Screenshots/` – Configuration and verification evidence
