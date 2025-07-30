# Network Defense Strategies – ECE567 Project

---

## 🛡️ Overview

This project focuses on defensive strategies to detect and prevent a **realistic NFS exploitation scenario** (CVE-1999-0170) previously identified in a simulated network environment. The goal was to implement and test a complete detection and prevention solution using **Snort IDS** and **IPTables firewall**, while analyzing the behavior of unauthorized traffic and maintaining access for legitimate clients.

---

## 🔍 Project Phases

### 🔎 Phase 1: Intrusion Detection

- **Scenario Analysis:**  
  Described how an attacker can exploit a misconfigured NFS share to access `/home` without authentication using tools like Metasploit or `showmount`.

- **Snort Rule Design:**  
  Developed 3 custom Snort rules to detect:
  - UDP and TCP traffic on port 111 (RPC/MOUNT and PORTMAP)
  - NFS exploitation attempts via TCP port 2049

- **Snort Deployment & Testing:**  
  Deployed Snort in detection mode on host `uranusR`, executed attacks from Kali, and analyzed logs:
  - Detected all attack phases as **true positives**
  - Legitimate internal traffic triggered **no false positives**

### 🚫 Phase 2: Intrusion Prevention

- **IPTables Firewall Configuration:**
  - Applied host-based firewall rules on `uranusZ` to allow only trusted IPs (`uranusN`, `uranusR`) to access NFS and RPC ports
  - Blocked all other traffic, including from Kali (attacker)

- **Validation:**  
  - Verified rule enforcement using test traffic from trusted and untrusted hosts
  - Ensured legitimate NFS clients could mount, while attacker was blocked

### 🔐 Additional Defense Recommendations

- Hardened `/etc/exports` NFS config to restrict access by IP
- Disabled unnecessary services (Nginx over HTTP)
- Applied software updates (OpenSSH, Nginx)
- Recommended removal of legacy services (FTP, Telnet) from other hosts

---

## 📊 Summary of Techniques

| Component         | Tools Used           | Outcome                          |
|------------------|----------------------|----------------------------------|
| Intrusion Detection | Snort IDS             | Detected Metasploit and manual NFS scans |
| Intrusion Prevention | IPTables firewall      | Blocked unauthorized access based on IP |
| Logging & Analysis | Snort logs, Wireshark  | Verified alert accuracy (TP/FP/FN) |
| System Hardening   | Exports config, updates | Reduced exposure and attack surface |

---
