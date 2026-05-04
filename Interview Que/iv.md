📘 Computer Networks — Complete Practice Question Bank


🔢 1. SUBNETTING (10 Questions)
🧪 Q1: What is subnetting?
🧪 Q2: Why is subnetting used?
🧪 Q3: What is CIDR notation?
🧪 Q4: Calculate hosts for /24 network.
🧪 Q5: Calculate hosts for /26 network.
🧪 Q6: What is VLSM?
🧪 Q7: Why is VLSM better than subnetting?
🧪 Q8: Solve VLSM for hosts: 50, 20, 10.
🧪 Q9: What is block size in subnetting?
🧪 Q10: What is default subnet mask of Class C?


🌐 2. DNS (10 Questions)
🧪 Q1: What is DNS?
🧪 Q2: Why is DNS needed?
🧪 Q3: DNS full form?
🧪 Q4: What is DNS hierarchy?
🧪 Q5: What is root server?
🧪 Q6: What is TLD server?
🧪 Q7: What is authoritative server?
🧪 Q8: What is DNS caching?
🧪 Q9: Which protocol does DNS use?
🧪 Q10: What is TTL in DNS?


🌐 3. HTTP / HTTPS (10 Questions)
🧪 Q1: What is HTTP?
🧪 Q2: What is HTTPS?
🧪 Q3: Difference between HTTP and HTTPS?
🧪 Q4: Why HTTPS is secure?
🧪 Q5: What is TLS?
🧪 Q6: What is SSL certificate?
🧪 Q7: HTTP port number?
🧪 Q8: HTTPS port number?
🧪 Q9: What is stateless protocol?
🧪 Q10: What happens when you hit a URL?


🔁 4. TCP / UDP (10 Questions)
🧪 Q1: What is TCP?
🧪 Q2: What is UDP?
🧪 Q3: TCP vs UDP difference?
🧪 Q4: What is TCP 3-way handshake?
🧪 Q5: Why TCP is reliable?
🧪 Q6: Why UDP is faster?
🧪 Q7: TCP use cases?
🧪 Q8: UDP use cases?
🧪 Q9: What happens if packet is lost in TCP?
🧪 Q10: Does UDP guarantee delivery?


🧠 5. OSI MODEL (10 Questions)
🧪 Q1: What is OSI model?
🧪 Q2: How many layers in OSI?
🧪 Q3: Name all OSI layers.
🧪 Q4: Which layer is HTTP?
🧪 Q5: Which layer is TCP?
🧪 Q6: Which layer is IP?
🧪 Q7: Which layer does encryption?
🧪 Q8: What is encapsulation?
🧪 Q9: Which layer handles routing?
🧪 Q10: Why OSI model is important?


🌍 6. REAL-WORLD SCENARIOS (10 Questions)
🧪 Q1: Website not opening — how to debug?
🧪 Q2: Internet works but site not loading?
🧪 Q3: Ping works but browser fails?
🧪 Q4: Slow internet reasons?
🧪 Q5: DNS works but HTTPS fails?
🧪 Q6: What if TCP handshake fails?
🧪 Q7: What if DNS fails?
🧪 Q8: What if server is down?
🧪 Q9: Why page loads slowly?
🧪 Q10: Which OSI layer fails if no internet?



# 📘 Computer Networks — Complete Practice Questions + Answers

---

# 🔢 1. SUBNETTING

## Q1: What is subnetting?
👉 Dividing a large network into smaller networks.

## Q2: Why is subnetting used?
👉 To reduce broadcast traffic and improve efficiency.

## Q3: What is CIDR?
👉 Compact IP notation like /24.

## Q4: Hosts in /24?
👉 254

## Q5: Hosts in /26?
👉 62

## Q6: What is VLSM?
👉 Variable Length Subnet Masking (different subnet sizes).

## Q7: Why VLSM better?
👉 Efficient IP usage.

## Q8: VLSM for 50, 20, 10?
👉 50=/26, 20=/27, 10=/28

## Q9: Block size?
👉 256 - subnet value

## Q10: Class C default mask?
👉 /24

---

# 🌐 2. DNS

## Q1: What is DNS?
👉 Converts domain names to IP.

## Q2: Why DNS?
👉 Humans use names, computers use IPs.

## Q3: Full form?
👉 Domain Name System

## Q4: DNS hierarchy?
👉 Root → TLD → Authoritative

## Q5: Root server?
👉 Top-level redirect server

## Q6: TLD server?
👉 Handles .com, .org

## Q7: Authoritative server?
👉 Gives final IP

## Q8: DNS caching?
👉 Stores results temporarily

## Q9: DNS protocol?
👉 UDP (port 53)

## Q10: TTL?
👉 Cache expiry time

---

# 🌐 3. HTTP / HTTPS

## Q1: HTTP?
👉 Web communication protocol

## Q2: HTTPS?
👉 HTTP + encryption (TLS)

## Q3: Difference?
👉 HTTP = unsafe, HTTPS = secure

## Q4: Why HTTPS secure?
👉 Encryption + authentication

## Q5: TLS?
👉 Security protocol

## Q6: SSL certificate?
👉 Website identity proof

## Q7: HTTP port?
👉 80

## Q8: HTTPS port?
👉 443

## Q9: Stateless?
👉 No memory of requests

## Q10: URL flow?
👉 DNS → IP → TCP → HTTP → Render

---

# 🔁 4. TCP / UDP

## Q1: TCP?
👉 Reliable protocol

## Q2: UDP?
👉 Fast protocol

## Q3: Difference?
👉 TCP reliable, UDP fast

## Q4: TCP handshake?
👉 SYN → SYN-ACK → ACK

## Q5: TCP reliable?
👉 ACK + retransmission

## Q6: UDP faster?
👉 No handshake

## Q7: TCP use?
👉 File transfer, web

## Q8: UDP use?
👉 Gaming, streaming

## Q9: TCP loss?
👉 Retransmission

## Q10: UDP loss?
👉 Not recovered

---

# 🧠 5. OSI MODEL

## Q1: OSI model?
👉 7-layer networking model

## Q2: Layers?
👉 Application, Presentation, Session, Transport, Network, Data Link, Physical

## Q3: HTTP layer?
👉 Application

## Q4: TCP layer?
👉 Transport

## Q5: IP layer?
👉 Network

## Q6: Encryption layer?
👉 Presentation

## Q7: Encapsulation?
👉 Adding headers at each layer

## Q8: Routing layer?
👉 Network

## Q9: Why OSI?
👉 Standard networking model

## Q10: Data flow?
👉 Down (send), up (receive)

---

# 🌍 6. REAL SCENARIOS

## Q1: Website not opening?
👉 Check DNS → TCP → HTTP

## Q2: Internet works but site not?
👉 DNS/server issue

## Q3: Ping works but browser fails?
👉 TCP/HTTP issue

## Q4: Slow internet?
👉 Congestion, packet loss

## Q5: DNS works but HTTPS fails?
👉 TLS/certificate issue

## Q6: TCP failure?
👉 No connection

## Q7: DNS failure?
👉 Name not resolved

## Q8: Server down?
👉 No response

## Q9: Slow loading?
👉 High latency

## Q10: No internet layer issue?
👉 Physical/Network layer

---

# 🚀 FINAL SUMMARY
✔ Subnetting  
✔ DNS  
✔ HTTP/HTTPS  
✔ TCP/UDP  
✔ OSI  
✔ Real-world troubleshooting  
