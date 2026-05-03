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

```text
192.168.1.10
```

* IPv4 = 32 bits
* Divided into 4 octets (0–255)
* Each octet = 8 bits

---

# 🧩 Structure of IP Address

Every IP has 2 parts:

```text
[ Network Part | Host Part ]
```

Example:

```text
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
| Changes per hop | ❌ No       | ✅ Yes          |

---

# 🧠 Key Insight

> IP = final destination
> MAC = next hop

---

# 🔍 ARP (Address Resolution Protocol)

Used to map:

```text
IP → MAC
```

Example:

```text
Who has 192.168.1.1?
```

Router replies with its MAC.

---

# 📏 Subnet Mask (Very Important)

> Defines where network part ends and host part begins

Example:

```text
255.255.255.0 = /24
```

Binary:

```text
11111111.11111111.11111111.00000000
```

* 1s → network bits
* 0s → host bits

---

# 🧠 CIDR Notation

```text
/n → n bits are network bits
```

Total bits = 32

```text
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

# 🧠 Local vs Remote Decision

Device compares:

```text
My Network vs Destination Network
```

---

## ✅ Same Network

* Direct communication
* Use destination MAC

---

## ❌ Different Network

* Send to router
* Use router MAC

---

# 🧪 Example

Your IP:

```text
192.168.1.5/24
```

Destination:

```text
192.168.2.8
```

Compare:

```text
192.168.1 ≠ 192.168.2
```

👉 **Remote (send to router)**

---

# ⚠️ Important Insight

> Same IPs can be local or remote depending on subnet mask

Example:

| CIDR                         | Result |
| ---------------------------- | ------ |
| /24 → 192.168.1 vs 192.168.2 | Remote |
| /16 → 192.168 vs 192.168     | Local  |

---

# 📦 Host Calculation

```text
Total addresses = 2^(host bits)
Usable hosts = 2^(host bits) - 2
```

(-2 for network + broadcast)

---

# 🧪 Example

Given:

```text
192.168.1.0/26
```

* Host bits = 6
* Total = 2⁶ = 64
* Usable = 62

---

# 🔥 Key Rules (Must Remember)

* /n → network bits
* 32 - n → host bits
* Smaller CIDR → larger network
* Subnet mask defines boundary
* Same subnet → direct
* Different subnet → router

---

