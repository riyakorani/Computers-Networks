# 🔥 FIREWALL — COMPUTER NETWORKS (FAANG LEVEL NOTES)

---

# 🧠 1. WHAT IS A FIREWALL?

👉 A firewall is a network security system that:
- Monitors traffic  
- Controls access  
- Filters packets  

based on predefined rules  

---

# 🎯 CORE IDEA

👉 "Gatekeeper between trusted and untrusted network"

---

# 🧪 REAL ANALOGY

👉 Like a security guard at a building:
- Allow trusted people ✅  
- Block suspicious ones ❌  

---

---

# 🚦 2. FIREWALL ACTIONS

---

## ✔ ACCEPT
👉 Allow traffic  

---

## ❌ REJECT
👉 Block + send error response  

---

## 🚫 DROP (VERY IMPORTANT ⭐)
👉 Block silently  

---

## 🎯 INTERVIEW TIP

👉 DROP is more secure (no info to attacker)

---

---

# 🧠 3. WHY FIREWALL IS IMPORTANT

---

✔ Prevent unauthorized access  
✔ Block malicious traffic  
✔ Protect sensitive data  
✔ Control network usage  
✔ Reduce insider threats  

---

---

# ⚙️ 4. HOW FIREWALL WORKS

---

## 🔁 FLOW

1. Packet enters network  
2. Firewall inspects packet  
3. Matches rules  
4. Action taken (accept/reject/drop)  

---

## 🧠 KEY CONCEPT

👉 Everything must pass through firewall  

---

---

# ⚠️ 5. DEFAULT POLICY (VERY IMPORTANT ⭐)

---

👉 If no rule matches → default action applied  

---

## TYPES

- Accept (not secure)  
- Reject  
- Drop (BEST PRACTICE)  

---

## 🎯 INTERVIEW EDGE

👉 Default = **DROP/REJECT** for security  

---

---

# 🔥 6. TYPES OF FIREWALLS

---

# 🌟 1. PACKET FILTERING FIREWALL

---

## 🧠 IDEA

👉 Filters based on:
- IP  
- Port  
- Protocol  

---

## ❌ LIMITATION

❌ No context awareness  

---

---

# 🌟 2. STATEFUL FIREWALL ⭐

---

## 🧠 IDEA

👉 Tracks connection state  

---

## ⚡ BENEFIT

✔ More intelligent filtering  

---

---

# 🌟 3. PROXY FIREWALL

---

## 🧠 IDEA

👉 Acts as intermediary  

---

## 🧪 SCENARIO

👉 Client → Proxy → Server  

---

## ⚡ BENEFIT

✔ Hides internal network  

---

---

# 🌟 4. WAF (Web Application Firewall) ⭐⭐

---

## 🧠 IDEA

👉 Protects web apps  

---

## 🧪 BLOCKS

- SQL injection  
- XSS  

---

---

# 🌟 5. NGFW (Next-Gen Firewall)

---

## 🧠 FEATURES

✔ Deep packet inspection  
✔ Intrusion prevention  
✔ Application awareness  

---

---

# 🌟 6. CIRCUIT-LEVEL GATEWAY

---

👉 Monitors session layer  

---

---

# 🧠 7. BASED ON DEPLOYMENT

---

## 🔹 Network Firewall
👉 Protects entire network  

---

## 🔹 Host-Based Firewall
👉 Protects single device  

---

---

# 🧠 8. BASED ON PLACEMENT

---

## 🔹 Perimeter Firewall
👉 At network boundary  

---

## 🔹 Internal Firewall
👉 Inside network  

---

## 🔹 Distributed Firewall
👉 Across multiple systems  

---

---

# 🧪 9. REAL-WORLD SCENARIO (VERY IMPORTANT)

---

## 🧪 Accessing Website

1. Request goes through firewall  
2. Firewall checks:
   - IP  
   - Port  
   - Protocol  

3. If safe → allowed  
4. If suspicious → blocked  

---

---

# 🛡️ 10. ATTACKS FIREWALL PROTECTS AGAINST

---

- Unauthorized access  
- Malware traffic  
- DoS attacks  
- Port scanning  

---

---

# 🎯 11. INTERVIEW QUESTIONS

---

## Q1: What is firewall?
👉 Traffic filtering system  

---

## Q2: Accept vs Reject vs Drop?
👉 Allow / Block with response / Block silently  

---

## Q3: Stateful vs stateless firewall?
👉 Tracks connection vs simple filtering  

---

## Q4: What is WAF?
👉 Protects web apps  

---

## Q5: Why default drop?
👉 Maximum security  

---

## Q6: Firewall vs IDS?
👉 Firewall blocks, IDS detects  

---

---

# 🔥 FINAL SUMMARY

👉 Firewall = network gatekeeper  
👉 Filters traffic using rules  
👉 Types vary by intelligence  
👉 Default DROP = best security  

---

