# 🧠 VLSM (Variable Length Subnet Masking) — Complete Notes (Interview + Practice Ready)

---

# 🚀 What is VLSM?

**VLSM = Variable Length Subnet Masking**

👉 It means:

> Dividing a network into subnets of **different sizes based on requirement**

---

# ❌ Without VLSM

* All subnets same size
* Huge IP wastage

# ✅ With VLSM

* Subnets sized based on need
* Efficient IP usage
* Used in real networks

---

# 🧠 Core Idea (Golden Line)

> “Allocate biggest subnet first, then move forward without overlap.”

---

# 📦 Basic Concepts Required

## 🔢 Total IP Formula

Total IPs = 2^(32 − CIDR)

---

## 🧮 Usable Hosts Formula

2^h − 2 ≥ required hosts

(h = number of host bits)

---

# 📊 Must-Know Table (MEMORIZE)

| CIDR | Block Size | Usable Hosts |
| ---- | ---------- | ------------ |
| /25  | 128        | 126          |
| /26  | 64         | 62           |
| /27  | 32         | 30           |
| /28  | 16         | 14           |
| /29  | 8          | 6            |
| /30  | 4          | 2            |

---

# ⚡ Block Size Trick

Block Size = 256 − Subnet Mask Value

Example:

* /26 → 255.255.255.192
* Block size = 64

---

# 🔥 Step-by-Step Process (VERY IMPORTANT)

## Step 1: Sort Hosts (Descending)

Biggest requirement first

---

## Step 2: Find CIDR for Each

Use:
2^h − 2 ≥ hosts

👉 Always choose **smallest valid subnet**

---

## Step 3: Allocate Subnets

* Start from lowest IP
* Assign block
* Move pointer forward

---

## Step 4: Repeat

Until all hosts are assigned

---

# 🧠 Important Rules

* Always allocate largest subnet first
* Never overlap ranges
* Always choose smallest valid subnet
* Move sequentially (no jumping randomly)

---

# 🚨 Interview Trap (VERY IMPORTANT)

Before solving:

👉 Check:
Total required IPs ≤ available IPs

Example:

* /24 → 256 IPs
* Required → 292 ❌ → Not possible

---

# 🧪 EXAMPLE 1 (Basic)

Network: 192.168.10.0/24
Hosts: 60, 30, 12, 5

---

## CIDR:

* 60 → /25
* 30 → /27
* 12 → /28
* 5  → /29

---

## Allocation:

| Hosts | Network        | Broadcast | Usable    |
| ----- | -------------- | --------- | --------- |
| 60    | 192.168.10.0   | .127      | .1–.126   |
| 30    | 192.168.10.128 | .159      | .129–.158 |
| 12    | 192.168.10.160 | .175      | .161–.174 |
| 5     | 192.168.10.176 | .183      | .177–.182 |

---

# 🧪 EXAMPLE 2 (Medium)

Network: 172.16.0.0/24
Hosts: 80, 40, 20, 10, 5

---

## CIDR:

* 80 → /25
* 40 → /26
* 20 → /27
* 10 → /28
* 5  → /29

---

## Allocation:

* 172.16.0.0 → /25
* 172.16.0.128 → /26
* 172.16.0.192 → /27
* 172.16.0.224 → /28
* 172.16.0.240 → /29

---

# 🧪 EXAMPLE 3 (Tricky — Avoid Waste)

Network: 192.168.50.0/24
Hosts: 70, 25, 25, 10, 2

---

## ❌ Common Mistakes:

* 25 → /26 ❌ (waste)
* 2 → /29 ❌ (wrong)

---

## ✅ Correct CIDR:

* 70 → /25
* 25 → /27
* 25 → /27
* 10 → /28
* 2  → /30

---

## Allocation:

* 192.168.50.0 → /25
* 192.168.50.128 → /27
* 192.168.50.160 → /27
* 192.168.50.192 → /28
* 192.168.50.208 → /30

---

# 🧪 EXAMPLE 4 (Advanced)

Network: 10.0.0.0/24
Hosts: 120, 60, 30, 12, 6

---

## CIDR:

* 120 → /25
* 60 → /26
* 30 → /27
* 12 → /28
* 6  → /29

---

## Allocation:

* 10.0.0.0 → /25
* 10.0.0.128 → /26
* 10.0.0.192 → /27
* 10.0.0.224 → /28
* 10.0.0.240 → /29

---

# 🧪 EXAMPLE 5 (INTERVIEW TRAP)

Network: 192.168.1.0/24
Hosts: 100, 50, 50, 20, 2

---

## Required IPs:

* /25 → 128
* /26 → 64
* /26 → 64
* /27 → 32
* /30 → 4

Total = 292 ❌

---

## ❌ Not Possible in /24

👉 Solution:
Use **/23 (512 IPs)**

---

# ⚡ Speed Tricks (VERY IMPORTANT)

## 1. Memorize CIDR → Hosts

| CIDR | Hosts |
| ---- | ----- |
| /25  | 126   |
| /26  | 62    |
| /27  | 30    |
| /28  | 14    |
| /29  | 6     |
| /30  | 2     |

---

## 2. Memorize Jumps

| CIDR | Jump |
| ---- | ---- |
| /25  | +128 |
| /26  | +64  |
| /27  | +32  |
| /28  | +16  |
| /29  | +8   |
| /30  | +4   |

---

# 🧠 Mental Model

Think like this:

👉 “I have a big block → I cut largest piece → move forward → repeat”

---

# 🎯 Interview Answer Style

Say:

> “I’ll sort requirements, assign smallest possible subnet, and allocate sequentially to avoid overlap.”

---


