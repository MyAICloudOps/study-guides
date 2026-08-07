# Cisco CCNA (200-301 v1.1) Complete Study Guide

![Cisco](https://img.shields.io/badge/Cisco-CCNA-blue)
![Exam](https://img.shields.io/badge/Exam-200--301_v1.1-success)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Markdown](https://img.shields.io/badge/Built%20With-Markdown-informational)

A comprehensive, exam-focused study guide covering every objective in the **Cisco Certified Network Associate (CCNA) 200-301 v1.1** certification exam.

This repository is designed to teach the concepts required to pass the CCNA exam using detailed explanations, diagrams, CLI examples, Packet Tracer labs, troubleshooting scenarios, and review questions.

---

# About This Repository

This study guide closely follows the official **Cisco CCNA 200-301 v1.1** exam blueprint.

Each lesson is written in beginner-friendly language while providing the technical depth expected on the certification exam.

Every chapter includes:

- 📖 Detailed explanations
- 🖼️ Network diagrams
- 💻 Cisco IOS CLI examples
- 🧪 Packet Tracer labs
- 🔍 Troubleshooting exercises
- 💡 CCNA exam tips
- ⚠️ Common exam mistakes
- ❓ Review questions

---

# Exam Information

| Item | Details |
|------|---------|
| Certification | Cisco Certified Network Associate (CCNA) |
| Exam Code | 200-301 |
| Version | v1.1 |
| Exam Time | 120 Minutes |
| Questions | Approximately 90–100 |
| Question Types | Multiple Choice, Multiple Answer, Drag-and-Drop, CLI Simulations, Simlets |

---

# Exam Domains

| Domain | Weight |
|---------|-------:|
| 1. Network Fundamentals | 20% |
| 2. Network Access | 20% |
| 3. IP Connectivity | 25% |
| 4. IP Services | 10% |
| 5. Security Fundamentals | 15% |
| 6. Automation and Programmability | 10% |

---

# Repository Structure

```
CCNA-200-301/
│
├── README.md
├── LICENSE
│
├── 01-Network-Fundamentals/
├── 02-Network-Access/
├── 03-IP-Connectivity/
├── 04-IP-Services/
├── 05-Security-Fundamentals/
└── 06-Automation-and-Programmability/
```

---

# 1. Network Fundamentals (20%)

## 1.1 Explain the Role and Function of Network Components

- Routers
- Layer 2 Switches
- Layer 3 Switches
- Next-Generation Firewalls
- Intrusion Prevention Systems (IPS)
- Wireless Access Points
- Wireless LAN Controllers
- Endpoints
- Servers
- Power over Ethernet (PoE)

---

## 1.2 Describe Network Topology Architectures

- Two-Tier
- Three-Tier
- Spine-Leaf
- WAN
- SOHO
- On-Premises
- Cloud

---

## 1.3 Compare Physical Interfaces and Cabling Types

- Copper Ethernet
- Single-Mode Fiber
- Multimode Fiber
- Shared Ethernet Media
- Point-to-Point Links

---

## 1.4 Identify Interface and Cable Issues

- Collisions
- CRC Errors
- Duplex Mismatch
- Speed Mismatch
- Runts
- Giants

---

## 1.5 Compare TCP and UDP

- TCP
- UDP
- Reliability
- Connection-Oriented vs Connectionless
- Common Port Numbers
- Header Comparison

---

## 1.6 Configure and Verify IPv4 Addressing and Subnetting

- Binary
- CIDR
- Subnetting
- VLSM
- Route Summarization

---

## 1.7 Describe Private IPv4 Addressing

- RFC1918
- Public vs Private Addresses
- NAT Overview

---

## 1.8 Configure and Verify IPv6 Addressing

- IPv6 Format
- Prefix Lengths
- Address Compression
- Address Expansion

---

## 1.9 Describe IPv6 Address Types

- Global Unicast
- Unique Local
- Link Local
- Anycast
- Multicast
- Modified EUI-64

---

## 1.10 Verify IP Parameters for Client Operating Systems

- Windows
- Linux
- macOS

---

## 1.11 Describe Wireless Principles

- RF
- SSID
- Nonoverlapping Wi-Fi Channels
- Wireless Encryption

---

## 1.12 Explain Virtualization Fundamentals

- Server Virtualization
- Virtual Machines
- Containers
- VRFs

---

## 1.13 Describe Switching Concepts

- MAC Learning
- MAC Address Table
- Frame Switching
- Frame Flooding
- MAC Aging

---

# 2. Network Access (20%)

## 2.1 VLAN Configuration

- VLAN Creation
- Access Ports
- Voice VLANs
- Default VLAN
- Inter-VLAN Routing

---

## 2.2 Interswitch Connectivity

- Trunk Ports
- IEEE 802.1Q
- Native VLAN

---

## 2.3 Layer 2 Discovery Protocols

- Cisco Discovery Protocol (CDP)
- Link Layer Discovery Protocol (LLDP)

---

## 2.4 EtherChannel

- Layer 2 EtherChannel
- Layer 3 EtherChannel
- LACP

---

## 2.5 Rapid PVST+

- Root Bridge
- Root Port
- Designated Port
- Alternate Port
- Port Roles
- Port States
- PortFast
- Root Guard
- Loop Guard
- BPDU Guard
- BPDU Filter

---

## 2.6 Cisco Wireless Architectures

- Lightweight AP
- Autonomous AP
- Controller-Based Wireless

---

## 2.7 WLAN Infrastructure

- Access Points
- Wireless LAN Controllers
- Access Ports
- Trunk Ports
- Link Aggregation (LAG)

---

## 2.8 Device Management Access

- Console
- Telnet
- SSH
- HTTP
- HTTPS
- TACACS+
- RADIUS
- Cloud Management

---

## 2.9 Wireless LAN GUI Configuration

- WLAN Creation
- Client Connectivity
- Security Settings
- QoS Profiles
- Advanced Settings

---

# 3. IP Connectivity (25%)

## 3.1 Routing Table Components

- Route Codes
- Prefixes
- Network Masks
- Next-Hop Addresses
- Administrative Distance
- Metrics
- Gateway of Last Resort

---

## 3.2 Router Forwarding Decisions

- Longest Prefix Match
- Administrative Distance
- Routing Metrics

---

## 3.3 Static Routing

- Network Routes
- Default Routes
- Host Routes
- Floating Static Routes
- IPv4
- IPv6

---

## 3.4 Single-Area OSPFv2

- Neighbor Adjacencies
- Router ID
- Point-to-Point Networks
- Broadcast Networks
- DR Election
- BDR Election

---

## 3.5 First Hop Redundancy Protocols

- Purpose
- Operation
- High Availability Concepts

---

# 4. IP Services (10%)

## 4.1 Network Address Translation

- Static NAT
- Dynamic NAT
- NAT Pools

---

## 4.2 Network Time Protocol (NTP)

- Client Mode
- Server Mode

---

## 4.3 DHCP and DNS

- DHCP Operation
- DNS Operation

---

## 4.4 SNMP

- Monitoring
- Management

---

## 4.5 Syslog

- Facilities
- Severity Levels

---

## 4.6 DHCP Client and Relay

- DHCP Client
- DHCP Relay Agent

---

## 4.7 Quality of Service (QoS)

- Classification
- Marking
- Queuing
- Congestion
- Policing
- Shaping

---

## 4.8 Secure Remote Access

- SSH Configuration
- SSH Verification

---

## 4.9 File Transfer Services

- TFTP
- FTP

---

# 5. Security Fundamentals (15%)

## 5.1 Security Concepts

- Threats
- Vulnerabilities
- Exploits
- Mitigation

---

## 5.2 Security Programs

- User Awareness
- Security Training
- Physical Security

---

## 5.3 Device Access Control

- Local Passwords
- Secure Access

---

## 5.4 Password Policies

- Password Complexity
- Password Management
- Multi-Factor Authentication
- Certificates
- Biometrics

---

## 5.5 VPN Technologies

- Remote Access VPN
- Site-to-Site VPN
- IPsec

---

## 5.6 Access Control Lists (ACLs)

- Standard ACLs
- Extended ACLs
- Verification

---

## 5.7 Layer 2 Security

- DHCP Snooping
- Dynamic ARP Inspection
- Port Security

---

## 5.8 AAA

- Authentication
- Authorization
- Accounting

---

## 5.9 Wireless Security

- WPA
- WPA2
- WPA3

---

## 5.10 WLAN Configuration

- WPA2-PSK Configuration
- Verification

---

# 6. Automation and Programmability (10%)

## 6.1 Network Automation

- Benefits
- Use Cases

---

## 6.2 Controller-Based Networking

- Traditional Networks
- SDN
- Controller-Based Networks

---

## 6.3 Software-Defined Architecture

- Overlay
- Underlay
- Fabric
- Control Plane
- Data Plane
- Northbound APIs
- Southbound APIs

---

## 6.4 AI and Machine Learning

- Predictive AI
- Generative AI
- Network Operations

---

## 6.5 REST APIs

- Authentication
- CRUD Operations
- HTTP Methods
- JSON
- XML

---

## 6.6 Configuration Management

- Ansible
- Terraform

---

## 6.7 JSON

- Objects
- Arrays
- Key-Value Pairs
- JSON Syntax

---

# Recommended Lab Software

- Cisco Packet Tracer
- Cisco Modeling Labs (CML)
- GNS3
- Wireshark
- VirtualBox

---

# Study Tips

- Complete the lessons in numerical order.
- Build every Packet Tracer lab yourself.
- Practice subnetting regularly until it becomes second nature.
- Learn to interpret routing tables without relying on memorization.
- Practice using the Cisco CLI daily.
- Review troubleshooting scenarios after each topic.
- Complete the review questions before moving to the next lesson.

---

# License

This project is licensed under the **MIT License**.
