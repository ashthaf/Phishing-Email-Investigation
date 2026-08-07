# 🔍 Investigation

![Case](https://img.shields.io/badge/Case-02-blue)
![Category](https://img.shields.io/badge/Category-Phishing%20Email-red)
![Methodology](https://img.shields.io/badge/Method-DFIR-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# Investigation Overview

This document provides an overview of the forensic investigation performed on **Case-02 – PayPal Phishing Email**.

The objective of the investigation was to determine whether the email was malicious, identify the attacker's infrastructure, extract Indicators of Compromise (IOCs), validate findings through threat intelligence, assess organizational risk, and recommend containment measures.

A structured **Digital Forensics and Incident Response (DFIR)** methodology was followed throughout the investigation to ensure evidence integrity and reproducibility.

---

# Investigation Objectives

The investigation aimed to:

- Preserve the original email evidence.
- Analyze the email headers and metadata.
- Reconstruct the SMTP delivery path.
- Verify sender authentication (SPF, DKIM, and DMARC).
- Examine sender-related information.
- Analyze the HTML email content.
- Investigate embedded URLs and domains.
- Determine whether attachments were present.
- Extract actionable Indicators of Compromise (IOCs).
- Validate findings using threat intelligence platforms.
- Map attacker behavior to the MITRE ATT&CK framework.
- Assess the overall security risk.
- Recommend containment and mitigation actions.

---

# Investigation Workflow

The investigation followed the workflow below.

| Phase | Status |
|--------|--------|
| Initial Triage | ✅ Completed |
| Header Analysis | ✅ Completed |
| Routing Analysis | ✅ Completed |
| Authentication Analysis | ✅ Completed |
| Sender Analysis | ✅ Completed |
| Content Analysis | ✅ Completed |
| URL & Domain Analysis | ✅ Completed |
| Attachment Analysis | ✅ Completed |
| IOC Extraction | ✅ Completed |
| Threat Intelligence Analysis | ✅ Completed |
| MITRE ATT&CK Mapping | ✅ Completed |
| Risk Assessment | ✅ Completed |
| Containment Recommendations | ✅ Completed |
| Lessons Learned | ✅ Completed |

---

# Investigation Artifacts

The following evidence and artifacts were collected during the investigation:

- Original phishing email
- Email headers
- SMTP routing information
- HTML email body
- URL extraction
- Domain intelligence
- IOC lists
- Threat intelligence results
- Investigation screenshots
- Chain of custody documentation

---

# Directory Structure

```
Case-02-PayPal/
├── Analysis/
├── Artifacts/
├── Attachments/
├── Evidence/
├── Headers/
├── IOCs/
├── Screenshots/
├── Incident-Report.md
├── Investigation.md
└── Timeline.md
```

---

# Analysis Documents

Detailed findings are documented within the **Analysis** directory.

| Phase | Document |
|--------|----------|
| Initial Triage | Analysis/01-Initial-Triage.md |
| Header Analysis | Analysis/02-Header-Analysis.md |
| Routing Analysis | Analysis/03-Routing-Analysis.md |
| Authentication Analysis | Analysis/04-Authentication-Analysis.md |
| Sender Analysis | Analysis/05-Sender-Analysis.md |
| Content Analysis | Analysis/06-Content-Analysis.md |
| URL & Domain Analysis | Analysis/07-URL-Domain-Analysis.md |
| Attachment Analysis | Analysis/08-Attachment-Analysis.md |
| IOC Extraction | Analysis/09-IOC-Extraction.md |
| Threat Intelligence | Analysis/10-Threat-Intelligence.md |
| MITRE ATT&CK Mapping | Analysis/11-MITRE-Mapping.md |
| Risk Assessment | Analysis/12-Risk-Assessment.md |
| Containment Recommendations | Analysis/13-Containment-Recommendations.md |
| Incident Report | Analysis/14-Incident-Report.md |
| Lessons Learned | Analysis/15-Lessons-Learned.md |

---

# Investigation Outcome

The investigation confirmed that the email is a **credential harvesting phishing campaign** impersonating the PayPal brand.

The campaign relied on:

- Social engineering
- HTML email content
- Embedded phishing hyperlinks
- Attacker-controlled infrastructure

No malware attachments were identified. Instead, the attacker attempted to redirect recipients to an external phishing website designed to steal credentials.

---

# Related Documents

- Incident-Report.md
- Timeline.md
- Evidence/
- Headers/
- IOCs/
- Artifacts/
- Analysis/

---

# Conclusion

This investigation successfully followed a structured DFIR methodology from evidence collection through final reporting. The investigation produced actionable Indicators of Compromise (IOCs), validated attacker infrastructure through threat intelligence, assessed the associated risk, and documented recommendations to strengthen defenses against similar phishing campaigns.
