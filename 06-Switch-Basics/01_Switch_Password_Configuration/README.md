
# Cisco Switch Password Configuration Lab

## Project Overview
This project demonstrates basic password security configuration on a Cisco switch using Cisco Packet Tracer.

The main objective was to secure switch access using local user authentication, enable secret, console login security, VTY login security, and password encryption.

## Topology
- 1 Cisco Switch
- 1 Laptop
- Console Cable

## Configuration Tasks

1. Configured switch hostname.
2. Created a local username using the secret command.
3. Configured enable secret for privileged EXEC mode.
4. Enabled local authentication on console line 0.
5. Enabled local authentication on VTY lines 0–4.
6. Enabled password encryption using service password-encryption.
7. Saved the configuration to startup-config.
8. Verified the configuration using show commands.

## Commands Used

- hostname Cisco-Switch
- username pranav secret [REDACTED]
- enable secret [REDACTED]
- line console 0
- login local
- line vty 0 4
- login local
- service password-encryption
- copy running-config startup-config

## Verification Commands

- show running-config
- show running-config | include password
- show running-config | include secret
- show running-config | section line

## Technologies Used
- Cisco Packet Tracer
- Cisco IOS CLI
- Switch Security
- Local Authentication
- Password Encryption

## Learning Outcomes

- Understanding local user authentication.
- Securing console access.
- Configuring VTY line authentication.
- Understanding enable secret.
- Understanding password encryption.
- Verifying and saving switch configurations.
