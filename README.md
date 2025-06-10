### 🛡️ Introduction to SIEM

**Room:** [Introduction to SIEM — TryHackMe](https://tryhackme.com/room/introtosiem)  
**Status:** ✅ Completed  
**Date:** *10 June 2025* 

### 🎯 Objective
Understand what SIEM is, how it works, and its role in a security operations centre (SOC). Learn about log ingestion, correlation rules, dashboards, and how SIEM helps analysts detect, investigate, and respond to threats.

---

### 🗝️ Key Concepts  
- **SIEM (Security Information and Event Management)** — Collects, centralises, and analyses logs from multiple systems in real-time to detect and respond to security incidents.  
- **Network Visibility** — SIEM provides full visibility by ingesting both host-centric logs (like Sysmon, Event Logs) and network-centric logs (like SSH, HTTP, VPN traffic).  
- **Log Ingestion Methods**:  
  - *Agent/Forwarder* (e.g. Splunk forwarder)  
  - *Syslog*  
  - *Manual Upload*  
  - *Port Forwarding*  

- **Log Sources** — Windows logs, Linux logs (`/var/log/`), Apache logs, etc. are all central to SIEM detection capabilities.  
- **Correlation Rules** — Logic-based triggers that raise alerts when specific patterns occur in the logs (e.g. multiple failed logins, execution of `whoami`, Event ID 104 for log clearing).  
- **Dashboards** — Visual displays of alerts, system health, failed login attempts, top domains, and more — used for quick monitoring.

---

### 🛠️ Tools Used
- **SIEM Dashboard** (simulated in lab) — Showed alert triggers, user and process attribution, and correlation rule matching.  
- **Event IDs** — Used to define rule conditions, e.g.:
  - `104` – Log cleared
  - `4688` – Process execution

---

### ⚠️ Challenges Faced
- Understanding how a single suspicious process (like `cudominer.exe`) could trigger an alert using just a keyword match (`miner`).
- Matching field-value conditions and identifying which part of the rule caused the alert.

---

### 🧠 What I Learned
- SIEMs provide real-time monitoring and alerting across complex infrastructure.
- Correlation rules are essential for catching threats based on logic, not just individual events.
- Analysts must constantly investigate alerts, decide true vs false positives, and tune rules accordingly.
- The SOC team depends on SIEM tools for visibility, threat hunting, and historical investigation.

---

### 🌐 Real-World Application:
> In real SOC environments, SIEM tools are used daily to detect attacks in progress, respond to incidents faster, and maintain compliance. SIEMs are the backbone of cyber defence in enterprise settings.

---

### 💭 Reflections:
- I enjoyed the lab simulation — it made the workflow from alert to investigation feel real. 
