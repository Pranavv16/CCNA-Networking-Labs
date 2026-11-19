# Inter-Area OSPF Routing Lab

## Project Overview

This project demonstrates the configuration and implementation of Inter-Area OSPF (Open Shortest Path First) routing using Cisco Packet Tracer.

The topology consists of 5 routers (R1, R2, ABR-R3, R4, and R5), multiple LAN networks, and three OSPF areas: Area 0, Area 100, and Area 200.

The main objective was to establish communication between different OSPF areas and understand how routing information is exchanged across a multi-area network.

## Network Topology

The network is divided into three OSPF areas:

- **Area 100:** Connected to R1 and R2.
- **Area 0:** Backbone area connecting R2, R3, and R4.
- **Area 200:** Connected to R4 and R5.

## IP Addressing

| Router | Interface | IP Address | Network |
|---|---|---|---|
| R1 | Fa0/0 | 170.170.0.1/30 | 170.170.0.0/30 |
| R1 | Fa0/1 | 192.168.1.1/24 | 192.168.1.0/24 |
| R2 | Fa0/0 | 170.170.0.2/30 | 170.170.0.0/30 |
| R2 | Fa0/1 | 180.180.180.1/30 | 180.180.180.0/30 |
| R2 | Fa1/0 | 172.20.0.1/24 | 172.20.0.0/24 |
| R3 | Fa0/0 | 180.180.180.2/30 | 180.180.180.0/30 |
| R3 | Fa0/1 | 200.50.50.1/30 | 200.50.50.0/30 |
| R4 | Fa0/0 | 200.50.50.2/30 | 200.50.50.0/30 |
| R4 | Fa0/1 | 150.160.100.1/30 | 150.160.100.0/30 |
| R4 | Fa1/0 | 10.10.10.1/26 | 10.10.10.0/26 |
| R5 | Fa0/0 | 150.160.100.2/30 | 150.160.100.0/30 |
| R5 | Fa0/1 | 172.16.0.1/28 | 172.16.0.0/28 |

## Technologies & Concepts Practiced

- OSPF Dynamic Routing
- Multi-Area OSPF Configuration
- OSPF Backbone Area (Area 0)
- Non-Backbone Areas (Area 100 and Area 200)
- OSPF Neighbor Adjacency
- Router ID and OSPF Process
- Network Advertisement
- Wildcard Masks
- Inter-Area Route Exchange
- Routing Table Verification

## Lab Objectives

- Configure OSPF on multiple routers.
- Establish communication between different OSPF areas.
- Configure OSPF network statements with appropriate wildcard masks.
- Establish OSPF neighbor relationships.
- Advertise LAN and point-to-point networks.
- Verify inter-area routes through routing tables.
- Test end-to-end network connectivity.

## Verification Commands

The following commands were used to verify OSPF configuration and routing information:

```bash
show ip interface brief
show ip ospf neighbor
show ip ospf interface brief
show ip ospf database
show ip route
show ip route ospf
show ip protocols
```

Connectivity testing:

```bash
ping <destination-ip>
traceroute <destination-ip>
```

## Routing Table Verification

Verified routing information using the `show ip route` command.

- **O:** OSPF intra-area route.
- **O IA:** OSPF inter-area route.

Successfully observed OSPF inter-area routes (O IA) in the routing tables, confirming the exchange of routing information between different areas.

## Tools Used

- Cisco Packet Tracer

## Project Files

- `README.md` – Project documentation.
- `Configuration-Commands.txt` – Individual router configuration commands.
- `Screenshots/` – Network topology, router configurations, and routing table outputs.

## Learning Outcome

Gained practical experience in configuring multi-area OSPF routing, understanding OSPF neighbor relationships, working with different OSPF areas, and verifying inter-area route advertisements through routing tables.
