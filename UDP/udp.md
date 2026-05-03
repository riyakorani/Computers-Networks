# 🌐 UDP (User Datagram Protocol)

---

# 🎯 Core Idea

> UDP provides **fast, connectionless, best-effort delivery** of data.

---

# 🧠 Key Principle

UDP is **connectionless**

👉 No handshake
👉 No guarantee of delivery
👉 No ordering

---

# ⚡ How UDP Works

* Data is sent directly as **datagrams**
* No setup phase
* No tracking of packets

---

# 📦 Data Unit

| Layer     | Data Unit |
| --------- | --------- |
| Transport | Datagram  |

---

# 🔥 What UDP DOES NOT Provide

* ❌ No reliability
* ❌ No retransmission
* ❌ No ordering
* ❌ No flow control
* ❌ No congestion control

---

# 🚀 What UDP DOES Provide

* ✅ Very low latency
* ✅ Minimal overhead
* ✅ Fast transmission

---

# 🧠 Real Scenario

You’re watching a live stream:

* Frame 1 lost ❌
* Frame 2 arrives ✅

👉 UDP **does NOT resend Frame 1**

Why?

👉 Because speed is more important than perfection

---

# ⚡ UDP vs TCP (Clear Contrast)

| Feature     | TCP             | UDP            |
| ----------- | --------------- | -------------- |
| Connection  | Yes (handshake) | No             |
| Reliability | High            | Low            |
| Ordering    | Guaranteed      | Not guaranteed |
| Speed       | Slower          | Faster         |
| Overhead    | High            | Low            |

---

# 📡 Real-World Use Cases

| Application        | Protocol |
| ------------------ | -------- |
| Video streaming    | UDP      |
| Online gaming      | UDP      |
| Voice calls (VoIP) | UDP      |
| DNS queries        | UDP      |

---

# 🧠 Mental Model

| TCP                             | UDP                                 |
| ------------------------------- | ----------------------------------- |
| Courier service (safe, tracked) | Throwing flyers (fast, no tracking) |

---

# ⚠️ When to Use UDP

Use UDP when:

* Speed is critical
* Some data loss is acceptable
* Real-time communication is needed

---

# 🎯 Key Takeaways

* UDP is **fast but unreliable**
* No connection setup
* No guarantees → but minimal delay
* Used in **real-time systems**

---

# 🧪 Quick Check

* Why is UDP faster than TCP?
* What happens if a UDP packet is lost?
* Why is UDP used in streaming?

---

# 🚀 Next Step

* Deep TCP vs UDP scenarios
* When systems choose one over the other
* Hybrid models (QUIC, HTTP/3)
