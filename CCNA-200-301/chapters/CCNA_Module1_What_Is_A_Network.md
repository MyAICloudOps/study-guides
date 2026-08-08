# 🌐 Module 1 — What Is a Network?
### 📘 Domain 1.0 Network Fundamentals | 🎯 Foundational concept before objective 1.1

---

## 🎓 Learning Objectives

By the end of this chapter, you will be able to:

1. 🧩 **Define** what a network is and identify its core purpose.
2. 🏢🌍 **Distinguish** between a LAN and a WAN based on scope and ownership.
3. 🔐 **Differentiate** an Internet, Intranet, and Extranet by who can access them.
4. 🕸️ **Compare** physical and logical topology, and explain why a network can have one of each simultaneously.
5. 🤝 **Compare** client-server and peer-to-peer network architectures and identify appropriate use cases for each.

---

## 💡 Core Concept: What Is a Network?

At its simplest: **a network is a collection of devices connected together so they can share resources and communicate.** Those resources might be files, printers, internet access, or applications — but the underlying goal is always the same: let devices exchange data reliably.

Every network, no matter how large or small, is built from the same basic ingredients:

- 🖥️ **End devices** — the things generating or consuming data (PCs, phones, servers, printers, IoT devices).
- 🔁🌐 **Intermediary devices** — the things moving data between end devices (switches, routers, access points, firewalls — covered in Module 1.1).
- 🔌 **Media** — the physical or wireless path data travels across (copper, fiber, radio waves — covered in Module 7).
- 📜 **Protocols/rules** — the agreed-upon "language" devices use to communicate (you'll formalize this with the OSI and TCP/IP models in Module 2).

### 🏢 LAN vs 🌍 WAN

The single biggest factor that separates these two is **geographic scope and who owns the connection** — not just physical distance.

| | 🏢 LAN (Local Area Network) | 🌍 WAN (Wide Area Network) |
|---|---|---|
| **Scope** | A single site: a home, office, building, or campus | Connects multiple sites across cities, countries, or continents |
| **Ownership** | Typically owned and fully controlled by the organization | Typically leased from or provided by a service provider (ISP/telco) |
| **Speed** | Generally high bandwidth, low cost per bit | Generally lower bandwidth relative to cost, since it spans provider infrastructure |
| **Example** | The switches and cabling inside one office building | The link connecting that office to a branch office in another city |

A useful exam heuristic: **if you own and can walk to every piece of cable, it's probably a LAN; if a provider's infrastructure carries your traffic between distant sites, it's a WAN.**

### 🔐 Internet vs Intranet vs Extranet

These terms describe **scope of access**, not a different type of underlying technology — all three typically run on the same IP-based networking you're learning throughout this guide.

- 🌐 **Internet** — the global, public network of networks. Open to anyone with a connection; not owned by any single entity.
- 🔒 **Intranet** — a private network, built with the same technologies as the internet, restricted to an organization's own members (employees, students, etc.). Think of it as "the internet, but walled off for us only."
- 🤝 **Extranet** — an intranet that has been selectively extended to include specific trusted outsiders — vendors, partners, or contractors — usually for a defined purpose, without opening it up to the public.

A good way to keep these straight: **Intranet = us only. Extranet = us + specific trusted partners. Internet = everyone.**

### 🕸️ Physical vs Logical Topology

A **topology** describes how a network's pieces are arranged. Every network actually has *two* topologies layered on top of each other:

- 🔌 **Physical topology** — how devices are *actually cabled/connected* in the real world (which port plugs into which port, how cables physically run).
- 🗺️ **Logical topology** — how data *actually flows* across the network, independent of the physical wiring (for example, which devices are grouped in the same broadcast domain/VLAN).

A classic example: a modern switched network is almost always **physically** a star (every device cabled to a central switch), but its **logical** topology depends on configuration — VLANs can make devices behave as if they're on entirely separate networks, even when they're physically plugged into the same switch. This distinction matters a lot once you reach VLANs (Module 9) — the cabling won't change, but the logical grouping will.

### 🤝 Client-Server vs Peer-to-Peer

This describes **how resources are shared** on a network:

- 🖥️➡️🗄️ **Client-server** — dedicated servers provide resources (files, email, authentication, web pages) and clients request them. Centralized, easier to secure, scale, and back up — the model virtually all business networks use.
- 🔄 **Peer-to-peer (P2P)** — every device can act as both client and requester simultaneously; there's no dedicated server. Simple and cheap for small setups (e.g., a home network sharing a printer), but harder to secure and manage as it grows, since there's no central point of control.

---

## 🧪 Activity 1: Classify Your Own Network — Deep Dive

**🎯 Goal:** Apply every concept in this chapter to a network you already know, in writing, before moving to configuration.

Using your home or work network (or one you're familiar with), answer each of the following in detail:

1. 🏢🌍 **LAN or WAN?** Identify every LAN segment you can think of, and identify at least one WAN link connecting one of those LANs to somewhere else (e.g., your home LAN to your ISP). Justify each classification using ownership and scope, not just "it feels local."
2. 🔐 **Internet, Intranet, or Extranet?** Identify a resource you access that's purely public (Internet), one that's restricted to just you/your organization (Intranet), and — if applicable — one shared with an outside partner (Extranet). If you can't think of an Extranet example personally, research a real-world scenario where a company would use one (e.g., a supplier accessing an inventory system) and explain why an Extranet fits better than opening the resource to the full Internet.
3. 🕸️ **Physical vs logical topology.** Describe how your devices are physically cabled/connected (star via a router/switch, mesh, etc.), then describe the logical grouping of traffic (is everything on one flat network, or are there separate logical groups like a guest Wi-Fi network isolated from your main devices?). Explain in your own words why these two descriptions can differ even though the physical wiring hasn't changed.
4. 🤝 **Client-server or peer-to-peer?** Identify at least one client-server interaction (e.g., a laptop requesting a webpage from a server) and one peer-to-peer interaction if one exists on your network (e.g., two devices sharing a file directly, or a smart-home mesh). Explain what would need to change for a peer-to-peer setup to scale to hundreds of users, and why organizations default to client-server at that scale.

## 💻 Activity 2: Model Both Topologies (Packet Tracer)

**🎯 Goal:** See physical vs. logical topology as two distinct, coexisting layers on the same equipment.

- 🖱️ In **Packet Tracer**, build a single switch with four PCs connected — this is your **physical topology**, and it will look like a star no matter what you do logically.
- 🏷️ Configure two VLANs on the switch (e.g., VLAN 10 and VLAN 20) and assign two PCs to each — refer to Module 9 concepts loosely here; the goal right now is just to see the effect, not master the configuration syntax.
- 📨 Use the simple PDU tool to ping between two PCs in the *same* VLAN, then between two PCs in *different* VLANs. Observe that the ping succeeds within the same VLAN and fails across VLANs (with no routing configured), even though **every PC is physically cabled into the exact same switch**.
- ✍️ Write one or two sentences explaining, in your own words, why this experiment proves that physical topology and logical topology are separate things — the cabling (physical) never changed, but the traffic flow (logical) did.

---

## ✅ Quick Check for Understanding

1. ❓ What are the four basic ingredients present in every network?
2. ❓ What is the primary factor that distinguishes a LAN from a WAN — is it purely physical distance?
3. ❓ Put these in order from most restricted to most open: Internet, Intranet, Extranet.
4. ❓ Can a single switch host multiple different logical topologies at once? Why or why not?
5. ❓ Why might a growing organization migrate from a peer-to-peer setup to a client-server model?

<details>
<summary>💬 <strong>Answers</strong></summary>

1. 🧩 **End devices, intermediary devices, media, and protocols/rules.**
2. 🏢🌍 **Ownership and scope** — not just distance. A LAN is typically a single site under one organization's control; a WAN connects multiple sites, usually over provider-owned infrastructure. (Distance is a common byproduct of this, not the defining factor.)
3. 🔐 **Intranet → Extranet → Internet** (most restricted to most open).
4. 🕸️ **Yes** — through VLANs, a single physical switch can host multiple separate logical networks; the physical cabling (star topology) stays the same regardless of the logical grouping.
5. 🤝 Because peer-to-peer becomes hard to **secure, manage, and scale** without centralized control — client-server centralizes resources and administration, which is essential once user count and security requirements grow.

</details>

---

*➡️ Next: Module 1 continued — [Network Devices (1.1.a Routers)](./CCNA_Chapter_1.1a_Routers.md), or on to network topologies and remaining device types.*
