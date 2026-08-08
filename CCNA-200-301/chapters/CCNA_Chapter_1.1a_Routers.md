# 🌐 Chapter 1.1.a — Routers
### 📘 Domain 1.0 Network Fundamentals | 🎯 Objective: Explain the role and function of network components

---

## 🎓 Learning Objectives

By the end of this chapter, you will be able to:

1. 🧭 **Describe** the primary role of a router in a network and how it differs from a switch or access point.
2. 🔀 **Explain** how a router makes forwarding decisions using the routing table.
3. ⚙️ **Identify** the key components inside a router (control plane vs. data plane) and how they interact.
4. 🏷️ **Recognize** common router roles in a topology (edge/gateway router, internal router).
5. 🔍 **Interpret** basic router `show` command output to describe what a router is doing.

---

## 💡 Core Concept: What Does a Router Actually Do?

A router's job is simple to state and deep to master: **it moves packets between different networks (different subnets/broadcast domains) by making a Layer 3 forwarding decision for every packet it receives.**

Contrast this with the other components you'll study in Domain 1:

| 🖥️ Device | 📶 Primary Layer | 🎯 Primary Job |
|---|---|---|
| 🔁 Switch | Layer 2 | Forwards frames within a single network/VLAN using MAC addresses |
| 📡 Access Point | Layer 1/2 | Bridges wireless clients into the wired LAN |
| **🌐 Router** | **Layer 3** | **Forwards packets between different networks using IP addresses** |
| 🛡️ Firewall | Layer 3/4 (+) | Enforces security policy on traffic crossing a boundary |

A router is, at heart, a device with **multiple interfaces on different subnets** whose job is to answer one question, over and over, for every packet: *"Based on the destination IP address, which interface (and next hop) should I send this out of?"*

### 📋 The Routing Table

Every router builds and maintains a **routing table** — the definitive list of known destination networks and how to reach them. Entries in the table come from three main sources:

