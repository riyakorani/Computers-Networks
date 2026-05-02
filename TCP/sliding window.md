# 📊 Sliding Window (Core of TCP Efficiency)

---

# 🎯 Core Idea

> Sliding Window allows TCP to send **multiple segments without waiting for individual ACKs**

👉 Improves **throughput + efficiency**

---

# 🧠 Why Sliding Window?

## ❌ Stop-and-Wait (Inefficient)

* Send 1 segment
* Wait for ACK
* Send next

👉 High delay, poor utilization

---

## ✅ Sliding Window (Efficient)

* Send multiple segments
* Receive ACKs cumulatively

👉 Better bandwidth utilization 🚀

---

# 📦 Basic Concept

Assume:

👉 Window Size = 3

Sender can send:

```text
[1] [2] [3]
```

Without waiting for ACK

---

# 🔁 Sliding Mechanism

Receiver sends:

```text
ACK = 4
```

👉 Means: “Received up to 3, expecting 4”

Now window shifts:

```text
[4] [5] [6]
```

👉 This movement = **Sliding**

---

# 🔑 Key Components

---

## 1️⃣ Window Size

* Number of unacknowledged segments allowed
* Controlled by:

  * Receiver capacity (flow control)
  * Network conditions (congestion control)

---

## 2️⃣ Cumulative ACK

* ACK = N → means **all data up to N-1 received**

### Example:

```text
ACK = 5 → received 1,2,3,4
```

---

## 3️⃣ Lost Packet Scenario

Sent:

```text
1  2  3  4
```

Received:

```text
1  2  ❌ 4
```

Receiver sends:

```text
ACK = 3
```

👉 Means: “Still waiting for 3”

---

## 🔁 What Sender Does

* Detects duplicate ACKs or timeout
* Retransmits missing segment (3)
* Continues transmission

---

# ⚡ Why Sliding Window is Powerful

* Reduces idle time
* Increases throughput
* Enables continuous data flow
* Adapts dynamically

---

# 🚦 Flow Control (Receiver Side)

Receiver advertises:

```text
Window Size = N
```

👉 Prevents sender from overwhelming receiver

---

# 🚦 Congestion Control (Network Side)

TCP adjusts window based on network:

* Network busy → reduce window
* Network free → increase window

👉 Achieved using:

* Slow Start
* Congestion Avoidance

---

# 🧠 Mental Model

| Concept | Meaning                    |
| ------- | -------------------------- |
| Window  | Allowed “in-flight” data   |
| ACK     | Progress signal            |
| Slide   | Move forward after success |

---

# 🎯 Key Takeaways

* Sliding Window enables **parallel transmission**
* Uses **cumulative ACKs**
* Handles **loss + ordering**
* Controlled by **flow + congestion control**

---

