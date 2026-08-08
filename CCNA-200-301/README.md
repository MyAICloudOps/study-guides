# 🌐 CCNA 200-301 Study Guide

*Structured around your outline below. Each ☑️ module becomes its own chapter as we build them — chapters already written are linked. Unlinked modules are next up.*

---

## 🎓 How This Guide Works

- Each **Part** below matches an exam domain and its official weight.
- Each **Module** will become a chapter with learning objectives, hands-on Packet Tracer activities, and a quick check for understanding — same format as the chapters already built.
- ✅ = chapter written and linked. ⬜ = not yet written.

---

## 📗 Part 1 – Network Fundamentals (20%)

### Module 1 – Network Components
- What is a network?
- LAN vs WAN
- Internet, Intranet, Extranet
- Network topologies (physical vs logical, client-server vs peer-to-peer)
- Network devices:
  - ✅ [1.1.a — Routers](./CCNA_Chapter_1.1a_Routers.md)
  - ✅ [1.1.b — Layer 2 and Layer 3 Switches](./CCNA_Chapter_1.1b_Switches.md)
  - ⬜ 1.1.c — Access Points
  - ⬜ 1.1.d — Firewalls
  - ⬜ 1.1.e — Wireless LAN Controllers
  - ⬜ 1.1.f — Load Balancers
- ⬜ Network media (copper, fiber, wireless)

### Module 2 – Network Models
- ⬜ OSI Model (purpose, seven layers, functions of each layer)
- ⬜ Encapsulation / decapsulation, PDUs
- ⬜ TCP/IP Model (four layers, comparison to OSI)

### Module 3 – Ethernet Fundamentals
- ⬜ Ethernet history, MAC addresses, frames
- ⬜ Collision domains, broadcast domains
- ⬜ Duplex, speed negotiation, Auto-MDIX

### Module 4 – IPv4 Addressing
- ⬜ Binary numbers, decimal conversion
- ⬜ IP address structure (network vs host portion)
- ⬜ Classes (historical), private/public addresses, APIPA, loopback, multicast, broadcast, network ID

### Module 5 – Subnetting
- ⬜ CIDR, prefix notation, wildcard masks
- ⬜ VLSM, network/host calculations, route summarization, practice subnetting

### Module 6 – IPv6
- ⬜ Why IPv6, structure, hexadecimal, prefix length
- ⬜ Link-local, global unicast, unique local, multicast, anycast
- ⬜ SLAAC, EUI-64, Neighbor Discovery

### Module 7 – Cabling
- ⬜ UTP categories, fiber types, connectors
- ⬜ Straight-through, crossover, console cable, SFP modules

---

## 📘 Part 2 – Network Access (20%)

### Module 8 – Switching Fundamentals
- ⬜ Switch operation, CAM table, frame forwarding, MAC learning, flooding, unknown unicast *(builds on 1.1.b)*

### Module 9 – VLANs
- ⬜ Purpose, default/native/voice/data VLANs
- ⬜ VLAN configuration and troubleshooting

### Module 10 – Trunking
- ⬜ 802.1Q, native VLAN, allowed VLANs, tagging
- ⬜ Trunk negotiation, verification commands

### Module 11 – Inter-VLAN Routing
- ⬜ Router-on-a-stick, Layer 3 switch, SVIs
- ⬜ Configuration and troubleshooting

### Module 12 – Spanning Tree Protocol
- ⬜ Layer 2 loops, STP operation
- ⬜ Root bridge, root port, designated port, blocking states
- ⬜ Rapid STP, PortFast, BPDU Guard, Root Guard

### Module 13 – EtherChannel
- ⬜ Purpose, static, PAgP, LACP
- ⬜ Configuration and verification

### Module 14 – Wireless Fundamentals
- ⬜ Wireless standards, SSIDs, channels, interference, roaming
- ⬜ WPA2, WPA3, authentication, wireless architectures

---

## 📙 Part 3 – IP Connectivity (25%)

### Module 15 – Routing Fundamentals
- ⬜ Static routes, default routes, administrative distance
- ⬜ Routing tables, longest prefix match *(builds on 1.1.a)*

### Module 16 – OSPFv2
- ⬜ Areas, router IDs, neighbor relationships, hello packets
- ⬜ DR/BDR, route calculation, single-area OSPF, verification

### Module 17 – First Hop Redundancy
- ⬜ HSRP, VRRP, GLBP
- ⬜ Election process, failover

---

## 📕 Part 4 – IP Services (10%)

### Module 18 – DHCP
- ⬜ DORA process, relay agents, pools, exclusions
- ⬜ Configuration and troubleshooting

### Module 19 – DNS
- ⬜ Name resolution, recursive lookup, records, forward/reverse lookup

### Module 20 – NAT
- ⬜ Static NAT, dynamic NAT, PAT/overload
- ⬜ Configuration and verification

### Module 21 – NTP
- ⬜ Time synchronization, stratum, client/server

### Module 22 – SNMP
- ⬜ Monitoring, communities, versions, traps

### Module 23 – Syslog
- ⬜ Logging levels, remote logging, severity

### Module 24 – QoS
- ⬜ Congestion, classification, marking, queuing, trust boundaries

---

## 📔 Part 5 – Security Fundamentals (15%)

### Module 25 – Security Concepts
- ⬜ CIA triad, AAA (authentication, authorization, accounting)

### Module 26 – Device Security
- ⬜ Secure passwords, SSH, disable Telnet, local users, login banners, password encryption

### Module 27 – Layer 2 Security
- ⬜ Port Security, Sticky MAC
- ⬜ DHCP Snooping, Dynamic ARP Inspection, IP Source Guard

### Module 28 – ACLs
- ⬜ Standard vs extended, numbered vs named, placement, troubleshooting

### Module 29 – VPN Concepts
- ⬜ IPSec, site-to-site, remote access, GRE overview

---

## 📓 Part 6 – Automation and Programmability (10%)

### Module 30 – Modern Networks
- ⬜ Traditional networking, controller-based networking, SDN, intent-based networking

### Module 31 – APIs
- ⬜ REST, RESTCONF, JSON, XML, HTTP methods

### Module 32 – Configuration Management
- ⬜ Puppet, Chef, Ansible, Terraform overview

### Module 33 – Cisco DNA Center
- ⬜ Purpose, architecture, provisioning, assurance, policy

### Module 34 – AI and Machine Learning in Networking
- ⬜ AI-assisted operations, predictive analytics, telemetry, automation use cases

### Module 35 – Virtualization
- ⬜ Virtual machines, containers, virtual networking, hypervisors

---

## 🗓️ Suggested Pacing

| Week(s) | Part | Modules |
|---|---|---|
| 1–2 | 📗 Network Fundamentals | 1–7 |
| 3–4 | 📘 Network Access | 8–14 |
| 5–6 | 📙 IP Connectivity | 15–17 |
| 7 | 📕 IP Services + 📔 Security Fundamentals | 18–29 |
| 8 | 📓 Automation & Programmability + full review, practice exams | 30–35 |

---

*Chapters are built one module (or sub-objective, like 1.1.a / 1.1.b) at a time in the same format: learning objectives, Packet Tracer activities, and a quick check for understanding. Tell me which module to write next and it'll be added — and linked — here.*
