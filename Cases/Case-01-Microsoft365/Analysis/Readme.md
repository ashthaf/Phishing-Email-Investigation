![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Case](https://img.shields.io/badge/Case-01-blue)
![Threat](https://img.shields.io/badge/Threat-Credential_Harvesting-red)
![Platform](https://img.shields.io/badge/Platform-Microsoft_365-0078D4)
![Investigation](https://img.shields.io/badge/Type-Phishing_Investigation-purple)
![MITRE ATT&CK](https://img.shields.io/badge/Framework-MITRE_ATT%26CK-orange)
# CASE-01 Technical Analysis

## Overview

This directory contains the complete technical analysis performed during the investigation of **CASE-01 – Microsoft 365 Credential Harvesting Phishing Email**.

The analysis follows a structured Digital Forensics and Incident Response (DFIR) workflow, beginning with **Initial Triage** and progressing through technical validation, threat intelligence enrichment, risk assessment, incident reporting, and lessons learned.

> **Note:** Evidence acquisition, preservation, chain of custody, and original email storage are documented separately within the **Evidence**, **Headers**, **Artifacts**, and **IOCs** directories. This directory focuses exclusively on the technical investigation and analysis process.

---

# Investigation Workflow

| Phase | Description |
|--------|-------------|
| 01 | Initial Triage |
| 02 | Header Analysis |
| 03 | Routing Analysis |
| 04 | Authentication Analysis |
| 05 | Sender Analysis |
| 06 | Content Analysis |
| 07 | URL Analysis |
| 08 | Attachment Analysis |
| 09 | IOC Extraction |
| 10 | Threat Intelligence |
| 11 | MITRE ATT&CK Mapping |
| 12 | Risk Assessment |
| 13 | Containment Recommendations |
| 14 | Incident Report |
| 15 | Lessons Learned |

---

# Analysis Objectives

The primary objectives of this investigation were to:

- Preserve forensic integrity throughout the investigation.
- Determine whether the email was malicious.
- Identify phishing techniques used by the attacker.
- Validate sender authenticity.
- Analyze email authentication mechanisms.
- Examine email routing and delivery path.
- Investigate embedded URLs.
- Extract Indicators of Compromise (IOCs).
- Correlate findings using multiple OSINT and threat intelligence platforms.
- Map observed attacker behavior to the MITRE ATT&CK framework.
- Assess organizational risk.
- Produce actionable containment and remediation recommendations.

---

# Investigation Tools

The following tools were used throughout the analysis:

### Email & Forensic Analysis

- Thunderbird
- ripMIME
- grep
- less
- cat
- file
- md5sum
- sha256sum

### DNS & Infrastructure Analysis

- dig
- host
- nslookup
- MXToolbox

### Threat Intelligence

- VirusTotal
- URLScan.io
- Cisco Talos Intelligence
- AbuseIPDB
- PhishTank
- EmailRep

### Operating System

- Kali Linux

---

# Investigation Methodology

The investigation followed a layered approach:

1. Initial triage
2. Email header extraction
3. Mail routing reconstruction
4. Authentication verification (SPF, DKIM, DMARC)
5. Sender verification
6. Content inspection
7. URL investigation
8. IOC extraction
9. Threat intelligence correlation
10. MITRE ATT&CK mapping
11. Risk assessment
12. Incident reporting
13. Lessons learned

---

# Case Summary

The analyzed email was identified as a **credential harvesting phishing attack** targeting Microsoft 365 users.

Key findings include:

- Credential harvesting through a Firebase-hosted phishing page.
- URL shortening used to conceal the phishing destination.
- Abuse of legitimate cloud infrastructure.
- Social engineering techniques designed to create urgency.
- No malware attachments or executable payloads were identified.

---

# Related Directories

| Directory | Purpose |
|-----------|---------|
| Evidence | Original email and forensic evidence |
| Headers | Extracted email headers |
| URLs | URL investigation artifacts |
| IOCs | Extracted indicators of compromise |
| Artifacts | Raw extracted investigation artifacts |
| Screenshots | Visual evidence supporting each investigation phase |

---

# Notes

This case represents a complete end-to-end phishing email investigation conducted using forensic best practices and publicly available threat intelligence sources.

The methodology documented here is reusable for future phishing investigations and serves as the foundation for subsequent case studies within this repository.
