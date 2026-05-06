# 🎯 QUALITY OF SERVICE (QoS) & MULTIMEDIA — FAANG LEVEL NOTES

---

# 🧠 1. WHAT IS QoS?

👉 QoS (Quality of Service) is a set of techniques used to:
- Prioritize network traffic  
- Control bandwidth  
- Ensure performance for critical applications  

---

# 🎯 CORE IDEA

👉 Not all traffic is equal

- Voice/video → high priority  
- Downloads → low priority  

---

# 🧪 REAL PROBLEM

Without QoS:
- Video call lags ❌  
- Voice breaks ❌  
- Streaming buffers ❌  

---

# 🚀 WITH QoS

✔ Smooth video calls  
✔ Stable audio  
✔ Better user experience  

---

# 📊 2. QoS PARAMETERS (VERY IMPORTANT ⭐)

---

## 🔹 1. LATENCY

👉 Time taken for packet to travel  

✔ Low latency = faster communication  

---

## 🔹 2. JITTER

👉 Variation in delay  

✔ Low jitter = smooth audio/video  

---

## 🔹 3. PACKET LOSS

👉 Dropped packets  

❌ High loss = broken video/audio  

---

## 🔹 4. BANDWIDTH

👉 Maximum data capacity  

---

## 🔹 5. THROUGHPUT

👉 Actual data delivered  

---

## 🔹 6. MOS (Mean Opinion Score)

👉 Voice quality (1–5 scale)

---

## 🔹 7. ERROR RATE

👉 Corrupted/lost packets  

---

# ⚡ 3. HOW QoS WORKS

---

## 🔹 Step 1: CLASSIFICATION

👉 Identify traffic:
- Voice  
- Video  
- Data  

---

## 🔹 Step 2: MARKING

👉 Label packets (e.g., DSCP)

---

## 🔹 Step 3: QUEUING

👉 Separate queues:
- High priority  
- Low priority  

---

## 🔹 Step 4: SCHEDULING

👉 Send high-priority packets first  

---

## 🔹 Step 5: TRAFFIC CONTROL

- Shaping → smooth traffic  
- Policing → limit traffic  

---

# 📦 4. QoS TYPES

---

# 🌟 1. STATELESS (DiffServ)

---

## 🧠 IDEA

👉 No per-flow tracking  

---

## ⚡ FEATURES

✔ Scalable  
✔ Class-based  

---

## ❌ LIMITATION

❌ No strict guarantees  

---

---

# 🌟 2. STATEFUL (IntServ)

---

## 🧠 IDEA

👉 Per-flow resource reservation  

---

## ⚡ FEATURES

✔ Strong guarantees  
✔ Precise control  

---

## ❌ LIMITATION

❌ Not scalable  

---

# 📊 5. IntServ vs DiffServ (IMPORTANT)

| Feature | IntServ | DiffServ |
|--------|--------|----------|
| Control | Per flow | Per class |
| Guarantee | Strong | Relative |
| Scalability | Low | High |
| Complexity | High | Low |

---

# 🧠 6. KEY MECHANISMS

---

## 🔹 RSVP

👉 Reserves resources for flows  

---

## 🔹 Admission Control

👉 Accept traffic only if resources available  

---

## 🔹 Scheduling

👉 Controls packet sending order  

---

---

# 🌍 7. REAL-WORLD SCENARIO

---

## 🧪 Video Call + Download

Without QoS:
- Download uses full bandwidth  
- Call lags  

With QoS:
- Video call prioritized  
- Download slowed  

---

# 🧰 8. QoS TOOLS

---

- Classification & Marking  
- Queuing & Scheduling  
- Traffic Shaping  
- Policing  
- Congestion Management  

---

# 🎬 9. QoS + MULTIMEDIA (VERY IMPORTANT ⭐)

---

## 🧠 WHY QoS NEEDED?

👉 Multimedia is sensitive to:

- Delay  
- Jitter  
- Packet loss  

---

## 🧪 EXAMPLES

- VoIP calls  
- Zoom meetings  
- Netflix streaming  

---

## ⚡ BENEFITS

✔ Smooth playback  
✔ No buffering  
✔ Sync audio/video  

---

# 🎥 10. MULTIMEDIA

---

## 🧠 DEFINITION

👉 Combination of multiple media types:

- Text  
- Audio  
- Video  
- Graphics  
- Animation  

---

## 🧪 COMPONENTS

- Text → content  
- Graphics → visuals  
- Audio → sound  
- Video → motion  
- Animation → effects  

---

# 🎯 11. INTERVIEW QUESTIONS

---

## Q1: What is QoS?
👉 Traffic prioritization mechanism  

---

## Q2: Why QoS needed?
👉 To support real-time apps  

---

## Q3: What is jitter?
👉 Variation in delay  

---

## Q4: IntServ vs DiffServ?
👉 Per-flow vs class-based  

---

## Q5: What is latency?
👉 Time delay  

---

## Q6: Why QoS important for video?
👉 Prevents lag and buffering  

---

## Q7: What is packet loss?
👉 Dropped packets  

---

# 🔥 FINAL SUMMARY

👉 QoS = traffic control system  
👉 Ensures performance for critical apps  
👉 Uses classification + queuing + scheduling  
👉 Essential for multimedia  

---

