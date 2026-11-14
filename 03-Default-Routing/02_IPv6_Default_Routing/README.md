
# IPv6 Default Routing

## Overview
This lab demonstrates IPv6 Default Static Routing between two Cisco routers using Cisco Packet Tracer.

A default route is configured on each router to forward packets destined for unknown networks toward the neighboring router.

## Topology
- 2 Routers (R1 and R2)
- 2 Switches
- 8 PCs
- IPv6 addressing

## IPv6 Addressing

| Device | Interface | IPv6 Address |
|---|---|---|
| R1 | Fa0/0 | FD00::1/64 |
| R1 | Fa0/1 | 2001::1/64 |
| R2 | Fa0/0 | FD01::1/64 |
| R2 | Fa0/1 | 2001::2/64 |

### Network Prefixes
- R1 LAN: FD00::/64
- R2 LAN: FD01::/64
- Router-to-router network: 2001::/64

## Configuration

### R1 - IPv6 Default Route
```cisco
ipv6 route ::/0 2001::2
```

### R2 - IPv6 Default Route
```cisco
ipv6 route ::/0 2001::1
```

## Verification Commands

```cisco
show ipv6 interface brief
show ipv6 route
```

## Connectivity Testing

- Verified connectivity between PCs in different LANs.
- Successfully pinged the remote LAN IPv6 addresses.
- Successfully pinged the neighboring router's IPv6 address.
- Confirmed successful communication with 0% packet loss in the displayed tests.

## Key Concepts Practiced

- IPv6 Addressing
- IPv6 Default Static Routing
- IPv6 Routing Table
- Default Route (::/0)
- Network Connectivity Testing

## Tool Used
Cisco Packet Tracer
