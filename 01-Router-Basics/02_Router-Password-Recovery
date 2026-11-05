# Cisco Router Password Recovery

## Overview
This practical lab demonstrates the Cisco router password recovery procedure using ROMMON (ROM Monitor) mode. The objective was to regain privileged access to a Cisco router when the existing login credentials were unavailable.

## Objectives
- Access the router through ROMMON mode.
- Modify the configuration register to bypass the startup configuration.
- Recover access to the existing router configuration.
- Remove the previous password configuration.
- Restore the default configuration register value.
- Save the updated configuration.

## Practical Implementation

### Step 1: Enter ROMMON Mode
Interrupted the router boot process to access ROMMON mode.

```cisco
rommon 1 > confreg 2142
rommon 2 > reset
```

### Step 2: Bypass Startup Configuration
After rebooting, bypassed the existing startup configuration and accessed the router without loading the previous credentials.

### Step 3: Load the Existing Configuration
Entered privileged EXEC mode and copied the startup configuration into the running configuration.

```cisco
Router> enable
Router# copy startup-config running-config
```

### Step 4: Remove Previous Password Configuration
Entered global configuration mode and removed the existing enable secret and local username credentials.

```cisco
Router# configure terminal
Router(config)# no enable secret
Router(config)# no username pranav
```

### Step 5: Update Line Authentication
Modified the console, auxiliary and VTY line authentication settings.

```cisco
Router(config)# line console 0
Router(config-line)# no login local

Router(config)# line aux 0
Router(config-line)# no login local

Router(config)# line vty 0 4
Router(config-line)# no login local
```

### Step 6: Restore Configuration Register
Restored the configuration register to its normal boot value.

```cisco
Router(config)# config-register 0x2102
```

### Step 7: Save Configuration
Saved the updated configuration to NVRAM.

```cisco
Router# copy running-config startup-config
```

## Technologies & Concepts
- Cisco IOS
- ROMMON Mode
- Configuration Register
- Startup Configuration
- Running Configuration
- NVRAM
- Password Recovery

## Learning Outcome
Successfully practiced the Cisco router password recovery procedure using ROMMON mode and learned how to regain access to an existing router configuration, modify authentication settings, restore the configuration register and save the updated configuration.

**Platform:** Cisco Packet Tracer  
**Router:** Cisco 2800 Series
