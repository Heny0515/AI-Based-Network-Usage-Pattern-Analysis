# AI-Based-Network-Usage-Pattern-Analysis
VLAN-based network designed using Cisco Packet Tracer featuring Student Staff Server and Attacker networks Implements VLAN segmentation, Router-on-a-Stick inter-VLAN routing, trunking, DNS and HTTP services, and network connectivity testing. Uses Simulation Mode to monitor packet flow and explores ACL-based security to restrict unauthorized access.
# Campus Network Security Using Cisco Packet Tracer

## Project Overview
This project focuses on designing and implementing a secure campus network using Cisco Packet Tracer. It demonstrates network segmentation, inter-VLAN routing, connectivity between departments, and network security using Access Control Lists (ACLs).

## Objectives
- Design a campus network topology.
- Create separate VLANs for Students, Staff, and Servers.
- Configure inter-VLAN routing using Router-on-a-Stick.
- Configure trunk and access ports.
- Assign static IP addresses to network devices.
- Implement ACLs to control network traffic.
- Test network connectivity using the ping command.

## Technologies Used
- Cisco Packet Tracer
- Cisco IOS CLI
- VLAN Configuration
- Inter-VLAN Routing
- Access Control Lists (ACL)
- IP Addressing and Subnetting

## Network Configuration

| Department | VLAN ID | Network |
|---|---|---|
| Students | 10 | 192.168.10.0/24 |
| Staff | 20 | 192.168.20.0/24 |
| Servers | 30 | 192.168.30.0/24 |
| Attacker Network | N/A | 203.0.113.0/24 |

## Key Features
- VLAN-based network segmentation.
- Communication between different VLANs.
- Router-on-a-Stick configuration.
- 802.1Q trunking.
- Dynamic MAC address learning.
- Spanning Tree Protocol (STP).
- ACL-based traffic filtering.
- Network connectivity and security testing.

## Security Implementation
Extended Access Control Lists (ACLs) are configured on the router to control traffic between the attacker network and the server network. This demonstrates how unauthorized access to protected network resources can be restricted.

## Testing
Network connectivity is verified using ping commands between:
- Student PCs and their gateway.
- Staff PC and its gateway.
- PCs and server devices.
- Attacker PC and internal network devices.

## Learning Outcomes
This project provides practical experience in Cisco networking, VLAN management, routing, subnetting, network troubleshooting, and implementing basic network security mechanisms.

## Conclusion
The project demonstrates the design of a segmented campus network with inter-VLAN communication and ACL-based security. It provides hands-on experience in configuring, testing, and securing a network infrastructure using Cisco Packet Tracer.
