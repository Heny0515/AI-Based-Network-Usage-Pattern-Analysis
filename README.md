# AI-Based-Network-Usage-Pattern-Analysis
VLAN-based network designed using Cisco Packet Tracer featuring Student Staff Server and Attacker networks Implements VLAN segmentation, Router-on-a-Stick inter-VLAN routing, trunking, DNS and HTTP services, and network connectivity testing. Uses Simulation Mode to monitor packet flow and explores ACL-based security to restrict unauthorized access.
#  Campus Network Security Using Cisco Packet Tracer

<p align="center">
  <b>A Secure, VLAN-Based Campus Network with Inter-VLAN Routing and Access Control</b>
</p>

##  Project Overview

This project demonstrates the design and implementation of a secure campus network using Cisco Packet Tracer. The network connects multiple departments, servers, and end devices through VLAN segmentation, inter-VLAN routing, and Access Control Lists (ACLs).

The main objective is to create a structured network infrastructure that enables communication between authorized departments while restricting unauthorized access to sensitive server resources.

##  Project Objectives

- Design a realistic campus network topology.
- Divide the network into separate departmental VLANs.
- Configure inter-VLAN communication using Router-on-a-Stick.
- Implement 802.1Q trunking between network devices.
- Configure static IP addressing and default gateways.
- Implement ACLs for network traffic filtering.
- Connect two routers to simulate communication between different networks.
- Test connectivity and verify security restrictions.

##  Technologies & Tools

| Technology | Purpose |
|---|---|
| Cisco Packet Tracer | Network simulation |
| Cisco IOS | Router and switch configuration |
| VLAN | Network segmentation |
| 802.1Q | VLAN trunking |
| Router-on-a-Stick | Inter-VLAN routing |
| ACL | Network access control |
| STP | Loop prevention |
| ICMP / Ping | Connectivity testing |

##  Network Architecture

The network consists of the following components:

- **R1:** Main campus router responsible for inter-VLAN routing.
- **R2:** Secondary router connected to the external network.
- **SW1:** Main campus switch connecting students, staff, and servers.
- **SW2:** Secondary switch connecting the attacker network.
- **Student PCs:** Devices assigned to the Students VLAN.
- **Staff PC:** Device assigned to the Staff VLAN.
- **Server A and Server B:** Centralized server resources.
- **Attacker PC:** External device used to demonstrate network security.

##  VLAN Configuration

| VLAN ID | VLAN Name | Network Address | Gateway |
|---|---|---|---|
| 10 | Students | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Staff | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Servers | 192.168.30.0/24 | 192.168.30.1 |

##  IP Addressing Scheme

| Device | IP Address |
|---|---|
| Student-PC1 | 192.168.10.2 |
| Student-PC2 | 192.168.10.3 |
| Staff-PC | 192.168.20.2 |
| Server-A | 192.168.30.10 |
| R1 VLAN 10 Gateway | 192.168.10.1 |
| R1 VLAN 20 Gateway | 192.168.20.1 |
| R1 VLAN 30 Gateway | 192.168.30.1 |
| Attacker-PC | 203.0.113.10 |
| R1-R2 Link | 172.16.0.1 / 172.16.0.2 |

Subnet Mask: `255.255.255.0`

##  Key Implementations

### 1. VLAN Configuration
Created three separate VLANs to isolate Students, Staff, and Servers.

### 2. Inter-VLAN Routing
Configured Router-on-a-Stick using router subinterfaces and IEEE 802.1Q encapsulation to enable communication between VLANs.

### 3. Trunk Configuration
Configured trunk links between the router and switch to carry multiple VLANs over a single physical connection.

### 4. Spanning Tree Protocol
Verified STP operation to prevent switching loops and maintain a stable network topology.

### 5. MAC Address Learning
Used dynamic MAC address tables to verify device connectivity and identify connected interfaces.

### 6. Access Control Lists (ACL)
Implemented an extended ACL to deny traffic from the attacker IP address `203.0.113.10` to the protected server network `192.168.30.0/24`, while permitting other IP traffic.

##  Testing & Verification

The following commands were used to verify network configuration:

**Router Commands**
- `show ip interface brief`
- `show ip route`
- `show access-lists`
- `show running-config`

**Switch Commands**
- `show vlan brief`
- `show interfaces trunk`
- `show spanning-tree vlan 20`
- `show mac address-table`
- `show cdp neighbors`

**Connectivity Testing**
- `ping 192.168.10.1`
- `ping 192.168.20.1`
- `ping 192.168.30.10`
- `ping 203.0.113.1`

##  Security Features

- Department-wise network isolation.
- Controlled communication between VLANs.
- Extended ACL-based traffic filtering.
- Restricted attacker access to the server network.
- Centralized network routing and management.

##  Project Structure

```text
Campus-Network-Security/
│
├── README.md
│
├── Packet-Tracer/
│   └── Campus-Network.pkt
│
├── Screenshots/
│   ├── Network-Topology.png
│   ├── VLAN-Configuration.png
│   ├── Router-Configuration.png
│   ├── Connectivity-Testing.png
│   └── ACL-Configuration.png
│
└── Documentation/
    └── Network-Configuration.txt
```

##  Learning Outcomes

Through this project, practical knowledge was gained in:

- Computer networking fundamentals.
- IP addressing and subnetting.
- VLAN creation and management.
- Router and switch configuration.
- Inter-VLAN routing.
- Network security using ACLs.
- Troubleshooting and connectivity verification.

##  Future Scope

- Implement DHCP for automatic IP allocation.
- Configure firewall-based security.
- Implement SSH for secure remote device management.
- Add network monitoring and logging.
- Expand the topology with additional departments.

##  Project Information

**Project Name:** Campus Network Security Using Cisco Packet Tracer

**Domain:** Computer Networking & Cybersecurity

**Platform:** Cisco Packet Tracer

**Project Type:** Academic / Practical Project

---

⭐ If you find this project useful, consider giving this repository a star!
