# 📝 Investigation Notes

![Category](https://img.shields.io/badge/Category-Investigation%20Notes-blue)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

# Purpose

This document contains investigation notes recorded throughout the analysis of the PayPal phishing email.

These notes summarize significant observations made during each phase of the investigation.

---

# Investigation Timeline

## Initial Triage

- Opened the phishing email in an isolated Kali Linux virtual machine.
- Thunderbird blocked remote content automatically.
- No attachments were observed.
- Email impersonated the PayPal brand.

---

## Header Analysis

- Successfully extracted the complete email header.
- Multiple Received headers identified.
- Return-Path differed from the visible sender.
- Authentication headers were present.

---

## Routing Analysis

- Reconstructed the SMTP delivery path.
- Email originated from messaggerocappuccino.it.
- Message passed through Microsoft Exchange Online infrastructure.
- No suspicious relay servers observed after Microsoft accepted the message.

---

## Authentication Analysis

- SPF passed.
- DKIM signature not present.
- DMARC passed.
- MX records verified.
- WHOIS information collected.

---

## Sender Analysis

- Visible sender differed from Return-Path.
- Reply-To header not present.
- Sender infrastructure investigated.

---

## Content Analysis

- HTML phishing email.
- German-language content.
- Fake PayPal promotion.
- Multiple embedded hyperlinks.
- External images loaded from easilett.com.
- Fake unsubscribe mechanism identified.

---

## URL Analysis

- Extracted embedded URLs.
- Investigated easilett.com.
- DNS and WHOIS completed.
- Threat Intelligence collected.

---

## Attachment Analysis

- No attachments identified.
- Email consisted only of HTML content.

---

## IOC Extraction

Primary Indicators of Compromise:

- service@stayfriends.de
- return@messaggerocappuccino.it
- easilett.com
- 77.91.100.118

---

## Threat Intelligence

Platforms consulted:

- VirusTotal
- URLScan.io
- Cisco Talos
- AbuseIPDB
- MXToolbox
- WHOIS

---

## MITRE ATT&CK Mapping

Observed techniques included:

- T1566 – Phishing
- T1566.002 – Spearphishing Link
- T1036 – Masquerading
- T1204.001 – User Execution: Malicious Link
- T1583.001 – Acquire Infrastructure: Domains
- T1585.001 – Establish Accounts

---

## Final Assessment

The investigation confirmed that the email was a **credential harvesting phishing campaign** targeting users through PayPal brand impersonation and malicious hyperlinks.

No malware or malicious attachments were identified.

---

# Conclusion

These notes document the major observations recorded throughout the investigation and provide a concise summary of the analytical process followed during the incident response workflow.
