# 🌍 IP Addressing & Subnetting (Core Networking)

---

# 🧠 First Principle

When sending data, two questions must be answered:

1. **Where should this go globally?** → IP Address
2. **Who should receive it locally?** → MAC Address

---

# 🌐 What is an IP Address?

> A logical address used to identify a device on a network

Example:

```
192.168.1.10
```

* IPv4 = 32 bits
* Divided into 4 octets (0–255)
* Each octet = 8 bits

---

# 🧩 Structure of IP Address

Every IP has 2 parts:

```
[ Network Part | Host Part ]
```

Example:

```
192.168.1 | 10
```

* Network → identifies the network
* Host → identifies the device

---

# 🔗 IP vs MAC Address

| Feature         | IP Address | MAC Address    |
| --------------- | ---------- | -------------- |
| Layer           | Network    | Data Link      |
| Scope           | Global     | Local          |
| Purpose         | Routing    | Local delivery |
| Changes per hop | ❌ No      |  ✅ Yes       |

---

# 🧠 Key Insight

> IP = final destination
> MAC = next hop

---

# 🔍 ARP (Address Resolution Protocol)

Used to map:

```
IP → MAC
```

Example:

```
Who has 192.168.1.1?
```

Router replies with its MAC.

---

# 📏 Subnet Mask (Very Important)

> Defines where network part ends and host part begins

Example:

```
255.255.255.0 = /24
```

Binary:

```
11111111.11111111.11111111.00000000
```

* 1s → network bits
* 0s → host bits

---

# 🧠 CIDR Notation

```
/n → n bits are network bits
```

Total bits = 32

```
Host bits = 32 - n
```

---

# 📊 Common CIDR Values

| CIDR | Subnet Mask     | Host Bits |
| ---- | --------------- | --------- |
| /8   | 255.0.0.0       | 24        |
| /16  | 255.255.0.0     | 16        |
| /24  | 255.255.255.0   | 8         |
| /26  | 255.255.255.192 | 6         |

---

# 🧠 CIDR to Subnet Mask (Deep Understanding)

---

## 🔍 Step 1: What does `/20` mean?

* First **20 bits = 1** → Network
* Remaining **12 bits = 0** → Host

---

## 🔢 Step 2: Write in Binary (8-bit groups)

```text
11111111.11111111.11110000.00000000
```

### Breakdown:

* First 8 bits → all 1s
* Next 8 bits → all 1s
* Next 4 bits → 1, remaining 4 bits → 0
* Last 8 bits → all 0s

---

## 🔄 Step 3: Convert to Decimal

### 1️⃣ First Octet

```text
11111111 = 255
```

### 2️⃣ Second Octet

```text
11111111 = 255
```

### 3️⃣ Third Octet

```text
11110000
```

👉 Calculation:

```text
128 + 64 + 32 + 16 = 240
```

### 4️⃣ Fourth Octet

```text
00000000 = 0
```

---

## ✅ Final Answer

```text
/20 = 255.255.240.0
```

---

# 🔥 Key Insight (VERY IMPORTANT)

> When CIDR is NOT a multiple of 8 → you get a **partial octet**

---

## 🧠 Shortcut Table (Memorize)

| Bits | Value |
| ---- | ----- |
| 1    | 128   |
| 2    | 192   |
| 3    | 224   |
| 4    | 240   |
| 5    | 248   |
| 6    | 252   |
| 7    | 254   |
| 8    | 255   |

---

## 🎯 Mental Model

* First fill full octets (8 bits each → 255)
* Remaining bits → use table

👉 For `/20`:

* 16 bits → `255.255`
* Next 4 bits → `240`

✔ Final:

```text
255.255.240.0
```

---

# 🧪 Quick Check

## ❓ What is `/18`?

👉 Hint:

* 16 bits → `255.255`
* Next 2 bits → ?

---

## ✅ Answer

```text
/18 = 255.255.192.0
```

👉 Because:

```text
11000000 = 128 + 64 = 192
```

---

# 🚀 Final Takeaway

CIDR → Subnet Mask is just:

* Fill **255s in blocks of 8 bits**
* Use **bit-value table for remaining bits**

---



# 🧠 Local vs Remote Decision

Device compares:

```
My Network vs Destination Network
```

### ✅ Same Network

* Direct communication
* Use destination MAC

### ❌ Different Network

* Send to router
* Use router MAC

---

# 🧪 Example

Your IP:

```
192.168.1.5/24
```

Destination:

```
192.168.2.8
```

👉 **Remote (send to router)**

---

# ⚠️ Important Insight

> Same IPs can be local or remote depending on subnet mask

| CIDR | Result |
| ---- | ------ |
| /24  | Remote |
| /16  | Local  |

---

# 📦 Host Calculation

```
Total addresses = 2^(host bits)
Usable hosts = 2^(host bits) - 2
```

---

# 🧪 Example

```
192.168.1.0/26
```

* Host bits = 6
* Total = 64
* Usable = 62

---

# 🔥 Subnetting Deep Dive (Interview Level)

---

## ⚡ Block Size (Shortcut)

```
Block Size = 256 - subnet mask (last octet)
```

For /26:

```
256 - 192 = 64
```

---

## 📦 Subnet Ranges (/26)

```
0–63
64–127
128–191
192–255
```

---

## 🎯 First Subnet

```
192.168.1.0/26
```

