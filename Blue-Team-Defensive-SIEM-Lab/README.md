# Blue Team Defensive Lab

## Overview

This project documents a Blue Team lab focused on vulnerability analysis, detection validation, and network hardening.

The lab combined vulnerability scanning, prioritization of findings, firewall and IPS policy enforcement, SIEM log ingestion, and alert validation using Splunk. Detection activity was also mapped to MITRE ATT&CK techniques to support structured defensive analysis.

## Objectives

- Perform vulnerability analysis using Nmap and Nessus
- Identify and prioritize relevant findings
- Apply network hardening through Palo Alto firewall and IPS policies
- Ingest firewall and system logs into Splunk SIEM
- Validate security detections using log analysis and alert review
- Map observed activity and detections to MITRE ATT&CK

## Tools and Technologies

- Nmap
- Nessus
- Palo Alto Firewall / IPS
- Splunk SIEM
- MITRE ATT&CK

## Lab Activities

### 1. Vulnerability Analysis
Performed vulnerability identification and service enumeration using Nmap and Nessus. Findings were reviewed and prioritized based on exposure, severity, and defensive relevance.

### 2. Network Hardening
Applied hardening controls using Palo Alto firewall and IPS policies to reduce attack surface and improve filtering and detection coverage.

### 3. SIEM Log Ingestion
Collected and ingested firewall and system logs into Splunk to support centralized visibility and event analysis.

### 4. Detection Validation
Validated detections by reviewing Splunk events, correlation behavior, and alert visibility after hardening changes and simulated activity.

### 5. MITRE ATT&CK Mapping
Mapped relevant alerts and observed behaviors to MITRE ATT&CK techniques to support structured threat analysis and defensive documentation.

## Validation Performed

- Nmap service and exposure verification
- Nessus vulnerability identification and prioritization
- Firewall / IPS policy validation
- Splunk log ingestion confirmation
- Detection review in Splunk
- MITRE ATT&CK mapping of relevant alerts

## Repository Structure

- `screenshots/` → scan results, policies, dashboards, and SIEM evidence
- `outputs/` → command outputs and validation notes
- `docs/` → methodology, hardening actions, and ATT&CK mapping

## Key Takeaways

This lab demonstrates practical Blue Team skills across vulnerability analysis, defensive hardening, SIEM visibility, and alert validation in a controlled environment.
