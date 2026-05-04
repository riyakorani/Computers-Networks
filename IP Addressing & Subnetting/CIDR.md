# 🧠 CIDR Aggregation (Supernetting) — Complete Notes (GitHub Ready)

---

# 🚀 What is CIDR?

**CIDR = Classless Inter-Domain Routing**

👉 It allows:

> **Combining multiple smaller networks into one larger network**

---

# 🌐 Why CIDR is Used?

Without CIDR:

* Large routing tables ❌
* Slower routing ❌

With CIDR:

* Fewer routes ✅
* Faster routing ✅
* Efficient network management ✅

---

# 🔥 Core Idea

> Combine networks only if they are:

1. **Continuous**
2. **Power of 2 in count**
3. **Properly aligned**

---

# 📦 Basic Concept

If you combine:

| Networks   | Result |
| ---------- | ------ |
| 2 networks | /23    |
| 4 networks | /22    |
| 8 networks | /21    |

---

# 🧠 Formula

If:

* Number of networks = 2ⁿ

Then:

* New CIDR = Old CIDR − n

---

# ⚡ Step-by-Step Method

## Step 1: Check Continuity

Networks must be sequential

✔️ Example:
192.168.0.0, 1.0, 2.0, 3.0

❌ Example:
192.168.0.0, 2.0, 3.0

---

## Step 2: Count Networks

Must be power of 2

✔️ 2, 4, 8
❌ 3, 5

---

## Step 3: Check Alignment (VERY IMPORTANT)

> Starting network must be divisible by group size

---

## Step 4: Calculate New CIDR

/24 − n

---

# 🧪 EXAMPLES

---

## 🧪 Example 1 (Basic)

Combine:

* 192.168.0.0/24
* 192.168.1.0/24

✔️ Continuous
✔️ Count = 2

👉 New CIDR = /23

✅ **Answer: 192.168.0.0/23**

---

## 🧪 Example 2

Combine:

* 192.168.4.0/24
* 192.168.5.0/24

✔️ Continuous
✔️ Count = 2

👉 Answer: **192.168.4.0/23**

---

## 🧪 Example 3 (4 Networks)

Combine:

* 192.168.0.0/24
* 192.168.1.0/24
* 192.168.2.0/24
* 192.168.3.0/24

✔️ Continuous
✔️ Count = 4

👉 /24 − 2 = /22

✅ **Answer: 192.168.0.0/22**

---

## 🧪 Example 4 (Alignment Trap)

Combine:

* 192.168.10.0/24
* 192.168.11.0/24
* 192.168.12.0/24
* 192.168.13.0/24

✔️ Continuous
✔️ Count = 4

❌ Start = 10 (not divisible by 4)

---

### ❌ Cannot combine into /22

---

### ✅ Best Possible Aggregation:

* 10 & 11 → **192.168.10.0/23**
* 12 & 13 → **192.168.12.0/23**

---

## 🧪 Example 5 (8 Networks)

Combine:

* 10.0.0.0/24 → 10.0.7.0/24

✔️ Continuous
✔️ Count = 8

👉 /24 − 3 = /21

✅ **Answer: 10.0.0.0/21**

---

## 🧪 Example 6 (Mixed Case)

Combine:

* 192.168.6.0/24
* 192.168.7.0/24
* 192.168.8.0/24
* 192.168.9.0/24

✔️ Continuous
✔️ Count = 4

❌ Start = 6 (not divisible by 4)

---

### ❌ Full aggregation not possible

---

### ✅ Best Grouping:

* 6 & 7 → **192.168.6.0/23**
* 8 & 9 → **192.168.8.0/23**

---

## 🧪 Example 7 (Advanced)

Combine:

* 10.0.4.0/24
* 10.0.5.0/24
* 10.0.6.0/24
* 10.0.7.0/24
* 10.0.8.0/24
* 10.0.9.0/24

---

### Step 1: Check full aggregation

Count = 6 ❌ (not power of 2)

---

### Step 2: Best grouping

* 4–7 → ✔️ (4 networks) → **10.0.4.0/22**
* 8–9 → ✔️ (2 networks) → **10.0.8.0/23**

---

### ✅ Final Answer:

* 10.0.4.0/22
* 10.0.8.0/23

---

# ⚠️ Common Mistakes

❌ Ignoring alignment
❌ Combining non-contiguous networks
❌ Using non-power-of-2 groups
❌ Stopping when full aggregation fails

---

# 🧠 Mental Model

Think like:

> “Group in powers of 2, check alignment, combine, repeat”

---

# ⚡ Quick Shortcut

* 2 networks → /23
* 4 networks → /22
* 8 networks → /21

---

# 🎯 Interview Answer Style

> “These networks are continuous and form a power-of-2 group. The starting address is aligned, so they can be aggregated into a /X network.”

---

# 🚀 Final Skills You Gained

You can:

* Perform CIDR aggregation
* Detect invalid combinations
* Apply alignment logic
* Find optimal grouping

---

