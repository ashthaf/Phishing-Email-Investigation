# 📄 Phase 14 – Incident Report

![Status](https://img.shields.io/badge/Status-Completed-44CC11)
![Phase](https://img.shields.io/badge/Phase-14-blue)
![Category](https://img.shields.io/badge/Category-Incident%20Report-red)
![Case](https://img.shields.io/badge/Case-02-blue)
![Verdict](https://img.shields.io/badge/Verdict-Credential%20Harvesting%20Phishing-critical)

---

# 📖 Overview

This report summarizes the complete phishing email investigation conducted throughout the Digital Forensics and Incident Response (DFIR) process.

It consolidates the evidence collected, investigation findings, extracted Indicators of Compromise (IOCs), Threat Intelligence results, MITRE ATT&CK mapping, risk assessment, and recommended containment measures into a single incident report.

---

# 🎯 Objectives

- Summarize the complete phishing investigation.
- Document the scope and methodology of the investigation.
- Present the key technical findings.
- Record the extracted Indicators of Compromise (IOCs).
- Summarize the overall risk and incident severity.
- Provide a final incident assessment and recommendations.

---

# Executive Summary

A phishing email impersonating the PayPal brand was investigated to determine its legitimacy, identify the attacker's infrastructure, and assess the potential impact on users and the organization.

The investigation followed a structured Digital Forensics and Incident Response (DFIR) methodology, including initial triage, email header analysis, routing analysis, authentication verification, sender analysis, content analysis, URL investigation, attachment analysis, IOC extraction, Threat Intelligence analysis, MITRE ATT&CK mapping, risk assessment, and containment planning.

The investigation concluded that the email is a **credential harvesting phishing campaign** designed to deceive recipients into interacting with attacker-controlled infrastructure through embedded hyperlinks. No malware or malicious attachments were identified.

---

# Incident Overview

| Item | Details |
| -------------------- | --------------------- |
| Incident Type | Phishing Email |
| Target Brand | PayPal |
| Investigation Status | Completed |
| Overall Severity | High |
| Malware Delivered | No |
| Primary Objective | Credential Harvesting |
| Analyst | Abdull Ashthaf CK |

---

# Scope of Investigation

The investigation included analysis of:

- Original email evidence
- Email headers
- SMTP routing
- Email authentication mechanisms
- Sender identity
- HTML email content
- Embedded URLs
- Domains
- Attachments
- Indicators of Compromise (IOCs)
- Threat Intelligence
- MITRE ATT&CK mapping
- Risk assessment

---

# Investigation Timeline

| Phase | Status |
| ----------------------- | --------- |
| Initial Triage | Completed |
| Header Analysis | Completed |
| Routing Analysis | Completed |
| Authentication Analysis | Completed |
| Sender Analysis | Completed |
| Content Analysis | Completed |
| URL Analysis | Completed |
| Attachment Analysis | Completed |
| IOC Extraction | Completed |
| Threat Intelligence | Completed |
| MITRE ATT&CK Mapping | Completed |
| Risk Assessment | Completed |
| Containment Planning | Completed |

---

# Investigation Findings

## Email Authentication

Analysis of SPF, DKIM, and DMARC records showed inconsistencies within the phishing infrastructure.

The sender and Return-Path information indicated suspicious email routing commonly observed in phishing campaigns.

---

## Sender Analysis

The visible sender address was:

```
service@stayfriends.de
```

The Return-Path was:

```
return@messagsgerocappuccino.it
```

The sender domain itself was found to be legitimate, while the Return-Path domain appeared suspicious and no longer actively registered.

---

## URL Analysis

The phishing email contained embedded hyperlinks leading to external infrastructure.

Primary suspicious domain:

```
easilett.com
```

Legitimate resource identified:

```
fonts.googleapis.com
```

Threat Intelligence analysis identified **easilett.com** as the primary suspicious infrastructure associated with the phishing campaign.

---

## Attachment Analysis

No file attachments were identified.

The phishing campaign relied entirely on HTML content and embedded hyperlinks rather than malware delivery.

---

# Indicators of Compromise (IOCs)

| IOC Type | Value |
| ----------------- | -------------------------------------------------------------------------- |
| Sender Email | `service@stayfriends.de` |
| Return-Path | `return@messagsgerocappuccino.it` |
| Source IP | `77.91.100.118` |
| Suspicious Domain | `easilett.com` |
| Legitimate Domain | `fonts.googleapis.com` |

---

# Threat Intelligence Summary

Multiple Threat Intelligence platforms were used to validate the extracted IOCs.

Platforms consulted:

- VirusTotal
- URLScan.io
- Cisco Talos Intelligence
- AbuseIPDB
- WHOIS
- MXToolbox

Key findings include:

- **easilett.com** was identified as suspicious.
- VirusTotal reported one phishing detection.
- The domain lacked SPF and DMARC records.
- Cisco Talos reported a neutral reputation.
- AbuseIPDB reported no historical abuse.
- WHOIS indicated a relatively new domain registration.

The sender domain (**stayfriends.de**) maintained a favorable reputation and appeared legitimate.

---

# MITRE ATT&CK Mapping

The phishing campaign was mapped to the following ATT&CK techniques.

| ATT&CK ID | Technique |
| --------- | ------------------------------- |
| T1566 | Phishing |
| T1566.002 | Spearphishing Link |
| T1036 | Masquerading |
| T1204.001 | User Execution: Malicious Link |
| T1583.001 | Acquire Infrastructure: Domains |
| T1585.001 | Establish Accounts |

The campaign relied primarily on social engineering rather than malware execution.

---

# Risk Assessment Summary

| Category | Assessment |
| ---------------------- | ---------- |
| Likelihood | High |
| Confidentiality Impact | High |
| Integrity Impact | Medium |
| Availability Impact | Low |
| Overall Risk | High |

Successful exploitation could result in:

- Credential theft
- Unauthorized account access
- Financial fraud
- Exposure of sensitive information
- Reputational damage

---

# Containment Actions

The following containment measures were recommended:

- Block **easilett.com** at DNS, firewall, and secure web gateways.
- Monitor or block **77.91.100.118** where appropriate.
- Quarantine similar phishing emails.
- Notify affected users.
- Reset compromised credentials.
- Enable Multi-Factor Authentication (MFA).
- Strengthen SPF, DKIM, and DMARC enforcement.
- Update phishing detection rules.

---

# 💡 Analyst Assessment

The investigation confirmed that the phishing campaign relied on social engineering, trusted branding, and attacker-controlled infrastructure rather than malware delivery.

The combination of HTML phishing content, embedded hyperlinks, suspicious routing infrastructure, and credential harvesting techniques demonstrates a well-structured phishing campaign designed to maximize user interaction.

The extracted Indicators of Compromise (IOCs), Threat Intelligence findings, and MITRE ATT&CK mapping provide sufficient evidence to classify this incident as a **High Severity Credential Harvesting Phishing Campaign**.

---

# Final Verdict

Based on the technical investigation, Threat Intelligence findings, and MITRE ATT&CK mapping, the email has been confirmed as a **credential harvesting phishing campaign**.

The attack leveraged social engineering, trusted branding, and attacker-controlled infrastructure to increase the likelihood of user interaction.

No malware payloads or malicious attachments were identified. Instead, the attacker relied entirely on HTML content and embedded hyperlinks to redirect victims to external phishing infrastructure.

The campaign presents a **High** risk to users and organizations due to the potential for credential compromise and unauthorized account access.

---

# Recommendations

To reduce the likelihood of similar phishing attacks, organizations should:

- Conduct regular phishing awareness training.
- Enforce Multi-Factor Authentication (MFA).
- Strengthen SPF, DKIM, and DMARC policies.
- Block identified malicious domains and infrastructure.
- Continuously monitor Threat Intelligence feeds.
- Implement advanced email filtering and anti-phishing controls.
- Encourage prompt reporting of suspicious emails.

---

# ✅ Conclusion

The investigation successfully identified the phishing infrastructure, extracted actionable Indicators of Compromise (IOCs), validated them using multiple Threat Intelligence platforms, and mapped the observed attacker behavior to the MITRE ATT&CK framework.

The structured investigation methodology provided a comprehensive understanding of the phishing campaign and produced actionable recommendations for improving organizational defenses against future phishing attacks.

---

# ➡️ Next Phase

Continue to **Phase 15 – Lessons Learned** to summarize the key takeaways from the investigation and identify improvements for future phishing investigations and incident response activities.
