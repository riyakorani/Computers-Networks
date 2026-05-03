# 🚦 TCP Congestion Control

---

# 🎯 Core Idea

> TCP dynamically adjusts its sending rate to **avoid network congestion**

👉 Too much data → congestion (like traffic jam)
👉 TCP slows down to maintain stability

---

# 🧠 Why Congestion Control is Needed

Without it:

* Network overload ❌
* Packet loss ❌
* Internet instability ❌

👉 Congestion control prevents **network collapse**

---

# 🚗 Real-World Analogy

* Empty road → increase speed 🚗💨
* Traffic jam → slow down 🚦

👉 TCP behaves the same way

---

# 🔥 Key Algorithms

---

## 1️⃣ Slow Start

> Start small, grow fast

* Initial window is small
* Doubles every round-trip time (RTT)

### Growth:

```text
1 → 2 → 4 → 8 → 16
```

👉 Exponential growth

---

## 2️⃣ Congestion Avoidance

> Grow slowly near capacity

* Linear increase

### Growth:

```text
16 → 17 → 18 → 19
```

👉 Avoids sudden congestion

---

## 3️⃣ Packet Loss Detection

Packet loss = signal of congestion

---

### 🔴 Case A: Timeout (Severe Congestion)

* Window reset to minimum
* Restart with slow start

---

### 🟡 Case B: Duplicate ACKs (Mild Congestion)

* Reduce window size (not reset completely)
* Continue transmission

---

## 4️⃣ AIMD (Core Principle)

> Additive Increase + Multiplicative Decrease

* Increase slowly (linear)
* Decrease sharply (usually halve window)

---

# 📊 Behavior Pattern

```text
Grow fast → grow slow → drop → repeat
```

👉 Ensures balance between:

* Speed ⚡
* Stability 🛡️

---

# 🧠 Key Terms

* **Congestion Window (cwnd)** → controls sending rate
* **RTT (Round Trip Time)** → time for send + ACK
* **Threshold (ssthresh)** → switch point (slow start → avoidance)

---

# 🎯 Key Takeaways

* TCP adjusts speed dynamically
* Packet loss = congestion signal
* Uses:

  * Slow Start
  * Congestion Avoidance
  * AIMD

---

# 🧪 Quetions i practiced

* Why does TCP reduce window size after packet loss?
* What is exponential growth in slow start?
* What does AIMD stand for?

---

# 🚀 Big Picture

TCP =

* Reliability
* Flow Control
* Sliding Window
* Congestion Control

👉 Together → stable and efficient communication

---

# 🚀 Next Step

* Fast Retransmit & Fast Recovery
* TCP vs UDP (deep real-world comparison)
* Transition to IP & Routing

---
