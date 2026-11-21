# IPv6 RIP Routing Lab (RIPng)

## Project Overview
This project demonstrates the configuration and implementation of IPv6 dynamic routing using RIPng (Routing Information Protocol next generation) in Cisco Packet Tracer.

The network consists of 7 routers, 2 switches, and multiple end devices connected through different IPv6 networks.

The objective of this lab is to establish communication between different IPv6 networks using RIPng and verify successful route advertisement and connectivity.

## Network Topology
- 7 Cisco routers (R1–R7)
- 2 switches
- Multiple laptops/end devices
- IPv6 addressing using /64 prefixes
- Multiple interconnected router networks

## IPv6 Addressing
The lab uses the following IPv6 network prefixes:

- 2001::/64
- 2002::/64
- 2003::/64
- 2004::/64
- 2005::/64
- 2006::/64
- 2007::/64
- FD00::/64
- FD01::/64

## Technologies and Concepts Practiced
- IPv6 Address Configuration
- RIPng Dynamic Routing
- IPv6 Router Interface Configuration
- IPv6 Routing Table Verification
- Link-Local IPv6 Addresses
- End-to-End IPv6 Connectivity
- Ping Testing
- Traceroute Verification

## Configuration Commands

RIPng configuration was performed on the routers using:

```cisco
ipv6 router rip R1
```

RIPng was enabled on the required router interfaces using:

```cisco
interface fastethernet 0/0
ipv6 rip R1 enable
```

The same routing configuration was implemented on the other routers using the appropriate RIPng process name and interface settings.

## Verification Commands

The following commands were used to verify the configuration:

```cisco
show ipv6 interface brief
show ipv6 route
```

Connectivity testing from end devices:

```text
ping 2005::2
tracert fd01::3
```

## Verification Results

- IPv6 RIP routes were successfully learned and displayed in the routing table.
- End-to-end IPv6 connectivity was verified using ping.
- Traceroute successfully displayed the path between source and destination networks.
- The routing table showed connected, local, and RIP-learned routes.

## Tools Used
- Cisco Packet Tracer

## Project Status
Successfully configured and tested IPv6 RIPng dynamic routing in a multi-router network.
