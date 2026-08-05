# Incident Report

## Executive Summary

A phishing email impersonating a Microsoft 365 password reset notification was investigated following the Master Phishing Investigation Playbook.

The email successfully passed SPF, DKIM, and DMARC authentication because the attacker abused legitimate email infrastructure rather than spoofing the sender domain. The message relied on social engineering techniques to convince recipients to reset their Microsoft 365 password through an embedded phishing link.

No malicious attachments were present. The primary attack vector was a shortened URL that redirected users toward a Firebase-hosted phishing page.

Based on the collected evidence, the email was classified as a **High Risk Credential Phishing Attempt**.

---

# Case Information

| Field | Value |
|-------|-------|
| Case ID | CASE-01 |
| Case Name | Microsoft 365 Credential Phishing Investigation |
| Analyst | Abdull Ashthaf CK |
| Investigation Date | 2026-08-05 |
| Email Platform | Microsoft 365 |
| Status | Closed |

---

# Incident Classification

| Category | Value |
|----------|-------|
| Incident Type | Credential Phishing |
| Delivery Method | Email |
| Primary Attack Vector | Embedded URL |
| Attachments | None |
| Target | Microsoft 365 Credentials |
| Risk Rating | High |

---

# Investigation Summary

The investigation included:

- Initial triage
- Email header analysis
- Routing analysis
- Authentication verification (SPF, DKIM, DMARC)
- Sender verification
- Content analysis
- URL analysis
- Attachment verification
- IOC extraction
- Threat intelligence enrichment
- MITRE ATT&CK mapping
- Risk assessment

---

# Technical Findings

## Email Authentication

- SPF: Pass
- DKIM: Pass
- DMARC: Pass

The attacker leveraged trusted email infrastructure, allowing authentication checks to succeed.

---

## Sender Analysis

The sender appeared legitimate from an authentication perspective but attempted to impersonate Microsoft 365 through social engineering.

---

## Content Analysis

The email used:

- Password reset theme
- Urgency
- User action request
- Microsoft branding
- Credential harvesting lure

---

## URL Analysis

The investigation identified:

- URL shortening service (is.gd)
- Firebase-hosted destination
- Trusted cloud infrastructure abused for phishing

Threat intelligence indicated suspicious and phishing-related characteristics despite the use of legitimate hosting providers.

---

## Attachment Analysis

No attachments were present.

The phishing campaign relied entirely on embedded URLs rather than malware delivery.

---

# Indicators of Compromise (Summary)

| Type | Indicator |
|------|-----------|
| Email Address | Sender email identified during investigation |
| URL | Embedded phishing URL |
| Shortened URL | is.gd |
| Domain | lolalhopb.firebaseio.com |
| IP Address | Google infrastructure observed during delivery |

A complete IOC list is available in the **IOCs** directory.

---

# MITRE ATT&CK Mapping

| Technique | Description |
|-----------|-------------|
| T1566.002 | Spearphishing Link |
| T1583.006 | Acquire Infrastructure: Web Services |
| T1204.001 | User Execution: Malicious Link |

---

# Risk Assessment

Overall Risk: **High**

Reasoning:

- Credential theft objective
- Social engineering
- Trusted infrastructure
- Successful email authentication
- URL shortening used to obscure destination

---

# Recommended Actions

- Block the phishing URL.
- Block identified malicious domains.
- Notify affected users.
- Monitor authentication logs for suspicious sign-ins.
- Reset credentials if user interaction occurred.
- Improve phishing awareness training.
- Update email filtering rules.

---

# Conclusion

The investigation determined that the email was a credential phishing attempt targeting Microsoft 365 users.

Although the message successfully passed standard email authentication checks, the embedded phishing URL, impersonation techniques, and social engineering indicators confirmed malicious intent.

The incident demonstrates that successful SPF, DKIM, and DMARC validation alone should not be considered sufficient evidence of legitimacy. A complete investigation involving technical analysis, threat intelligence, and analyst judgment remains essential for accurately identifying phishing campaigns.
