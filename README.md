# SOC / Blue Team Projects

🛡️ **Blue Team Portfolio – Gabriel Naranjo**  
This repository contains a collection of cybersecurity defense projects focused on **intrusion detection, incident response, and memory forensics**. The goal is to showcase practical skills in monitoring, defending, and analyzing compromised systems using industry-standard tools and academic methodologies.

---

## 📁 Projects

### 🔹 ECE567 – Network Defense Strategies  
**[View Project →](./ECE567-Defense-Strategies)**  
Course: Advanced Network Security – University of Victoria  

Designed and implemented a complete **host-based intrusion detection and prevention** setup to defend against NFS exploitation (CVE-1999-0170).  
- ✅ Created custom Snort rules to detect suspicious NFS activity (ports 111/2049)
- ✅ Configured IPTables firewall on the vulnerable host to allow access only from whitelisted IPs
- ✅ Validated alerts and blocking behavior through simulated attack scenarios
- ✅ Recommended hardening strategies: export restrictions, service disabling, and system updates

### 🔹 ECE570 – Memory Forensics Investigation  
**[View Project →](./ECE570-Memory-Forensics-Investigation)**  
Course: Computer Forensics Methodologies – University of Victoria  

Performed full forensic analysis on a compromised Windows 7 memory image.  
- 🔍 Identified suspicious processes and command injection behavior  
- 🧠 Detected hidden DLLs and injected code using Volatility (`malfind`, `ldrmodules`)  
- 🧪 Verified extracted executables via VirusTotal  
- 🌐 Flagged malicious URLs and matched them with IPs  
- 🧾 Parsed suspicious registry hives and extracted NTLM hashes for analysis  

### 🔹 Blue Team Defensive Lab  
**[View Project →](./Blue-Team-Defensive-Lab)**  

Performed vulnerability analysis using Nessus and Nmap, prioritized findings, and applied network hardening through Palo Alto firewall and IPS policies. Ingested firewall and system logs into Splunk SIEM, validated detections, and mapped alerts to MITRE ATT&CK.
- ✅ Performed service enumeration and vulnerability analysis with Nmap and Nessus
- ✅ Prioritized findings based on exposure and defensive relevance
- ✅ Applied hardening through Palo Alto firewall and IPS policies
- ✅ Ingested firewall and system logs into Splunk SIEM
- ✅ Validated detections and mapped alerts to MITRE ATT&CK

---

## 🧰 Tools & Technologies

- 🐍 **Snort** (custom rules, signature-based detection)  
- 🔥 **IPTables** (host-based firewall)  
- 🧠 **Volatility v2.6** (memory forensics)  
- 📦 **VirusTotal, CrackStation, Regripper**  
- 🐧 Kali Linux, bash scripting, Windows registry forensics
- 🔎 **Nmap, Nessus** (vulnerability analysis and exposure validation)
- 🧱 **Palo Alto Firewall / IPS** (network hardening and policy enforcement)
- 📊 **Splunk SIEM** (log ingestion, search, and detection validation)
- 🧭 **MITRE ATT&CK** (alert and activity mapping)
---

## 🧠 Skills Demonstrated

- Intrusion detection & rule tuning  
- Incident response & prevention logic  
- Packet-level protocol analysis  
- Memory dump analysis & malware behavior reconstruction  
- Registry artifact extraction  
- Report writing & security validation

---

## 📌 Disclaimer

All work was conducted in **controlled academic environments** for educational purposes only.  
No real systems were accessed or harmed. Ethical standards and UVic guidelines were strictly followed.

---

## 👤 Author

**Gabriel Naranjo**  
