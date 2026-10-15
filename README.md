Cisco RIP v2 Routing Lab – Packet Tracer

Overview

This lab demonstrates how to configure RIP Version 2 on two Cisco routers to enable dynamic routing and communication between two different LANs.

Objectives

Configure router interfaces with IP addresses.

Enable RIP Version 2 on both routers.

Exchange routing information dynamically.

Verify routing tables and test connectivity.

Devices Used

2 Cisco Routers

2 PCs

Ethernet cables

IP Addressing

Device

Interface/Network

IP Address

Subnet Mask

R1

LAN

192.168.1.1

255.255.255.0

R1

Router Link

10.0.0.1

255.255.255.252

R2

Router Link

10.0.0.2

255.255.255.252

R2

LAN

192.168.2.1

255.255.255.0

PC1

NIC

192.168.1.2

255.255.255.0

PC2

NIC

192.168.2.2

255.255.255.0

RIP Configuration

Router R1

router rip
version 2
no auto-summary
network 192.168.1.0
network 10.0.0.0

Router R2

router rip
version 2
no auto-summary
network 192.168.2.0
network 10.0.0.0

PC Default Gateways

PC1: 192.168.1.1

PC2: 192.168.2.1

Verification Commands

show ip interface brief
show ip route
show ip protocols

Use ping from PC1 to PC2 to verify end-to-end connectivity. Routes learned through RIP are marked with R in the routing table.

Result

RIP Version 2 was configured to exchange routing information dynamically between two routers, allowing communication between the two LANs.

Key Learnings

RIP Version 2 configuration

Dynamic routing

IP addressing and subnetting

Routing table verification

Network connectivity troubleshooting

Tools

Cisco Packet Tracer
