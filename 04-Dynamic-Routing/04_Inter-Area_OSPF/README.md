# Inter-Area OSPF Routing Lab

## Project Overview
This project demonstrates the configuration and implementation of Inter-Area OSPF (Open Shortest Path First) routing in a multi-area network environment using Cisco Packet Tracer.

The main objective was to establish communication between different OSPF areas through an Area Border Router (ABR).

## Technologies & Concepts Practiced
- OSPF Dynamic Routing
- OSPF Area 0 (Backbone Area)
- Non-Backbone OSPF Area
- Area Border Router (ABR)
- OSPF Neighbor Adjacency
- Router ID Configuration
- Network Advertisement
- Routing Table Verification
- End-to-End Connectivity Testing

## Lab Objectives
- Configure OSPF on multiple routers.
- Divide the network into different OSPF areas.
- Establish OSPF neighbor relationships.
- Configure an ABR to connect Area 0 with another OSPF area.
- Exchange routing information between different areas.
- Verify routes using routing table commands.
- Test connectivity between different networks.

## Verification Commands

```bash
show ip ospf neighbor
show ip ospf interface brief
show ip ospf database
show ip route ospf
show ip protocols
ping
traceroute
```

## Tools Used
- Cisco Packet Tracer

## Project Files
- `Configurations/` – Individual router configurations.
- `Screenshots/` – Network topology and verification screenshots.
- `Inter-Area-OSPF-Demo.mp4` – Lab demonstration video.

## Learning Outcome
Gained practical experience in configuring multi-area OSPF routing, understanding the role of an ABR, establishing neighbor relationships, and exchanging routing information between different OSPF areas.
