# Distributed Denial of Service (DDoS) Attack – Detailed Overview

---

## Introduction

A **Distributed Denial of Service (DDoS)** attack is a **coordinated cyberattack** where multiple compromised systems (often part of a **botnet**) flood a target with massive amounts of traffic or requests.  

Unlike **DoS**, which uses a single source, DDoS is harder to stop because traffic originates from **thousands or millions of devices worldwide**.  

---

## How DDoS Works

1. **Botnet Creation**  
   - Attackers compromise IoT devices, PCs, or servers with malware (e.g., **Mirai**).  

2. **Command & Control (C2)**  
   - Infected devices connect to a central system controlled by the attacker.  

3. **Attack Launch**  
   - Botnet floods the target with requests or data packets.  

4. **Overload**  
   - Target’s bandwidth, CPU, or application resources become exhausted.  

5. **Denial of Service**  
   - Legitimate users are unable to access the service.  

---

## Types of DDoS Attacks

### 1. Volume-Based
- **Examples:** UDP Flood, ICMP Flood, Amplification attacks.  
- **Goal:** Consume bandwidth.  

### 2. Protocol Attacks
- **Examples:** SYN Flood, Smurf Attack, Ping of Death.  
- **Goal:** Exploit vulnerabilities in Layer 3/4 protocols.  

### 3. Application Layer Attacks
- **Examples:** HTTP Flood, Slowloris.  
- **Goal:** Overload web apps with seemingly legitimate traffic.  

### 4. Amplification Attacks
- **Examples:** DNS Amplification, Memcached Amplification.  
- **Goal:** Use small queries to trigger massive responses.  

---

## Tools & Botnets

- **Mirai Botnet** → Famous IoT-based botnet used in Dyn attack.  
- **LOIC (Low Orbit Ion Cannon)** → Basic stress testing tool.  
- **HOIC (High Orbit Ion Cannon)** → Advanced version, targets multiple URLs.  
- **Botnets** (e.g., Reaper, Mozi) → Compromise IoT and servers for mass-scale attacks.  

---

## Real-World Case Studies

### 1. GitHub (2018)
- **Attack:** 1.35 Tbps Memcached amplification.  
- **Impact:** Temporary outage.  
- **Mitigation:** Akamai rerouted and scrubbed traffic.  

### 2. Dyn DNS (2016)
- **Attack:** Mirai botnet used IoT devices to launch a massive DDoS.  
- **Impact:** Twitter, Netflix, Reddit, Spotify are inaccessible across the US/EU.  
- **Mitigation:** Improved DNS redundancy, IoT vendor security patches.  

### 3. Krebs on Security (2016)
- **Attack:** 620 Gbps Mirai DDoS.  
- **Impact:** Akamai dropped free protection due to scale.  
- **Mitigation:** Google’s Project Shield took over.  

### 4. Estonia Cyberattacks (2007)
- **Attack:** Politically motivated DDoS against banks, media, and government.  
- **Impact:** National-level service disruption.  
- **Mitigation:** NATO assistance, filtering, and blacklisting.  

### 5. AWS DDoS (2020)
- **Attack:** Largest recorded DDoS at **2.3 Tbps**, using CLDAP reflection.  
- **Impact:** AWS services were briefly affected.  
- **Mitigation:** AWS Shield defended with scrubbing and scaling.  

---

## Impacts of DDoS

-  **Financial Losses:** Cost of downtime + mitigation (millions per hour).  
-  **Global Reach:** Disrupts major services (e.g., Netflix, Twitter).  
-  **Reputation Damage:** Users lose trust after repeated downtime.  
-  **Collateral Damage:** Attacks on one provider affect dependent businesses.  
-  **National Security Risks:** State-sponsored DDoS can cripple infrastructure.  

---

## Mitigation Strategies

### Network-Level
- Firewalls with traffic filtering & rate-limiting.  
- IDS/IPS for anomaly detection.  
- Geo-blocking suspicious traffic sources.  

### Application-Level
- Web Application Firewall (WAF).  
- Request throttling & CAPTCHA.  
- Load balancing across clusters.  

### Cloud-Based
- **DDoS protection services:** Cloudflare, Akamai, AWS Shield, Google Cloud Armor.  
- Traffic rerouting & scrubbing centres.  

### Architectural
- **Anycast Routing:** Distributes load globally.  
- **Redundancy:** Multiple data centers.  
- **CDNs:** Cache static content to reduce load.  

### Preventive
- Keep IoT devices updated.  
- Regular penetration testing & red teaming.  
- Incident Response Plans & Business Continuity strategies.  

---

## Emerging Defenses

- **AI & Machine Learning:** Detect abnormal traffic patterns early.  
- **Blockchain-Based Security:** Decentralized mitigation for IoT & cloud.  
- **Zero-Trust Networking:** Verify traffic sources before granting access.  
- **Adaptive Immune Systems:** Self-healing defenses inspired by biology.  

---

## Summary

- **DDoS = Distributed DoS** with botnets or many sources.  
- **Types:** Volume, Protocol, Application, Amplification.  
- **Case Studies:** GitHub (2018), Dyn (2016), Krebs (2016), Estonia (2007), AWS (2020).  
- **Impact:** Massive financial losses, global disruptions, reputational harm.  
- **Defense:** Requires **layered security** (network + app + cloud + architecture).  

---

## References

- [Cloudflare – What is DDoS?](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/)  
- [AWS Shield – DDoS Protection](https://aws.amazon.com/shield/)  
- [Wikipedia – DDoS](https://en.wikipedia.org/wiki/Denial-of-service_attack)  
- [Krebs on Security – DDoS Attacks](https://krebsonsecurity.com/)  

---
