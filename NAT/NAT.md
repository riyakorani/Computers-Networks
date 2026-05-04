# 🌐 NAT (Network Address Translation) — Complete Interview Notes

# 🧠 1. WHAT IS NAT?
NAT is a technique that translates private IP addresses into a public IP address.
👉 Multiple devices in a private network share one public IP to access the internet.

# 🏠 2. WHY NAT IS NEEDED?
❌ Problem:
- IPv4 addresses are limited
- Not every device can have a public IP

✅ Solution:
- Use private IP inside LAN
- Use one public IP for internet access

# 📦 3. HOW NAT WORKS

## Example:
Private IPs:
192.168.1.2
192.168.1.3
192.168.1.4

Public IP:
203.0.113.10

## Flow:
1. 192.168.1.2 → request to internet
2. NAT replaces IP → 203.0.113.10
3. Server responds to 203.0.113.10
4. NAT maps response back → 192.168.1.2



# 📦  HOW NAT WORKS

---

## 🧪 Example:

### Private Network:

192.168.1.2
192.168.1.3
192.168.1.4


### Public IP:

203.0.113.10


---

## 🔁 NAT Process:

### Step 1: Device sends request

192.168.1.2 → Google


---

### Step 2: NAT router replaces IP

203.0.113.10 → Google


---

### Step 3: Response comes back

Google → 203.0.113.10


---

### Step 4: NAT maps back to correct device

→ 192.168.1.2


---

# 🔥 4. TYPES OF NAT

## 1️⃣ Static NAT
One private IP ↔ One public IP (fixed mapping)

## 2️⃣ Dynamic NAT
Private IP mapped from pool of public IPs (temporary)

## 3️⃣ PAT (MOST IMPORTANT)
Many private IPs → One public IP using ports
Example:
192.168.1.2:5000 → 203.0.113.10:1
192.168.1.3:5001 → 203.0.113.10:2
👉 Also called NAT Overloading

# 🧠 5. PRIVATE IP RANGES
10.0.0.0 – 10.255.255.255
172.16.0.0 – 172.31.255.255
192.168.0.0 – 192.168.255.255

# 🌍 6. PUBLIC IP
👉 IP address reachable over the internet

# 📊 7. NAT TABLE
Stores mapping:
Private IP + Port → Public IP + Port

# 🚀 8. ADVANTAGES
✔ Saves IPv4 addresses
✔ Security (hides internal network)
✔ Multiple devices share one IP

# ❌ 9. DISADVANTAGES
❌ Slight delay due to translation
❌ Breaks end-to-end connectivity
❌ Difficult for peer-to-peer apps

# 🧠 10. INTERVIEW QUESTIONS

Q1: What is NAT?
👉 Mapping private IP to public IP

Q2: Why NAT used?
👉 To solve IPv4 shortage

Q3: Types of NAT?
👉 Static, Dynamic, PAT

Q4: What is PAT?
👉 Many devices share one IP using ports

Q5: NAT table?
👉 Stores IP-port mappings

Q6: Does NAT change IP?
👉 Yes

Q7: Why NAT needed?
👉 IPv4 shortage

Q8: Is NAT security feature?
👉 Indirectly yes

Q9: Which NAT is most used?
👉 PAT

Q10: NAT vs Routing?
👉 NAT translates IP, routing forwards packets

# 🔥 SUMMARY
NAT = IP translation system
Used to solve IPv4 shortage
Most important type = PAT
Works using NAT table + ports