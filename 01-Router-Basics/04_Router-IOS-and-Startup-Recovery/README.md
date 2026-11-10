# Router IOS and Startup Configuration Recovery Using TFTP

## Project Overview
This practical lab demonstrates how to recover a Cisco router's IOS image and restore its startup configuration using a TFTP server.

The lab covers two recovery procedures:
1. Router IOS recovery through ROMMON mode.
2. Startup configuration recovery from a TFTP server.

## Objectives
- Understand the router IOS recovery process.
- Recover a deleted IOS image from a TFTP server.
- Configure ROMMON environment variables.
- Restore a backed-up startup configuration.
- Understand the role of TFTP in disaster recovery.

## Network Details

| Device | IP Address |
|---|---|
| Router FastEthernet0/0 | 192.168.1.1/28 |
| TFTP Server | 192.168.1.10/28 |

**IOS Image:** `2800nm-advipservicesk9-mz.151-4.M4.bin`

**Backup Configuration File:** `Pune-Router-config`

## Practical Implementation

### Part 1: Router IOS Recovery
1. Checked the router's flash memory using `show flash`.
2. Deleted the existing IOS image from flash memory.
3. Restarted the router and entered ROMMON mode.
4. Configured the required ROMMON environment variables:
   - IP_ADDRESS
   - IP_SUBNET_MASK
   - DEFAULT_GATEWAY
   - TFTP_SERVER
   - TFTP_FILE
5. Executed `tftpdnld` to download the IOS image from the TFTP server.
6. Reloaded the router using `reset`.

### Part 2: Startup Configuration Recovery
1. Configured the router's FastEthernet interface.
2. Assigned the IP address and enabled the interface.
3. Retrieved the backed-up configuration using `copy tftp startup-config`.
4. Loaded the startup configuration into running configuration using `copy startup-config running-config`.
5. Verified the restored configuration.

## Commands Used
Refer to [Commands.txt](Commands.txt) for the complete list of configuration and recovery commands.

## Verification
- IOS image successfully recovered from the TFTP server.
- Router successfully restarted after IOS recovery.
- Startup configuration successfully copied from the TFTP server.
- Restored configuration loaded into running configuration.

## Technologies and Concepts
- Cisco IOS
- ROMMON Mode
- TFTP Server
- IOS Image Recovery
- Startup Configuration Recovery
- Cisco Router CLI
- Disaster Recovery

## Learning Outcome
Through this practical, I gained hands-on experience with Cisco router IOS recovery and startup configuration restoration using a TFTP server. I also learned how ROMMON mode helps recover a router when its IOS image is unavailable.

**Platform:** Cisco Packet Tracer

**Category:** CCNA Practical Lab
