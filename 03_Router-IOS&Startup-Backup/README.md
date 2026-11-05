# Cisco Router IOS and Startup Configuration Backup Using TFTP

## Overview
This practical lab demonstrates how to back up a Cisco router's IOS image and startup configuration to a TFTP server. The objective was to transfer important router files from the Cisco 2811 router to a centralized TFTP server for backup and recovery purposes.

## Lab Topology
- Cisco 2811 Router
- TFTP Server
- Laptop (Console Access)

## IP Addressing

| Device | Interface | IP Address |
|---|---|---|
| Pune-Router | FastEthernet0/0 | 192.168.1.1/28 |
| TFTP Server | FastEthernet0 | 192.168.1.10/28 |

## Practical Implementation

### Step 1: Configure Router Interface

Configured the router's FastEthernet interface and assigned an IP address.

```cisco
configure terminal
interface fastethernet 0/0
ip address 192.168.1.1 255.255.255.240
no shutdown
```

### Step 2: Verify IOS Image in Flash Memory

Used the following command to view the IOS image stored in router flash memory.

```cisco
do show flash
```

IOS Image:
`2800nm-advipservicesk9-mz.151-4.M4.bin`

### Step 3: Back Up IOS Image to TFTP Server

Used the copy command to transfer the IOS image from router flash memory to the TFTP server.

```cisco
do copy flash tftp
```

- Source filename: 2800nm-advipservicesk9-mz.151-4.M4.bin
- TFTP Server Address: 192.168.1.10
- Transfer Status: Successful

### Step 4: Back Up Startup Configuration

Transferred the router's startup configuration to the TFTP server.

```cisco
do copy startup-config tftp
```

- TFTP Server Address: 192.168.1.10
- Destination Filename: Pune-Router-config
- Transfer Status: Successful

## Verification

Both backup operations completed successfully.

- IOS image transferred: 33,591,768 bytes
- Startup configuration transferred: 632 bytes
- TFTP server received both backup files.

## Technologies & Concepts
- Cisco IOS
- Cisco 2811 Router
- TFTP (Trivial File Transfer Protocol)
- Flash Memory
- Startup Configuration
- Network File Backup
- Cisco IOS CLI

## Learning Outcome
Practiced backing up a Cisco router's IOS image and startup configuration to a TFTP server. This lab helped me understand how to preserve important router files for future recovery, restoration and backup purposes.

**Platform:** Cisco Packet Tracer  
**Router:** Cisco 2811  
**Backup Method:** TFTP
