# 🌐 TCP (Transmission Control Protocol)

---

# 🎯 Core Idea

> TCP provides **reliable, ordered, and error-checked delivery** of data between applications.

---

# 🧠 Key Principle

TCP is **connection-oriented**
👉 Data transfer starts **only after connection establishment**

---

# 🤝 TCP 3-Way Handshake

## Purpose:

* Establish connection
* Synchronize sequence numbers

---

## 🔁 Steps

### 1️⃣ SYN (Synchronize)

Client → Server

* Initiates connection
* Sends initial sequence number

---

### 2️⃣ SYN-ACK

Server → Client

* Acknowledges request
* Sends its own sequence number

---

### 3️⃣ ACK

Client → Server

* Confirms connection

---

## ✅ Result

Connection established → Data transfer begins

---

## 📡 Flow

```text
Client        Server
  |   SYN   →   |
  |  ← SYN-ACK  |
  |   ACK   →   |
```

---

# 📦 Data Transfer (After Handshake)

Data is sent in **segments**

---

# 🧠 Core TCP Mechanisms

---

## 1️⃣ Sequence Numbers

* Each segment is numbered
* Ensures **correct ordering**

---

## 2️⃣ Acknowledgment (ACK)

Receiver sends:

> “Next expected sequence number”

### Example:

Sent: 1, 2, 3
Received: 1, 2

👉 ACK = 3 (means “send 3 again”)

---

## 3️⃣ Retransmission

* Lost packets are **automatically resent**
* Triggered by:

  * Timeout
  * Duplicate ACKs

---

## 4️⃣ Flow Control

* Prevents overwhelming receiver
* Uses **window size**

👉 Sender adjusts speed based on receiver capacity

---

## 5️⃣ Congestion Control

* Prevents network overload

### Behavior:

* Increase speed gradually
* Reduce speed on congestion

---

# ⚠️ Why TCP is Slower

* Connection setup (handshake)
* Acknowledgments required
* Error checking overhead

👉 Trade-off: **Speed vs Reliability**

---

# ⚡ TCP vs UDP

| Feature     | TCP                 | UDP              |
| ----------- | ------------------- | ---------------- |
| Reliability | ✅ Yes               | ❌ No             |
| Ordering    | ✅ Guaranteed        | ❌ Not guaranteed |
| Speed       | Slower              | Faster           |
| Connection  | Connection-oriented | Connectionless   |

---

# 🧠 Real-World Usage

| Application               | Protocol     |
| ------------------------- | ------------ |
| Web browsing (HTTP/HTTPS) | TCP          |
| File transfer             | TCP          |
| Video streaming           | UDP (mostly) |
| Online gaming             | UDP          |

---

# 🎯 Key Takeaways

* TCP ensures **reliable and ordered delivery**
* Uses **handshake before communication**
* Handles:

  * Loss (retransmission)
  * Order (sequence numbers)
  * Speed (flow + congestion control)

---


# 🚀 Next Step

* TCP Congestion Control (deep dive)
* UDP internals
* Real-world protocol mapping (HTTP, HTTPS)
