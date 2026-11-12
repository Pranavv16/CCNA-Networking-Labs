# IPv4 Static Routing – Three Router Network

## Project Overview
In this lab, I configured IPv4 Static Routing between three routers (R1, R2, and R3) using Cisco Packet Tracer.

The objective was to establish communication between three different LAN networks connected through multiple routers using manually configured static routes.

## Topology
- 3 Routers (R1, R2, R3)
- 3 Switches
- 9 PCs
- 3 LAN Networks
- Point-to-point router connections

## IP Addressing

| Device | Interface | IP Address |
|---|---|---|
| R1 | Fa0/0 | 170.170.0.1/30 |
| R1 | Fa0/1 | 192.168.1.1/26 |
| R2 | Fa0/0 | 170.170.0.2/30 |
| R2 | Fa0/1 | 180.180.0.1/30 |
| R2 | Fa1/0 | 172.16.0.1/26 |
| R3 | Fa0/0 | 180.180.0.2/30 |
| R3 | Fa0/1 | 10.10.10.1/26 |

## Static Routing Configuration

### R1
```cisco
ip route 10.10.10.0 255.255.255.192 170.170.0.2
ip route 172.16.0.0 255.255.255.192 170.170.0.2
```

### R2
```cisco
ip route 192.168.1.0 255.255.255.192 170.170.0.1
ip route 10.10.10.0 255.255.255.192 180.180.0.2
```

### R3
```cisco
ip route 172.16.0.0 255.255.255.192 180.180.0.1
ip route 192.168.1.0 255.255.255.192 180.180.0.1
```

## Verification
- Verified routing tables using `show ip route`.
- Checked interface status using `show ip interface brief`.
- Tested end-to-end connectivity using the `ping` command.
- Successfully established communication between devices across different LAN networks.

## Concepts Practiced
- IPv4 Addressing and Subnetting
- Static Route Configuration
- Next-Hop IP Address
- Routing Table Verification
- Inter-network Communication
- Network Connectivity Testing

## Tools Used
- Cisco Packet Tracer
- Cisco IOS CLI

