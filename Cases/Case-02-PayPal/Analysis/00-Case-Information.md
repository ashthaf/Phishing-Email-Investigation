# 📁 Case Information

![Status](https://img.shields.io/badge/Status-Completed-44CC11)
![Case](https://img.shields.io/badge/Case-02-blue)
![Category](https://img.shields.io/badge/Category-Phishing-red)
![Severity](https://img.shields.io/badge/Severity-High-red)
![Framework](https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-orange)

---

# 📖 Overview

This case documents the investigation of a phishing email impersonating **PayPal**. The objective was to determine whether the email was malicious, identify attacker infrastructure, extract Indicators of Compromise (IOCs), map attacker techniques to the MITRE ATT&CK framework, and provide containment recommendations.

The investigation followed a structured Digital Forensics and Incident Response (DFIR) workflow from initial evidence collection through final reporting.

---

# 🎯 Investigation Objectives

- Determine whether the email is malicious.
- Identify sender infrastructure.
- Verify SPF, DKIM, and DMARC authentication.
- Analyze embedded URLs.
- Investigate sender reputation.
- Extract Indicators of Compromise (IOCs).
- Perform Threat Intelligence lookups.
- Map attacker techniques to MITRE ATT&CK.
- Assess organizational risk.
- Recommend containment actions.

---

# 📋 Case Summary

| Item | Value |
|------|-------|
| Case ID | 02 |
| Incident Type | PayPal Credential Harvesting Phishing |
| Severity | High |
| Status | Completed |
| Malware Attachment | No |
| Primary Goal | Credential Theft |
| Target Brand | PayPal |
| Analyst | Abdull Ashthaf CK |
| Investigation Platform | Kali Linux |

---

# 📂 Evidence Collected

| Evidence | Description |
|----------|-------------|
| Original Email | Raw phishing email |
| Email Headers | SMTP routing information |
| HTML Source | Email body source code |
| Embedded URLs | Phishing and legitimate links |
| WHOIS Data | Domain registration information |
| Threat Intelligence | Reputation data from OSINT platforms |

---

# 🛠️ Investigation Methodology

The investigation followed the workflow below:

1. Initial Triage
2. Header Analysis
3. Routing Analysis
4. Authentication Analysis
5. Sender Analysis
6. Content Analysis
7. URL Analysis
8. Attachment Analysis
9. IOC Extraction
10. Threat Intelligence
11. MITRE ATT&CK Mapping
12. Risk Assessment
13. Containment Recommendations
14. Incident Reporting
15. Lessons Learned

---

# 🔧 Tools Used

## Operating System

- Kali Linux

## Linux Utilities

- grep
- cat
- less
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

# 📈 Investigation Outcome

The investigation confirmed that the email is a **credential harvesting phishing attack** impersonating PayPal. The attacker relied on deceptive branding and malicious links to redirect users to attacker-controlled infrastructure with the objective of stealing account credentials.

Multiple Indicators of Compromise (IOCs) were identified, threat intelligence analysis was completed, and attacker techniques were successfully mapped to the MITRE ATT&CK framework.

---

# ✅ Next Phase

➡️ Continue to **01-Initial-Triage.md** for the initial assessment of the phishing email.
