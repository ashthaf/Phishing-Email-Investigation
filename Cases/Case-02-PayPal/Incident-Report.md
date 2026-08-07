# 📋 Incident Report

![Case](https://img.shields.io/badge/Case-02-blue)
![Category](https://img.shields.io/badge/Category-Phishing%20Investigation-red)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Report](https://img.shields.io/badge/Type-Incident%20Report-orange)

---

# Overview

This document provides a high-level summary of the phishing email investigation conducted for **Case-02 – PayPal Phishing Email**.

The investigation followed a structured Digital Forensics and Incident Response (DFIR) methodology to analyze the phishing email, identify attacker infrastructure, extract Indicators of Compromise (IOCs), validate findings using threat intelligence, assess organizational risk, and recommend appropriate containment actions.

The detailed technical report is available in the Analysis directory.

---

# Investigation Summary

| Item | Value |
|------|-------|
| Case ID | Case-02 |
| Incident Type | Phishing Email |
| Impersonated Brand | PayPal |
| Investigation Status | Completed |
| Severity | High |
| Malware Delivered | No |
| Primary Objective | Credential Harvesting |

---

# Investigation Phases

The investigation included the following phases:

- Initial Triage
- Header Analysis
- Routing Analysis
- Authentication Analysis
- Sender Analysis
- Content Analysis
- URL & Domain Analysis
- Attachment Analysis
- IOC Extraction
- Threat Intelligence Analysis
- MITRE ATT&CK Mapping
- Risk Assessment
- Containment Recommendations
- Lessons Learned

---

# Key Findings

- The email impersonated the PayPal brand.
- The campaign relied on social engineering techniques.
- Embedded hyperlinks redirected victims to attacker-controlled infrastructure.
- No malware attachments were present.
- Multiple Indicators of Compromise (IOCs) were successfully extracted.
- Threat intelligence confirmed suspicious infrastructure associated with the campaign.
- Overall risk was assessed as **High**.

---

# Evidence

The investigation included analysis of:

- Original email sample
- Email headers
- SMTP routing
- Authentication results
- HTML content
- Embedded URLs
- DNS records
- Threat intelligence sources
- IOC extraction

---

# Detailed Report

The complete technical report is available here:

```text
Analysis/14-Incident-Report.md
```

---

# Related Documents

- `Investigation.md`
- `Timeline.md`
- `Analysis/`
- `Evidence/`
- `Headers/`
- `IOCs/`

---

# Conclusion

The investigation confirmed that the email is a **credential harvesting phishing campaign** leveraging trusted branding, malicious hyperlinks, and attacker-controlled infrastructure. The findings, evidence, extracted IOCs, and recommended containment measures have been fully documented throughout this case repository.
