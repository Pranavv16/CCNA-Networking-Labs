# VLAN and Inter-VLAN Routing – Router-on-a-Stick

## Project Overview
This project demonstrates VLAN creation, access port assignment, trunk configuration, and Inter-VLAN Routing using the Router-on-a-Stick method in Cisco Packet Tracer.

The objective is to establish communication between multiple VLANs using a single physical router interface with multiple subinterfaces.

## Network Topology
- 1 Cisco Router
- 1 Cisco Switch
- 12 End Devices (PCs)
- 4 VLANs
- Router-on-a-Stick configuration

## VLAN and IP Addressing

| VLAN ID | VLAN Name | Network Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| 10 | Account | 192.168.10.0/26 | 255.255.255.192 | 192.168.10.1 |
| 20 | Sales | 192.168.10.64/26 | 255.255.255.192 | 192.168.10.65 |
| 30 | Marketing | 192.168.10.128/26 | 255.255.255.192 | 192.168.10.129 |
| 40 | Production | 192.168.10.192/26 | 255.255.255.192 | 192.168.10.193 |

## PC Address Allocation

| VLAN | PCs | IP Addresses |
|---|---|---|
| VLAN 10 | PC1–PC3 | 192.168.10.2–192.168.10.4 |
| VLAN 20 | PC4–PC6 | 192.168.10.66–192.168.10.68 |
| VLAN 30 | PC7–PC9 | 192.168.10.130–192.168.10.132 |
| VLAN 40 | PC10–PC12 | 192.168.10.194–192.168.10.196 |

## Switch Configuration

- Created VLAN 10 – Account
- Created VLAN 20 – Sales
- Created VLAN 30 – Marketing
- Created VLAN 40 – Production
- Assigned access ports to their respective VLANs.
- Configured GigabitEthernet0/1 as a trunk port to connect the router.

### Switch Port Allocation

| Interface Range | Mode | Assigned VLAN |
|---|---|---|
| Fa0/1–Fa0/3 | Access | VLAN 10 |
| Fa0/4–Fa0/6 | Access | VLAN 20 |
| Fa0/7–Fa0/9 | Access | VLAN 30 |
| Fa0/10–Fa0/12 | Access | VLAN 40 |
| Gi0/1 | Trunk | Router Connection |

## Router Configuration

Configured Router-on-a-Stick using FastEthernet0/0.

| Subinterface | VLAN | IP Address |
|---|---|---|
| Fa0/0.1 | 10 | 192.168.10.1/26 |
| Fa0/0.2 | 20 | 192.168.10.65/26 |
| Fa0/0.3 | 30 | 192.168.10.129/26 |
| Fa0/0.4 | 40 | 192.168.10.193/26 |

Used IEEE 802.1Q encapsulation to identify VLAN traffic on the router subinterfaces.

## Verification and Testing

The following commands were used to verify the configurations:

- `show vlan brief` – Verified VLAN creation and access port assignments.
- `show ip interface brief` – Verified router interface and subinterface status.
- `ping` – Tested connectivity between devices belonging to different VLANs.

### Connectivity Results

Successfully tested communication between PCs in different VLANs.

Examples:
- VLAN 10 to VLAN 20
- VLAN 10 to VLAN 30
- VLAN 10 to VLAN 40

Inter-VLAN communication was successfully established.

## Technologies and Concepts Practiced

- Virtual LAN (VLAN)
- VLAN Creation and Naming
- Access Port Configuration
- Trunk Port Configuration
- IEEE 802.1Q Encapsulation
- Router-on-a-Stick
- Router Subinterfaces
- IPv4 Subnetting (/26)
- Inter-VLAN Routing
- Network Connectivity Testing

## Tools Used
- Cisco Packet Tracer

## Project Outcome

Successfully configured four VLANs and established communication between different VLANs using Router-on-a-Stick configuration.

This lab provided practical experience in Layer 2 switching, VLAN segmentation, trunking, and Layer 3 Inter-VLAN Routing.
