# RIP Dynamic Routing Using RIPv2

## Lab Overview
This project demonstrates the configuration and implementation of RIP (Routing Information Protocol) using RIPv2 in Cisco Packet Tracer.

The network consists of five routers connected through point-to-point links and two LAN networks. RIPv2 is configured on all routers to enable dynamic route exchange and communication between different networks.

## Technologies & Concepts Practiced
- RIP Dynamic Routing
- RIPv2 Configuration
- IPv4 Addressing
- VLSM and Subnetting
- /30 Subnetting for Point-to-Point Connections
- /26 Subnetting for LAN Networks
- Routing Table Verification
- End-to-End Connectivity Testing

## Network Topology
The topology includes:
- 5 Routers (R1, R2, R3, R4, R5)
- 2 Switches
- 6 End Devices
- 2 LAN Networks
- 5 Point-to-Point Router Connections

## IP Addressing Scheme

| Network | Subnet |
|---|---|
| LAN 1 | 192.168.1.0/26 |
| LAN 2 | 192.168.1.64/26 |
| R1 – R2 | 192.168.1.128/30 |
| R2 – R3 | 192.168.1.132/30 |
| R3 – R4 | 192.168.1.136/30 |
| R4 – R5 | 192.168.1.140/30 |
| R5 – R1 | 192.168.1.144/30 |

## Configuration
RIPv2 was configured on all five routers using the appropriate network statements.

## Verification
- Verified routing tables using `show ip route`.
- Checked dynamically learned routes marked with the `R` routing code.
- Performed ping tests between end devices on different LANs.
- Verified successful communication across the network.

## Tools Used
- Cisco Packet Tracer

## Lab Outcome
Successfully implemented RIPv2 dynamic routing across a five-router topology and verified end-to-end connectivity between the two LAN networks.