- 🔗 **Directly connected networks** — subnets on the router's own interfaces.
- ✍️ **Static routes** — routes manually configured by an administrator.
- 🔄 **Dynamic routing protocols** — routes learned automatically (e.g., OSPF, which you'll cover in Domain 3).

For every incoming packet, the router performs a **longest-match lookup** against the routing table to pick the most specific matching route, then forwards the packet out the associated interface toward the next hop (or directly to the destination if it's on a connected network).

### 🧠 Control Plane vs. 🚚 Data Plane

This distinction shows up repeatedly across the CCNA, so it's worth locking in here:

- 🧠 **Control plane** — the "thinking" part of the router: building the routing table, running routing protocols, processing ARP. This is CPU-intensive and relatively slow.
- 🚚 **Data plane** (a.k.a. forwarding plane) — the "doing" part: actually moving packets in and out of interfaces based on decisions the control plane already made. This is optimized for speed, often in hardware (ASICs) on higher-end platforms.

> 🗺️ A useful mental model: the control plane **builds the map**; the data plane **drives the route**.

### 🏢 Common Router Roles

- 🚪 **Edge/gateway router** — sits at the boundary of your network, typically connecting to an ISP or another autonomous network. Often the point where NAT and default routes live.
- 🏬 **Internal/distribution router** — routes between internal subnets (e.g., between VLANs, or between sites over WAN links), often exchanging routes dynamically with OSPF.

You'll see both roles referenced throughout later domains — IP Connectivity (3.0) is essentially "everything a router does with that routing table," and IP Services (4.0) covers services (NAT, DHCP relay) that commonly live on edge routers.

---

## 🧪 Activity 1: Trace a Packet's Path — Deep Dive

**🎯 Goal:** Build a detailed, teachable model of what "routing" means, end to end, before you touch configuration syntax.

Work through this scenario in writing, step by step, filling in every detail — this is the kind of reasoning the exam expects you to do instantly:

**Setup:** Two LANs — 192.168.1.0/24 (HostA, gateway 192.168.1.1) and 192.168.2.0/24 (HostB, gateway 192.168.2.1) — connected by a single router with one interface on each network. HostA sends a ping to HostB.

1. 🧭 **Gateway decision.** HostA compares HostB's IP to its own subnet mask and determines HostB is *not* on the local network. Explain why this means HostA must send the frame to its **default gateway** rather than directly to HostB, and where that gateway address comes from (static config or DHCP).
2. 🔎 **ARP resolution.** Before HostA can build a frame, it needs the *MAC address* of its default gateway, not HostB's MAC. Walk through the ARP request/reply exchange that resolves this, and explain why ARP only ever needs to resolve the *next hop's* MAC, never the final destination's, when the destination is remote.
3. 📦 **Encapsulation.** Describe the frame HostA sends: source MAC = HostA, destination MAC = router's interface, source IP = HostA, destination IP = HostB (the IP addresses stay the same end-to-end; only the MAC addresses change hop by hop).
4. 🌐 **Router receives the frame.** The router strips the Layer 2 frame header, exposing the IP packet, and performs a **longest-match lookup** on the destination IP (192.168.2.x) against its routing table. Explain what happens if no matching route exists (packet is dropped, and — if configured — an ICMP "destination unreachable" is sent back).
5. 🔁 **Re-encapsulation.** The router builds a *new* Layer 2 frame to send the packet out its 192.168.2.0/24 interface: source MAC = router's outbound interface, destination MAC = HostB (resolved via ARP if not already known), while the IP addresses remain unchanged. Explain why this MAC swap, repeated at every hop, is the mechanic that actually gets a packet across a multi-hop network even though the IP addresses never change.
6. ⏱️ **TTL.** Note that the router decrements the packet's IP Time-to-Live (TTL) by 1 before forwarding. Explain what TTL is protecting against, and what happens when it reaches 0.

**Extend it:** Now add a second router and a third LAN (192.168.3.0/24), so HostA's packet has to cross two routers to reach a host on the third LAN. Re-run steps 3–6 for the second hop, and explicitly explain why the *first* router doesn't need to know the full path to 192.168.3.0/24 — it only needs a route pointing to the *next* router as its next hop, which then makes its own independent longest-match decision. This "next hop, not full path" principle is the foundation for how dynamic routing protocols like OSPF (Domain 3) scale to large networks.

## 💻 Activity 2: Read Real Router Output (Packet Tracer)

**🎯 Goal:** Connect the routing table concept to what you'll actually see on the exam and in the field.

- 🖱️ In **Packet Tracer**, build a topology with two routers connected directly to each other, each with one LAN (switch + PCs) attached.
- ▶️ Run `show ip route` on each router and identify: which routes are marked `C` (connected), which are `L` (local), and confirm there are no dynamic routes yet since none are configured.
- ➕ Add a static route on one router pointing to the other router's LAN, then re-run `show ip route` and identify the new `S` entry. Explain in your own words why that entry appeared and what it tells the router to do.
- 🔎 Run `show ip interface brief` and practice correlating interface status (✅ up/up, ❌ down/down, 🚫 administratively down) with whether that interface's connected network appears in the routing table.

---

## ✅ Quick Check for Understanding

1. ❓ A router receives a packet. What information does it use to decide where to forward it?
2. ❓ What's the difference between the control plane and the data plane on a router?
3. ❓ True or false: a router can forward traffic between two devices on the *same* subnet.
4. ❓ What routing table entry type (in Cisco IOS output) represents a directly attached network?
5. ❓ Why does an edge/gateway router commonly need a default route?

<details>
<summary>💬 <strong>Answers</strong></summary>

1. 🎯 The **destination IP address** in the packet header, matched against the routing table via longest-match lookup.
2. 🧠🚚 The **control plane** builds the routing table and makes decisions (e.g., running routing protocols); the **data plane** actually forwards packets based on those decisions.
3. ❌ **False** — that's a switch's job. A router forwards between *different* networks; same-subnet traffic doesn't need to leave the local network to reach its destination.
4. 🔗 **`C`** (connected) — with `L` marking the router's own local interface address.
5. 🌍 Because it can't have a specific route for every possible destination on the internet — a default route (`0.0.0.0/0`) gives it a "send it here if nothing else matches" catch-all, typically pointing toward the ISP.

</details>

---

*➡️ Next chapter: [1.1.b — Layer 2 and Layer 3 switches](./CCNA_Chapter_1.1b_Switches.md)*
