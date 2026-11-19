Inter-Area OSPF Routing Lab
Project Overview
This project demonstrates a multi-area OSPF (Open Shortest Path First) network configured in Cisco Packet Tracer. The topology contains five routers (R1, R2, ABR-R3, R4, and R5), four LAN segments, and three OSPF areas:
- Area 100 – Left-side networks connected through R1 and R2
- Area 0 – OSPF backbone connecting R2, ABR-R3, and R4
- Area 200 – Right-side networks connected through R4 and R5
The lab focuses on OSPF neighbor formation and the exchange of routing information between areas.
Network Topology and Addressing
Router	Interface	IP address	Connected network	OSPF area
R1	FastEthernet0/0	170.170.0.1/30	170.170.0.0/30	100
R1	FastEthernet0/1	192.168.1.1/24	192.168.1.0/24	100
R2	FastEthernet0/0	170.170.0.2/30	170.170.0.0/30	100
R2	FastEthernet0/1	180.180.180.1/30	180.180.180.0/30	0
R2	FastEthernet1/0	172.20.0.1/24	172.20.0.0/24	100
ABR-R3	FastEthernet0/0	180.180.180.2/30	180.180.180.0/30	0
ABR-R3	FastEthernet0/1	200.50.50.1/30	200.50.50.0/30	0
R4	FastEthernet0/0	200.50.50.2/30	200.50.50.0/30	0
R4	FastEthernet0/1	150.160.100.1/30	150.160.100.0/30	200
R4	FastEthernet1/0	10.10.10.1/26	10.10.10.0/26	200
R5	FastEthernet0/0	150.160.100.2/30	150.160.100.0/30	200
R5	FastEthernet0/1	172.16.0.1/28	172.16.0.0/28	200


OSPF Configuration Summary
- OSPF process ID 1 is configured on R1, R2, R4, and R5.
- OSPF process ID 2 is configured on ABR-R3.
- R1 and R2 advertise their LAN and inter-router networks in Area 100.
- R2 connects Area 100 to the Area 0 backbone.
- ABR-R3 has both shown interfaces configured in Area 0.
- R4 connects Area 0 to Area 200.
- R5 advertises its LAN and inter-router network in Area 200.
Concepts Practiced
- OSPF multi-area routing
- Backbone Area 0 and non-backbone areas
- OSPF network statements and wildcard masks
- OSPF neighbor adjacency
- Inter-area route learning
- Reading and verifying OSPF routing-table entries
Verification Commands
The following commands were used in the lab to inspect interfaces, OSPF neighbors, routing information, and protocol operation:
show ip interface brief
show ip ospf neighbor
show ip ospf interface brief
show ip ospf database
show ip route
show ip route ospf
show ip protocols
Use ping <destination-ip> and traceroute <destination-ip> to test reachability and the path to a destination.
Routing Table Verification
The routing-table screenshots show:
- O – OSPF route
- O IA – OSPF inter-area route
The displayed routing tables contain O IA entries for networks learned from other OSPF areas. This is evidence of inter-area route exchange in the lab.
Project Structure
Inter-Area-OSPF-Routing/
├── README.md
├── Configuration-Commands.txt
└── Screenshots/
    ├── 01-Network-Topology.png
    ├── 02-R1-Configuration.png
    ├── 03-R1-Routing-Table.png
    ├── 04-R2-Configuration.png
    ├── 05-R2-Routing-Table.png
    ├── 06-ABR-R3-Configuration.png
    ├── 07-ABR-R3-Routing-Table.png
    ├── 08-R4-Configuration.png
    ├── 09-R4-Routing-Table.png
    ├── 10-R5-Configuration.png
    └── 11-R5-Routing-Table.png
Tools Used
- Cisco Packet Tracer
Learning Outcome
Practiced configuring OSPF across multiple areas, forming OSPF neighbor relationships, and verifying routes learned from other areas through the routing table.
Configuration Note
The topology image labels R3 as Area Border Router. However, the supplied R3 CLI screenshot shows both R3 network statements assigned to Area 0. Based on the displayed configurations, R2 connects Area 100 to Area 0, and R4 connects Area 0 to Area 200. Review this role/label difference if you update the topology or router configurations.
