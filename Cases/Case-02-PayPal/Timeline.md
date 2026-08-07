# ⏱️ Investigation Timeline

![Case](https://img.shields.io/badge/Case-02-blue)
![Category](https://img.shields.io/badge/Category-Investigation%20Timeline-purple)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# Overview

This document provides a chronological timeline of the Digital Forensics and Incident Response (DFIR) investigation conducted for **Case-02 – PayPal Phishing Email**.

The timeline summarizes each stage of the investigation from evidence acquisition through final reporting and containment planning.

---

# Investigation Timeline

| Phase | Activity | Status |
|--------|----------|--------|
| 01 | Original phishing email acquired and preserved as evidence | ✅ Completed |
| 02 | Initial triage performed in an isolated virtual machine | ✅ Completed |
| 03 | Email headers extracted for forensic analysis | ✅ Completed |
| 04 | SMTP routing reconstructed using Received headers | ✅ Completed |
| 05 | SPF, DKIM, and DMARC authentication verified | ✅ Completed |
| 06 | Sender and Return-Path analysis completed | ✅ Completed |
| 07 | HTML email body extracted and examined | ✅ Completed |
| 08 | Embedded hyperlinks and domains investigated | ✅ Completed |
| 09 | Attachment analysis performed | ✅ Completed |
| 10 | Indicators of Compromise (IOCs) extracted | ✅ Completed |
| 11 | Threat intelligence validation performed | ✅ Completed |
| 12 | MITRE ATT&CK techniques mapped | ✅ Completed |
| 13 | Risk assessment completed | ✅ Completed |
| 14 | Containment recommendations documented | ✅ Completed |
| 15 | Incident report finalized | ✅ Completed |
| 16 | Lessons learned documented | ✅ Completed |

---

# Investigation Flow

```
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
URL & Domain Analysis
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

# Investigation Outcome

The investigation successfully identified:

- A PayPal-themed credential harvesting phishing campaign.
- Suspicious sender infrastructure.
- Attacker-controlled phishing domains.
- Multiple Indicators of Compromise (IOCs).
- Relevant MITRE ATT&CK techniques.
- Appropriate containment and mitigation recommendations.

---

# Related Documents

- Investigation.md
- Incident-Report.md
- Analysis/
- Evidence/
- Headers/
- IOCs/
- Artifacts/

---

# Summary

The investigation followed a structured Digital Forensics and Incident Response (DFIR) methodology, progressing from evidence preservation through detailed technical analysis to final reporting. Each phase built upon the findings of the previous stage, resulting in a comprehensive assessment of the phishing campaign and actionable recommendations for detection and mitigation.
