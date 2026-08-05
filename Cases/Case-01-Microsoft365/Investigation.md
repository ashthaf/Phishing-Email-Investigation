# CASE-01 Investigation Summary

## Overview

This investigation documents the analysis of a Microsoft 365 credential phishing email received in EML format. The objective was to determine the legitimacy of the email, identify indicators of compromise (IOCs), assess the associated risk, and document the complete investigation following the Master Phishing Investigation Playbook.

The investigation was performed using a hybrid methodology that combined command-line forensic analysis with open-source threat intelligence platforms.

---

# Case Information

| Field | Value |
|-------|-------|
| Case ID | CASE-01 |
| Case Name | Microsoft 365 Credential Phishing Investigation |
| Email Platform | Microsoft 365 |
| Evidence Format | EML |
| Analyst | Abdull Ashthaf CK |
| Status | Completed |

---

# Investigation Objectives

- Preserve original evidence
- Verify email authenticity
- Analyze message headers
- Reconstruct the delivery path
- Verify SPF, DKIM, and DMARC authentication
- Identify sender impersonation techniques
- Analyze embedded URLs
- Determine whether attachments were present
- Extract Indicators of Compromise (IOCs)
- Perform Threat Intelligence enrichment
- Map attacker behavior to MITRE ATT&CK
- Assess business risk
- Provide containment recommendations

---

# Investigation Workflow

The investigation followed the Master Phishing Investigation Playbook.

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
14. Incident Report
15. Lessons Learned

---

# Investigation Tools

## Command-Line Tools

- ripMIME
- grep
- file
- sha256sum
- md5sum

## Threat Intelligence Platforms

- VirusTotal
- Cisco Talos Intelligence
- AbuseIPDB
- URLScan.io
- PhishTank

---

# Key Findings

- The email successfully passed SPF, DKIM, and DMARC authentication.
- The sender abused legitimate cloud email infrastructure.
- Social engineering techniques were used to impersonate a Microsoft 365 password reset notification.
- A shortened URL redirected users toward a Firebase-hosted page.
- No malicious attachments were included in the email.
- Multiple phishing indicators were identified despite successful email authentication.
- Threat intelligence supported the phishing assessment.

---

# Investigation Outcome

The email was determined to be a credential phishing attempt designed to deceive recipients into interacting with a malicious password reset link.

The attacker relied on trusted third-party infrastructure and social engineering rather than malware or malicious attachments.

Overall Risk Rating: **High**

---

# Investigation Structure

```
Case-01-Microsoft365
│
├── Analysis/
├── Evidence/
├── Headers/
├── URLs/
├── IOCs/
├── Artifacts/
├── Attachments/
├── Screenshots/
├── Timeline.md
├── Investigation.md
└── Incident-Report.md
```

---

# Related Documentation

Detailed technical findings are available in the `Analysis` directory, where each investigation phase is documented individually according to the Master Phishing Investigation Playbook.
