
# OSPF Routing Configuration – Cisco Packet Tracer

## Project Overview
Configured a multi-router network using OSPF (Open Shortest Path First) as the dynamic routing protocol in Cisco Packet Tracer.

The lab consists of 5 routers connected in a network topology, with two LAN networks and multiple point-to-point connections.

## Network Topology
- 5 Cisco routers (R1, R2, R3, R4, R5)
- 2 switches
- 3 PCs on the first LAN
- 1 server and 2 laptops on the second LAN

## IP Addressing
- LAN 1: 10.10.10.0/26
- LAN 2: 10.10.10.64/26
- Router-to-router links: /30 subnets
- Used private IPv4 addressing with VLSM.

## Technologies & Concepts Practiced
- OSPF Dynamic Routing
- Single-Area OSPF (Area 1000)
- OSPF Router ID
- OSPF Network Statements and Wildcard Masks
- OSPF Neighbor Adjacency
- OSPF Neighbor States (FULL)
- OSPF Cost Configuration
- Routing Table Verification
- DHCP Configuration
- IP Addressing and VLSM
- Connectivity Testing using ICMP

## Verification Commands
- show ip ospf neighbor
- show ip route
- show ip ospf database
- show ip interface brief

## Tools Used
Cisco Packet Tracer

## Learning Outcome
Practiced configuring OSPF across five routers, establishing neighbor adjacencies, exchanging routing information, and verifying dynamically learned routes between different networks.
