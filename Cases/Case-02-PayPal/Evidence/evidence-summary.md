# 📑 Evidence Summary

![Evidence](https://img.shields.io/badge/Evidence-Summary-blue)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

# 📖 Overview

This document summarizes the primary evidence collected during the investigation of the PayPal phishing email.

The collected evidence formed the basis for all subsequent analysis phases, including header analysis, routing analysis, authentication verification, content analysis, URL investigation, IOC extraction, Threat Intelligence validation, and incident reporting.

---

# Primary Evidence

| Evidence | Description |
|----------|-------------|
| sample-1407.eml | Original phishing email sample |

---

# Extracted Evidence

## Email Headers

- email-header.txt
- Received-header.txt

Purpose:

- Sender analysis
- Routing analysis
- Authentication verification

---

## Email Content

- phishing-email.html

Purpose:

- HTML analysis
- Hyperlink extraction
- Content analysis

---

## URL Investigation

- extracted_urls.txt
- domains.txt
- dig.txt
- whois.txt

Purpose:

- URL analysis
- Domain investigation
- DNS validation
- WHOIS verification

---

## Threat Intelligence

The extracted indicators were validated using:

- VirusTotal
- URLScan.io
- Cisco Talos
- AbuseIPDB
- MXToolbox
- WHOIS

---

# Key Indicators of Compromise

| Type | Value |
|------|-------|
| Sender | service@stayfriends.de |
| Return-Path | return@messaggerocappuccino.it |
| Source IP | 77.91.100.118 |
| Suspicious Domain | easilett.com |
| Legitimate Domain | fonts.googleapis.com |

---

# Investigation Outcome

The investigation determined that:

- The email impersonated PayPal.
- The campaign relied on social engineering.
- Embedded hyperlinks redirected victims to attacker-controlled infrastructure.
- No malware attachments were identified.
- The campaign was classified as a credential harvesting phishing attack.

---

# Conclusion

The collected evidence provided sufficient technical information to reconstruct the phishing campaign, identify the supporting infrastructure, extract actionable Indicators of Compromise (IOCs), and complete the incident investigation.
