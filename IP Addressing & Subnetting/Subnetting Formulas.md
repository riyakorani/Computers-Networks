# 🧠 Subnetting Formulas Cheat Sheet (FAANG-Level)

> You don’t need more formulas — you need the right ones + when to use them.

---

## 🔢 1. Total IP Addresses

**Formula:**
```
Total Addresses = 2^(32 - n)
```

- `n = CIDR`

**Example:**
```
/26 → 2^(32-26) = 2^6 = 64
```

---

## 👥 2. Usable Hosts

**Formula:**
```
Usable Hosts = 2^(32 - n) - 2
```

👉 Why `-2`?

- 1 for **Network Address**
- 1 for **Broadcast Address**

**Example:**
```
/26 → 64 - 2 = 62 usable
```

---

## 🧱 3. Block Size (MOST IMPORTANT)

**Formula:**
```
Block Size = 256 - Subnet Mask (last octet)
```

**Example:**
```
/26 → mask = 255.255.255.192
Block size = 256 - 192 = 64
```

👉 Subnet jumps:
```
0, 64, 128, 192
```

---

## 📊 4. Number of Subnets

**Formula:**
```
Subnets = 2^(new CIDR - old CIDR)
```

**Example:**
```
/24 → /26
Borrowed bits = 26 - 24 = 2
Subnets = 2^2 = 4
```

---

## 🧠 5. Host Bits

**Formula:**
```
Host Bits = 32 - n
```

**Example:**
```
/20 → 32 - 20 = 12 host bits
```

---

## 🌐 6. Subnet Mask Conversion (CIDR → Decimal)

👉 Rule:
- Every 8 bits = 255

👉 Partial octet values:

| Bits  | Value |
|---------|
| 1 | 128 |
| 2 | 192 |
| 3 | 224 |
| 4 | 240 |
| 5 | 248 |
| 6 | 252 |
| 7 | 254 |
| 8 | 255 |

**Examples:**
```
/20 → 255.255.240.0
/18 → 255.255.192.0
```

---

## 🎯 7. Network, Broadcast, Range

👉 No formula needed — just rules:

- **Network Address** = First IP  
- **Broadcast Address** = Last IP  
- **Usable Range** = Between them  

**Example (/26 → block size 64):**
```
Subnet: 64–127

Network   = 192.168.1.64
Broadcast = 192.168.1.127
Usable    = 192.168.1.65 – 192.168.1.126
```

---

## ⚡ 8. Fast Mental Patterns (INTERVIEW GOLD)

| CIDR | Block Size | Pattern |
|------|----------- |-------- |
| /25  | 128        | 2subnet |
| /26  |  64        | 4subnet |
| /27  | 32         | 8 subnet|
| /28  | 16         | 16subnet|

👉 Think:
```
/26 → jump by 64
/27 → jump by 32
```

---

## 🔥 9. Design Rule (Real-World)

👉 Choose subnet based on requirement:

```
Required hosts ≤ Usable hosts
```

**Example:**
```
Need 50 devices

/27 → 30 ❌
/26 → 62 ✅
```

👉 Final answer: `/26`

---

## 🧠 10. Golden Rules (Must Remember)

- Subnets start at **multiples of block size**
- First IP = **Network**
- Last IP = **Broadcast**
- Never create random ranges ❌
- Always: **Block → Range → Answer**

---

## 🚀 Final Insight (FAANG Thinking)

Subnetting is NOT about formulas.

👉 It’s about:
- Pattern recognition  
- Range spotting  
- Fast decision making  