* Network Address → 192.168.1.0
* Broadcast Address → 192.168.1.63
* Valid Hosts → 192.168.1.1 – 192.168.1.62

---

## 🧠 Core Understanding

Each subnet = fixed block

* First → Network
* Last → Broadcast
* Middle → Usable

---

## ⚡ Fast Method

Example:

```
192.168.1.70/26
```

* Falls in → 64–127
* Network → 192.168.1.64
* Broadcast → 192.168.1.127
* Range → 65–126

---

# 🧠 Golden Rule

> Subnets ALWAYS start at multiples of block size

For /26:

```
0, 64, 128, 192
```

❌ Not allowed:

```
72, 80, 100
```

---

# 🏢 Real Scenario (Office Network)

Given:

```
192.168.1.0/24
```

Split into 4 departments:

```
0–63     (HR)
64–127   (Tech)
128–191  (Sales)
192–255  (Admin)
```

---

## Example Subnet

```
192.168.1.64 – 192.168.1.127
```

* Network → 192.168.1.64
* Broadcast → 192.168.1.127
* Usable → 192.168.1.65 – 192.168.1.126

---

# 🔥 Pattern Recognition (Important)

| CIDR | Meaning              |
| ---- | -------------------- |
| /25  | 2 subnets (128 each) |
| /26  | 4 subnets (64 each)  |
| /27  | 8 subnets (32 each)  |
| /28  | 16 subnets (16 each) |

---

# 🧪 Practice Examples

### 1️⃣ 192.168.1.130/26

* Subnet → 128–191
* Network → 192.168.1.128
* Broadcast → 192.168.1.191
* Range → 129–190

---

### 2️⃣ 192.168.1.75/26

* Subnet → 64–127
* Network → 192.168.1.64
* Broadcast → 192.168.1.127
* Range → 65–126

---

### 3️⃣ 10.0.5.130/25

* Subnet → 128–255
* Network → 10.0.5.128
* Broadcast → 10.0.5.255
* Range → 129–254

---

# 🧠 Subnet Calculation Rules

* Subnets = 2^(borrowed bits)
* Hosts = 2^(host bits) - 2

---

# 🧪 Example

```
/24 → /26
Borrowed bits = 2
Subnets = 2² = 4
```

---

# 🚀 Real-World Design Question

### Requirement:

👉 50 devices

| CIDR | Usable Hosts | Result       |
| ---- | ------------ | ------------ |
| /26  | 62           | ✅ Use this   |
| /27  | 30           | ❌ Not enough |
| /28  | 14           | ❌ Too small  |

---


# 🚀 Subnetting Trap: /19 (Interview-Level Insight)

---

## 🧪 Given

```text
192.168.1.150/19
```

---

## 🧠 Step 1: Understand `/19`

* Subnet mask → **255.255.224.0**
* Block size →

```text
256 - 224 = 32
```

---

## 📦 Step 2: Subnet Ranges (3rd Octet)

```text
0–31   32–63   64–95   96–127  
128–159   160–191   192–223   224–255
```

---

## 🔍 Step 3: Locate the IP

IP = **192.168.1.150**

👉 Focus on **third octet = 1**

✔ 1 lies in:

```text
0–31
```

---

## ❗ Important Correction

Many students incorrectly jump to:

👉 “150 → 128–159” ❌ (wrong octet)

But:

* /19 affects **third octet**, NOT the last
* So we must evaluate **third octet (1)**, not 150

---

## ✅ Final Answer

* **Subnet range (3rd octet)** → 0–31
* **Network address** → `192.168.0.0`
* **Broadcast address** → `192.168.31.255`
* **Usable range** → `192.168.0.1 – 192.168.31.254`

---

# 🔥 CRITICAL INSIGHT

> CIDR decides **which octet changes**

---

## 🧠 Mental Model

| CIDR Range | Changes In   |
| ---------- | ------------ |
| /24 – /32  | Last octet   |
| /16 – /23  | Third octet  |
| /8 – /15   | Second octet |

---

## ⚠️ Common Trap

❌ Thinking only last octet matters
✔ Actually depends on CIDR

---

# 🧠 Interview-Level Answer

> “/19 gives a block size of 32 in the third octet.
> The IP 192.168.1.150 falls in the 0–31 range of the third octet,
> so the network is 192.168.0.0 and broadcast is 192.168.31.255.”

---

# 🧪 Quick Check

## ❓ What is the network for:

```text
192.168.45.10/19
```

---

## 🧠 Solve

* Third octet = **45**
* Block size = **32**

Ranges:

```text
0–31   32–63   64–95 ...
```

👉 45 lies in:

```text
32–63
```

---

## ✅ Answer

* **Network** → `192.168.32.0`
* **Broadcast** → `192.168.63.255`
* **Usable** → `192.168.32.1 – 192.168.63.254`

---

# 🚀 Final Takeaway

Subnetting mistakes don’t come from math…

👉 They come from:

* Looking at the **wrong octet**
* Not understanding **where CIDR applies**

---




# 🧠 Engineering Insight

> Always choose the **smallest subnet that satisfies requirement**

---

# ⚠️ Common Mistakes

* Confusing /24 vs /16
* Forgetting -2
* Ignoring block size
* Guessing instead of pattern recognition

---

# 🚀 Final Takeaway

Subnetting is NOT about memorizing formulas.

👉 It’s about:

* Seeing patterns
* Understanding blocks
* Thinking in ranges

---
