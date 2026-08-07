# 🛡️ PayPal Phishing Email Investigation

<p align="left">

<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />
<img src="https://img.shields.io/badge/Severity-High-red?style=for-the-badge" />
<img src="https://img.shields.io/badge/Case-02-blue?style=for-the-badge" />
<img src="https://img.shields.io/badge/Incident-Credential%20Harvesting-darkred?style=for-the-badge" />
<img src="https://img.shields.io/badge/Target-PayPal-00457C?style=for-the-badge" />
<img src="https://img.shields.io/badge/Platform-Kali%20Linux-557C94?style=for-the-badge" />
<img src="https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-orange?style=for-the-badge" />
<img src="https://img.shields.io/badge/IOC-Extracted-success?style=for-the-badge" />
<img src="https://img.shields.io/badge/Threat%20Intel-Completed-yellow?style=for-the-badge" />

</p>

---

# 📖 Overview

This repository documents a complete **Digital Forensics and Incident Response (DFIR)** investigation of a **PayPal phishing email**.

The investigation follows a structured workflow used by SOC analysts to determine the legitimacy of the email, identify attacker infrastructure, extract Indicators of Compromise (IOCs), perform threat intelligence analysis, map attacker behavior using the **MITRE ATT&CK Framework**, assess organizational risk, and produce a professional incident report.

---

# 📑 Table of Contents

- Project Objectives
- Investigation Workflow
- Tools & Technologies
- Repository Structure
- Investigation Reports
- Indicators of Compromise
- MITRE ATT&CK Mapping
- Investigation Summary
- Skills Demonstrated
- License

---

# 🎯 Project Objectives

- Perform a complete phishing email investigation.
- Analyze SMTP headers and routing.
- Validate SPF, DKIM, and DMARC authentication.
- Investigate sender identity.
- Analyze HTML email content.
- Investigate embedded URLs.
- Perform threat intelligence analysis.
- Extract Indicators of Compromise (IOCs).
- Map attacker behavior to MITRE ATT&CK.
- Assess organizational risk.
- Produce a professional incident report.

---

# 🔍 Investigation Workflow

```text
Evidence Collection
        │
        ▼
Initial Triage
        │
        ▼
Header Analysis
        │
        ▼
Routing Analysis
        │
        ▼
Authentication Analysis
        │
        ▼
Sender Analysis
        │
        ▼
Content Analysis
        │
        ▼
URL Analysis
        │
        ▼
Attachment Analysis
        │
        ▼
IOC Extraction
        │
        ▼
Threat Intelligence
        │
        ▼
MITRE ATT&CK Mapping
        │
        ▼
Risk Assessment
        │
        ▼
Containment Recommendations
        │
        ▼
Incident Report
        │
        ▼
Lessons Learned
```

---

# 🛠️ Tools & Technologies

## Operating System

- Kali Linux

## Linux Utilities

- grep
- cat
- less
- file
- whois

## Threat Intelligence Platforms

- VirusTotal
- URLScan.io
- Cisco Talos Intelligence
- AbuseIPDB
- MXToolbox

## Frameworks

- MITRE ATT&CK
- DFIR Methodology

---

# 📂 Repository Structure

```text
Case-02-PayPal/
│
├── Evidence/
│
├── Analysis/
│   ├── Initial-Triage.md
│   ├── Header-Analysis.md
│   ├── Routing-Analysis.md
│   ├── Authentication-Analysis.md
│   ├── Sender-Analysis.md
│   ├── Content-Analysis.md
│   ├── URL-Analysis.md
│   ├── Attachment-Analysis.md
│   ├── IOC-Extraction.md
│   ├── Threat-Intelligence.md
│   ├── MITRE-Mapping.md
│   ├── Risk-Assessment.md
│   ├── Containment-Recommendations.md
│   ├── Incident-Report.md
│   └── Lessons-Learned.md
│
├── Screenshots/
│
└── README.md
```

---

# 📚 Investigation Reports

| Phase | Status |
|:------|:------:|
| Initial Triage | ✅ |
| Header Analysis | ✅ |
| Routing Analysis | ✅ |
| Authentication Analysis | ✅ |
| Sender Analysis | ✅ |
| Content Analysis | ✅ |
| URL Analysis | ✅ |
| Attachment Analysis | ✅ |
| IOC Extraction | ✅ |
| Threat Intelligence | ✅ |
| MITRE ATT&CK Mapping | ✅ |
| Risk Assessment | ✅ |
| Containment Recommendations | ✅ |
| Incident Report | ✅ |
| Lessons Learned | ✅ |

---

# 🚨 Indicators of Compromise (IOCs)

| IOC Type | Value |
|----------|-------|
| Sender Email | service@stayfriends.de |
| Return-Path | return@messagsgerocappuccino.it |
| Source IP | 77.91.100.118 |
| Suspicious Domain | easilett.com |
| Legitimate Domain | fonts.googleapis.com |

---

# 🛡️ MITRE ATT&CK Mapping

| ATT&CK ID | Technique |
|------------|-----------------------------|
| T1566 | Phishing |
| T1566.002 | Spearphishing Link |
| T1036 | Masquerading |
| T1204.001 | User Execution: Malicious Link |
| T1583.001 | Acquire Infrastructure: Domains |
| T1585.001 | Establish Accounts |

---

# 📊 Investigation Summary

| Category | Result |
|----------|--------|
| Incident Type | Credential Harvesting Phishing |
| Target Brand | PayPal |
| Severity | High |
| Malware | No |
| Attachments | None |
| IOC Count | Multiple |
| Threat Intelligence | Completed |
| MITRE Mapping | Completed |
| Final Status | Investigation Completed |

---

# 🎓 Skills Demonstrated

- Digital Forensics
- Incident Response
- Email Forensics
- Header Analysis
- SMTP Routing Analysis
- SPF, DKIM & DMARC Validation
- Sender Verification
- HTML Email Analysis
- URL Investigation
- IOC Extraction
- Threat Intelligence
- VirusTotal Analysis
- Cisco Talos Intelligence
- URLScan.io
- WHOIS Analysis
- AbuseIPDB
- MXToolbox
- MITRE ATT&CK Mapping
- Risk Assessment
- Technical Documentation

---

# 📝 Executive Summary

The investigation confirmed that the email is a **credential harvesting phishing campaign** impersonating the PayPal brand.

The attacker relied on social engineering, HTML email content, and embedded hyperlinks to redirect users toward attacker-controlled infrastructure.

A structured DFIR methodology was followed to validate the attack, identify Indicators of Compromise (IOCs), perform threat intelligence analysis, assess organizational risk, and produce actionable containment recommendations.

---

# 📜 License

This repository is intended for **educational purposes**, **cybersecurity training**, and **portfolio demonstration**. All analysis was performed in a controlled environment for defensive security research.
