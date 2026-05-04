# 🔥 Reverse Subnetting — Complete Notes (GitHub Ready)

---

# 🧠 WHAT IS REVERSE SUBNETTING?

Reverse Subnetting means:

> Given **IP + CIDR → find**

* Network Address
* Broadcast Address
* Usable Range

---

# 🚀 WHY IMPORTANT?

* Very common in interviews
* Tests **speed + accuracy**
* Used in real networking scenarios

---

# ⚡ CORE METHOD (STEP-BY-STEP)

---

## 🔹 Step 1: Find Block Size

Formula:
Block Size = 256 − Subnet Mask Value

Examples:

| CIDR | Mask            | Block Size |
| ---- | --------------- | ---------- |
| /26  | 255.255.255.192 | 64         |
| /27  | 255.255.255.224 | 32         |
| /28  | 255.255.255.240 | 16         |
| /29  | 255.255.255.248 | 8          |
| /30  | 255.255.255.252 | 4          |

---

## 🔹 Step 2: Create Ranges

Example for /26 (block = 64):

* 0–63
* 64–127
* 128–191
* 192–255

---

## 🔹 Step 3: Locate IP in Range

Whichever range contains the IP → that is your subnet

---

## 🔹 Step 4: Final Answer

* Network = Start of range
* Broadcast = End of range
* Usable = (network + 1) → (broadcast − 1)

---

# 🧪 EXAMPLES

---

## 🧪 Example 1

IP: 192.168.1.77/26

### Step 1:

Block size = 64

### Step 2:

Ranges:

* 0–63
* 64–127 ✅

### ✅ Answer:

* Network: 192.168.1.64
* Broadcast: 192.168.1.127
* Usable: 192.168.1.65 – 192.168.1.126

---

## 🧪 Example 2

IP: 10.0.0.145/27

### Step 1:

Block size = 32

### Step 2:

Ranges:

* 128–159 ✅

### ✅ Answer:

* Network: 10.0.0.128
* Broadcast: 10.0.0.159
* Usable: 10.0.0.129 – 10.0.0.158

---

## 🧪 Example 3

IP: 172.16.5.200/28

### Step 1:

Block size = 16

### Step 2:

Ranges:

* 192–207 ✅

### ✅ Answer:

* Network: 172.16.5.192
* Broadcast: 172.16.5.207
* Usable: 172.16.5.193 – 172.16.5.206

---

## 🧪 Example 4

IP: 192.168.10.200/27

* Block = 32
* Range = 192–223

✅ Answer:

* Network: 192.168.10.192
* Broadcast: 192.168.10.223
* Usable: 192.168.10.193 – 192.168.10.222

---

## 🧪 Example 5

IP: 10.0.5.34/28

* Block = 16
* Range = 32–47

✅ Answer:

* Network: 10.0.5.32
* Broadcast: 10.0.5.47
* Usable: 10.0.5.33 – 10.0.5.46

---

## 🧪 Example 6 (Important Edge Case)

IP: 172.16.1.99/26

* Block = 64
* Range = 64–127

⚠️ Common mistake:
Starting usable from wrong value

✅ Correct Answer:

* Network: 172.16.1.64
* Broadcast: 172.16.1.127
* Usable: 172.16.1.65 – 172.16.1.126

---

# 🧠 GOLDEN RULE

> Usable Range = (Network + 1) → (Broadcast − 1)

---

# ⚡ SPEED TRICK (VERY IMPORTANT)

## Memorize Block Sizes

| CIDR | Block |
| ---- | ----- |
| /26  | 64    |
| /27  | 32    |
| /28  | 16    |
| /29  | 8     |
| /30  | 4     |

---

# 🚀 MENTAL SHORTCUT (NO RANGES NEEDED)

👉 Find:

> “Nearest multiple of block size BELOW the IP”

---

## Example:

IP = 145
Block = 32

Multiples:

* 128 ✔️
* 160 ❌

👉 Network = 128

---

# 🎯 INTERVIEW ANSWER STYLE

Say:

> “Block size is X. IP falls in this range, so network is Y and broadcast is Z.”

---

# ⚠️ COMMON MISTAKES

❌ Wrong block size
❌ Wrong range selection
❌ Forgetting +1 / −1
❌ Mixing CIDR values

---

# 🧠 MENTAL MODEL

Think like:

> “Find block → locate range → pick start & end”

---

# 🚀 FINAL SKILLS YOU GAINED

You can now:

* Solve reverse subnetting quickly
* Identify ranges mentally
* Avoid off-by-one mistakes
* Answer confidently in interviews

---

