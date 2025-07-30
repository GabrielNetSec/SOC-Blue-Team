# Memory Forensics Investigation – ECE570 Project

---

## 🕵️‍♂️ Overview

This project involved a forensic investigation of a compromised Windows 7 machine using a memory dump.  
The objective was to **identify evidence of malicious activity**, including hidden processes, injected code, suspicious registry hives, and potential indicators of remote command-and-control (C2) communications.

Tools used include **Volatility**, **VirusTotal**, **CrackStation**, and standard Linux shell commands.

---

## 🧰 Tools & Plugins Used

- `Volatility v2.6`: imageinfo, pslist, pstree, malfind, ldrmodules, procdump, hivelist, hashdump
- `VirusTotal`: executable & URL scanning
- `CrackStation`: NTLM hash cracking
- `Regripper`: registry hive analysis
- `nslookup`, `strings`, `bash`

---

## 🔍 Key Findings

### 🧠 Suspicious Processes
Identified unusual and short-lived processes with non-standard names and parent-child relationships, suggesting scripted or automated behavior:
- `aifkydk.exe`, `7004af389d633b`, `bcdedit.exe`, `vssadmin.exe`, `cmd.exe`, `iexplore.exe`

### 📈 Process Tree & Initial Entry Point
Using `pstree`, traced all activity back to:
- **Initial exploit process:** `7004af389d633b`
- Responsible for spawning all other suspicious subprocesses

### 🧬 Code Injection & Hidden DLLs
- `malfind` revealed suspicious memory regions in `iexplore.exe`
- DLL loaded from `\tmp\ifsubua\bin\monitor-x86.dll`
- Hidden modules found using `ldrmodules`
- Executable dumped with `procdump` → flagged as malicious by CrowdStrike Falcon on VirusTotal

### 🌐 Command & Control Indicators
- Malicious URLs extracted from memory strings (via `strings`)
- VirusTotal flagged multiple URLs as phishing/malware
- IPs resolved with `nslookup` (though domains inactive)

### 🛠 Registry Analysis & Password Hashes
- Identified unnamed registry hive and analyzed with `hivelist`, `hivedump`, and `Regripper`
- SAM and SYSTEM hives revealed same NTLM hash for all accounts
- NTLM hash could not be cracked → indicates strong or blank password

---

## 🧠 Learning Outcomes

- Gained hands-on experience with full memory forensic workflow
- Applied plugins for process analysis, code injection detection, and registry parsing
- Correlated malware activity through process trees and command-line artifacts
- Validated malicious behavior through VirusTotal and public tools
- Practiced practical memory forensics aligned with real-world incident response

---
