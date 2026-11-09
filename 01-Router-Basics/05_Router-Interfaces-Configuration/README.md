# Router Interface IP Configuration

## Lab Overview
This practical demonstrates how to configure IPv4 addresses on router interfaces using Cisco IOS commands in Cisco Packet Tracer.

## Objectives
- Configure IP addresses on router interfaces.
- Enable router interfaces using the `no shutdown` command.
- Configure static IP addresses on end devices.
- Assign appropriate subnet masks and default gateways.
- Verify interface status using CLI commands.

## Network Topology
The topology consists of:
- 2 Cisco Routers
- 2 Switches
- 6 PCs

## IP Addressing Scheme

| Device | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| Router0 | Fa0/0 | 180.180.0.1 | 255.255.255.252 |
| Router0 | Fa0/1 | 192.168.1.1 | 255.255.255.240 |
| Router1 | Fa0/0 | 180.180.0.2 | 255.255.255.252 |
| Router1 | Fa0/1 | 172.16.0.1 | 255.255.255.240 |

## Technologies and Commands Used
- IPv4 Addressing
- Subnetting (/30 and /28)
- Cisco IOS CLI
- Interface Configuration
- `ip address`
- `no shutdown`
- `show ip interface brief`

## Verification
Used the `show ip interface brief` command to verify the configured IP addresses and interface status.

## Learning Outcome
Gained practical experience in configuring router interfaces, assigning IPv4 addresses, enabling interfaces, and understanding basic network addressing.

## Tools Used
Cisco Packet Tracer

## Project Files
- Packet Tracer topology file
- Router configuration commands
- Practical screenshots
