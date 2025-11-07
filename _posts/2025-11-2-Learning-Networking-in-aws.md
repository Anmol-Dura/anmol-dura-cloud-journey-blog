---
layout: post
title: "Learning Networking in AWS"
date: 2025-11-02
tags: [aws, cloud, learning]
---

It has been a few weeks since I started learning about the **networking side of AWS** — the part that explains how IPs are organized using **CIDR (Classless Inter-Domain Routing)** blocks.  
In simple terms, a **CIDR block** is like a large pool of IP addresses, and **subnets** are smaller chunks carved out from that pool.

---

## 🌐 Understanding Subnetting

**Subnetting** is the process of dividing a large network into smaller, more manageable pieces.  
Every IP address has two parts:

- **Network portion:** identifies the network.
- **Host portion:** identifies a specific device (or host) within that network.

Think of it like an apartment complex:

- The **network portion** is the building address.
- The **host portion** is the apartment number.

---

## 🤔 Why Not Just Use Host IPs for Everything?

Imagine you have a bunch of computers connected through a switch.  
When one computer wants to find another, it sends a **broadcast message**:

> “Who has IP `195.195.195.0`?”

Every device on the network hears that broadcast and replies “Not me,” except for the correct one.  
This happens **every time**, causing unnecessary traffic and chaos — especially in large networks.

To fix this, we divide the network into smaller **subnets**.  
This keeps each subnet’s broadcast traffic local, making communication **faster and more efficient**.

---

<div style="margin:0; padding:2rem; font-family:Arial, sans-serif; background:#0b0c10; color:#e8e8e8; text-align:center;">
<h2 style="color:#7c5cff;">🧩 Simple Personal Company Network</h2>

<svg width="700" height="400" style="background:#111317; border-radius:12px; box-shadow:0 0 20px rgba(0,0,0,0.4); margin:2rem auto; display:block; max-width:800px;">
  <ellipse cx="350" cy="50" rx="90" ry="35" fill="#444" stroke="#888" stroke-width="2"/>
  <text x="320" y="55" fill="#fff">Internet</text>
  <rect x="300" y="120" width="100" height="40" rx="6" ry="6" fill="#222" stroke="#7c5cff" stroke-width="2"/>
  <text x="325" y="145" fill="#fff">Router</text>
  <rect x="300" y="200" width="100" height="40" rx="6" ry="6" fill="#222" stroke="#00c896" stroke-width="2"/>
  <text x="325" y="225" fill="#fff">Switch</text>
  <rect x="150" y="280" width="80" height="40" rx="6" ry="6" fill="#222" stroke="#fff" stroke-width="1.5"/>
  <text x="160" y="305" fill="#fff">Laptop</text>
  <rect x="310" y="280" width="80" height="40" rx="6" ry="6" fill="#222" stroke="#fff" stroke-width="1.5"/>
  <text x="320" y="305" fill="#fff">Desktop</text>
  <rect x="470" y="280" width="80" height="40" rx="6" ry="6" fill="#222" stroke="#fff" stroke-width="1.5"/>
  <text x="485" y="305" fill="#fff">Printer</text>
  <line x1="350" y1="85" x2="350" y2="120" stroke="#888" stroke-width="2" stroke-dasharray="4 2"/>
  <line x1="350" y1="160" x2="350" y2="200" stroke="#7c5cff" stroke-width="2"/>
  <line x1="340" y1="240" x2="190" y2="280" stroke="#00c896" stroke-width="2"/>
  <line x1="350" y1="240" x2="350" y2="280" stroke="#00c896" stroke-width="2"/>
  <line x1="360" y1="240" x2="510" y2="280" stroke="#00c896" stroke-width="2"/>
</svg>
</div>

---

## 🧮 How Subnetting Actually Works

Let’s start with an example:

**Network:** `192.168.1.0/24`  
**Subnet Mask:** `255.255.255.0`  
**Binary Form:** `11111111.11111111.11111111.00000000`

Here:

- The **first 24 bits** (`11111111.11111111.11111111`) represent the **network**.
- The **last 8 bits** (`00000000`) represent the **hosts**.

That means:

- Network range → `192.168.1.0 – 192.168.1.255`
- Usable hosts → `254` (since `.0` is the network and `.255` is the broadcast)

---

## ✂️ Borrowing Bits (Making Smaller Networks)

When we **borrow bits** from the host portion, we create **more networks** but **fewer hosts per network**.

| Borrowed Bits | New Prefix | New Mask        | Subnets Created | Hosts per Subnet |
| ------------- | ---------- | --------------- | --------------- | ---------------- |
| 1             | /25        | 255.255.255.128 | 2               | 126              |
| 2             | /26        | 255.255.255.192 | 4               | 62               |
| 3             | /27        | 255.255.255.224 | 8               | 30               |
| 4             | /28        | 255.255.255.240 | 16              | 14               |

---

### Example 1 – Borrowing 1 Bit
