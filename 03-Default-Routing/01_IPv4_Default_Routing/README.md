# Default Routing Lab (Cisco Packet Tracer)

## Overview
This lab demonstrates the configuration of Default Static Routing using three Cisco routers in Cisco Packet Tracer.

The topology consists of three routers connected through point-to-point links, with each router connecting to its own LAN network.

## Network Topology

- **R1 LAN:** 192.168.1.0/24
- **R2 LAN:** 172.16.0.0/24
- **R1–R2 Link:** 100.100.50.0/30

## Technologies & Concepts Practiced

- Default Static Routing
- IPv4 Addressing
- Point-to-Point Router Connectivity
- Routing Table Verification
- End-to-End Connectivity Testing

## Default Route Configuration

**R1:**
```bash
ip route 0.0.0.0 0.0.0.0 100.100.50.2
```

**R2:**
```bash
ip route 0.0.0.0 0.0.0.0 100.100.50.1
```

## Verification Commands

```bash
show ip interface brief
show ip route
ping <destination-ip>
```

## Connectivity Testing

Successfully tested connectivity between different LAN networks using ping commands.

## Tools Used
- Cisco Packet Tracer

