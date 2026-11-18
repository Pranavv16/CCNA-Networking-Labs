# EIGRP Dynamic Routing Configuration Using 5 Routers

## Project Overview
This project demonstrates the configuration and implementation of Enhanced Interior Gateway Routing Protocol (EIGRP) in a multi-router network using Cisco Packet Tracer.

The network consists of 5 routers connected through multiple point-to-point links, with two LAN networks connected to the routing infrastructure.

## Network Topology
- 5 Cisco Routers (R1, R2, R3, R4, R5)
- 2 Switches
- 6 End Devices (PCs)
- EIGRP Autonomous System Number: 100

## Technologies and Concepts Practiced
- EIGRP Dynamic Routing
- EIGRP Neighbor Adjacency
- Autonomous System (AS) Configuration
- IPv4 Addressing
- VLSM Subnetting
- /26 Subnets for LAN Networks
- /30 Subnets for Point-to-Point Router Links
- Routing Table Verification
- End-to-End Connectivity Testing

## Network Addressing
- LAN 1: 172.16.1.0/26
- LAN 2: 172.16.1.64/26
- Router-to-Router Links: 172.16.1.128/30, 172.16.1.132/30, 172.16.1.136/30, 172.16.1.140/30, 172.16.1.144/30

## Verification Commands
```bash
show ip eigrp neighbors
show ip route
show ip protocols
ping <destination-ip>
```

## Connectivity Testing
Successfully verified connectivity between end devices and remote networks using ICMP ping commands.

The routing tables confirmed that remote networks were learned dynamically through EIGRP.

## Files Included
- Cisco Packet Tracer project file (.pkt)
- Network topology screenshot
- Router routing table screenshots
- EIGRP neighbor verification
- End-to-end ping testing screenshot
- EIGRP configuration commands

## Learning Outcome
Through this practical lab, I gained hands-on experience configuring EIGRP, establishing neighbor relationships, exchanging routing information, and verifying connectivity across multiple networks.

**Tool Used:** Cisco Packet Tracer
