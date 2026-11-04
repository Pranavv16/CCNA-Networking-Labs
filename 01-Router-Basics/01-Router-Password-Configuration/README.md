# Cisco Router Password Configuration

**Platform:** Cisco Packet Tracer  
**Router Model:** Cisco 2811  
**Access Method:** Console Connection  
**Category:** Router Security & Basic Configuration

---

## 1. Overview

This lab focuses on implementing basic password security and user authentication on a Cisco router using the Command Line Interface (CLI).

A laptop is connected to the router through a console cable to perform the initial configuration and secure different router access lines.

## 2. Lab Objectives

- Configure a hostname for router identification.
- Create a local user account with an encrypted secret.
- Implement console line authentication using local credentials.
- Configure AUX line authentication.
- Secure privileged EXEC mode using an enable secret.
- Configure VTY line authentication for remote access.
- Enable password encryption in the running configuration.
- Verify the implemented security configurations.

## 3. Network Topology

The lab consists of the following devices:

| Device | Model / Type | Purpose |
|---|---|---|
| Router | Cisco 2811 | Password configuration and authentication |
| Laptop | Laptop-PT | Accessing router CLI |
| Connection | Console Cable | Local device management |

## 4. Configurations Performed

### 4.1 Hostname Configuration

Configured the router hostname for device identification.

```cisco
hostname Pune-Router
```

### 4.2 Local User Account Configuration

Created a local user account using the `secret` keyword.

```cisco
username pranav secret <password>
```

### 4.3 Console Line Authentication

Enabled local user authentication for console access.

```cisco
line console 0
login local
```

### 4.4 AUX Line Authentication

Configured local authentication for the auxiliary line.

```cisco
line aux 0
login local
```

### 4.5 Enable Secret Configuration

Secured privileged EXEC mode using an enable secret.

```cisco
enable secret <password>
```

### 4.6 VTY Line Authentication

Configured local user authentication for VTY lines.

```cisco
line vty 0 4
login local
```

### 4.7 Password Encryption

Enabled password encryption in the router configuration.

```cisco
service password-encryption
```

## 5. Verification and Testing

Used the following commands to verify the router security configuration.

| Command | Purpose |
|---|---|
| `show running-config` | Displays the active configuration |
| `show running-config \| include password` | Displays password-related configuration |
| `show running-config \| include secret` | Verifies secret entries |
| `show running-config \| section line` | Displays line configuration |

**Authentication Testing:**
- Verified local username authentication through the console connection.
- Tested privileged EXEC access using the enable secret.
- Verified the configured console, AUX and VTY line settings.

## 6. Skills Practiced

- Cisco IOS CLI
- Local User Authentication
- Console Line Security
- AUX Line Configuration
- VTY Line Authentication
- Enable Secret Configuration
- Password Encryption
- Configuration Verification

## 7. Learning Outcomes

Gained practical experience in securing Cisco router access through local user authentication and password configurations. Also developed an understanding of different router access lines and the verification of security-related configurations.

## 8. Lab Resources

- Packet Tracer Project: `Router-Password-Configuration.pkt`
- Configuration Screenshots
- Verification Screenshots
- Network Topology

---
