# Cisco Switch Configuration and IOS Image Backup Using TFTP

## Project Overview
In this Cisco Packet Tracer lab, I practiced backing up a Cisco Catalyst 2960 switch's startup configuration and IOS image to a TFTP server.

The objective was to understand how network administrators can securely maintain copies of switch configurations and IOS software for recovery and troubleshooting purposes.

## Network Topology
The lab consists of:
- 1 Cisco Catalyst 2960 Switch
- 1 Laptop (Console Connection)
- 1 Server (TFTP Server)

## IP Addressing

| Device | Interface | IP Address | Subnet Mask |
|---|---|---|---|
| Switch | VLAN 1 | 192.168.10.1 | 255.255.255.248 |
| TFTP Server | FastEthernet0 | 192.168.10.5 | 255.255.255.248 |

## Configuration and Implementation

### 1. Switch Management Configuration
- Configured FastEthernet0/1 as an access port.
- Configured VLAN 1 as the switch management interface.
- Assigned the management IP address.
- Enabled the VLAN interface.

### 2. Startup Configuration Backup
Used the following command to copy the switch startup configuration to the TFTP server:

`copy startup-config tftp:`

Provided the TFTP server IP address: `192.168.10.5`

The configuration backup was successfully transferred to the server.

### 3. IOS Image Backup
First, verified the available files in switch flash memory:

`show flash`

Identified the Cisco IOS image:

`2960-lanbasek9-mz.150-2.SE4.bin`

Then copied the IOS image to the TFTP server:

`copy flash: tftp:`

Provided the source filename and TFTP server IP address.

The IOS image was successfully transferred.

## Technologies and Concepts Practiced
- Cisco IOS CLI
- Switch Management Interface (SVI)
- VLAN 1 Management
- TFTP Server Configuration
- Startup Configuration Backup
- Cisco IOS Image Backup
- Flash Memory Management
- Network Device Backup and Recovery

## Verification
Successfully verified:
- Startup configuration file on the TFTP server.
- Cisco IOS image on the TFTP server.
- Successful file transfer messages on the switch CLI.

## Lab Environment
- Cisco Packet Tracer
- Cisco Catalyst 2960 Switch
- TFTP Server

## Learning Outcome
Learned how to back up Cisco switch configurations and IOS images using a TFTP server, an important task in network device administration and disaster recovery.

## Author
Pranav Mahangare
