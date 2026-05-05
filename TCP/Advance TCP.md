# 🚦 TCP ADVANCED — COMPLETE DEEP NOTES (FAANG LEVEL)

---

# 🧠 1. WHY ADVANCED TCP?

Basic TCP ensures reliability, but real-world networks face:
- Packet loss
- Congestion
- Delay (latency)

👉 Advanced TCP mechanisms handle these efficiently.

---

# 📦 2. PACKET LOSS PROBLEM

---

## 🧪 Example:

Sender sends:

1 2 3 4 5


Receiver gets:

1 2 ❌ 4 5


👉 Packet 3 is lost

---

# 🔁 3. DUPLICATE ACKs (KEY SIGNAL)

Receiver keeps sending:

ACK = 3
ACK = 3
ACK = 3


👉 Meaning:
> “I am still waiting for packet 3”

---

# 🚀 4. FAST RETRANSMIT ⭐

---

## 🧠 What happens?

After **3 duplicate ACKs**:
👉 Sender retransmits missing packet immediately

---

## 🧪 Scenario:

- Packet 3 lost
- Receiver sends 3 duplicate ACKs
- Sender quickly resends packet 3

---

## 🔥 Why important?

✔ No need to wait for timeout  
✔ Faster recovery  
✔ Improves performance  

---

# 🔄 5. FAST RECOVERY

---

## 🧠 Idea:

After fast retransmit:
👉 Do NOT restart from beginning

Instead:
- Reduce congestion window (cwnd)
- Continue with congestion avoidance

---

## 🧪 Scenario:

Before loss:

cwnd = 16


After loss:

cwnd = 8 (halved)


👉 Then grows linearly

---

# 📉 6. CONGESTION WINDOW (cwnd)

---

## 🧠 What is cwnd?

Controls how much data can be sent without ACK.

---

## 📈 Growth Pattern:

### Slow Start:

1 → 2 → 4 → 8 → 16


### Congestion Avoidance:

16 → 17 → 18 → 19


---

# 🔁 7. TIMEOUT vs DUPLICATE ACK

---


## 🔴 Timeout (Severe Congestion)

- No ACK received
- Reset cwnd to 1
- Restart slow start

---

## 🟡 Duplicate ACK (Mild Congestion)

- Fast retransmit
- cwnd reduced (not reset)

---

## 🧪 Comparison:

| Condition | Action |
|----------|--------|
| Timeout | Restart from 1 |
| Duplicate ACK | Reduce window |

---

# 🔚 8. TCP 4-WAY TERMINATION

---

## 🧠 Why 4 steps?

Because both sides close independently.

---

## 📦 Flow:


Client → FIN
Server → ACK
Server → FIN
Client → ACK


---

## 🧪 Scenario:

- Client finishes sending data
- Server still has data to send
- Hence separate close signals

---

# ⏳ 9. TIME_WAIT STATE

---

## 🧠 What is TIME_WAIT?

After connection close:
👉 Client waits for some time

---

## Why?

✔ Ensure last ACK is received  
✔ Prevent duplicate packets  

---

# 🌍 10. REAL-WORLD SCENARIOS

---

## 🧪 Scenario 1: Slow Internet

👉 Cause:
- Congestion
- Packet loss

👉 TCP action:
- Reduces window size
- Slows down sending rate

---

## 🧪 Scenario 2: Video Buffering

👉 Cause:
- Lost packets

👉 TCP action:
- Retransmits missing packets

---

## 🧪 Scenario 3: High Traffic Network

👉 TCP:
- Detects congestion
- Uses AIMD (reduce rate)

---

## 🧪 Scenario 4: Long Distance Server

👉 Effect:
- High RTT
- Slower ACK

👉 Result:
- Lower throughput

---

# ⚡ 11. KEY TERMS

---

## 🔑 cwnd (Congestion Window)
Controls sending rate

---

## 🔑 ssthresh (Threshold)
Switch between slow start and avoidance

---

## 🔑 RTT (Round Trip Time)
Time for send + ACK

---

## 🔑 Duplicate ACK
Signal of missing packet

---

# 🧠 12. INTERVIEW QUESTIONS

---

## Q1: What is Fast Retransmit?
👉 Retransmit after 3 duplicate ACKs

---

## Q2: What is Fast Recovery?
👉 Continue after reducing window (no restart)

---

## Q3: Timeout vs duplicate ACK?
👉 Timeout = severe, duplicate = mild

---

## Q4: Why TCP reduces window?
👉 To avoid congestion

---

## Q5: What is cwnd?
👉 Controls number of packets in flight

---

## Q6: Why 4-way termination?
👉 Both sides close independently

---

## Q7: What is TIME_WAIT?
👉 Wait state after closing connection

---

## Q8: What causes duplicate ACK?
👉 Missing packet

---

## Q9: What happens after packet loss?
👉 Retransmission + cwnd reduction

---

## Q10: Why TCP is reliable?
👉 ACK + retransmission + control mechanisms

---

# 🔥 FINAL SUMMARY

👉 Fast retransmit = quick loss recovery  
👉 Fast recovery = avoid restart  
👉 Timeout = severe congestion  
👉 TCP adapts dynamically  
👉 Ensures stable internet communication  

---