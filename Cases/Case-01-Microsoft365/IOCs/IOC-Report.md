# IOC Report

**Case ID:** CASE-01 – Microsoft 365 Phishing Email

**Analysis Date:** August 2026

**Analyst:** Abdull Ashthaf CK

---

# Overview

This report summarizes the Indicators of Compromise (IOCs) identified during the investigation of a phishing email targeting Microsoft 365 users.

The phishing campaign relied on social engineering and credential harvesting through embedded URLs. No malicious attachments or executable payloads were identified.

---

# IOC Summary

| IOC Type | Count |
|----------|------:|
| URLs | 2 |
| Domains | 4 |
| IP Addresses | 2 |
| Email Addresses | 2 |
| Message IDs | 1 |
| Attachments | 0 |

---

# URLs

| Indicator | Description |
|-----------|-------------|
| `https://is.gd/...` | URL shortening service used to conceal the destination |
| `https://lolalhopb.firebaseio.com/...` | Firebase-hosted credential harvesting page |

---

# Domains

| Domain | Notes |
|--------|-------|
| `is.gd` | URL shortening service |
| `lolalhopb.firebaseio.com` | Phishing landing page hosted on Firebase |
| `firebaseio.com` | Legitimate Google-owned hosting platform abused by the attacker |
| `googleusercontent.com` | Legitimate cloud infrastructure observed during analysis |

---

# IP Addresses

| IP Address | Notes |
|-----------|-------|
| `104.25.233.53` | Cloudflare infrastructure serving the shortened URL |
| `209.85.210.72` | Google mail infrastructure observed in email routing |

> **Note:** The IP addresses belong to legitimate service providers (Cloudflare and Google). They are included as contextual indicators and should **not** be considered malicious on their own.

---

# Email Addresses

| Email Address | Purpose |
|--------------|---------|
| Sender address | Phishing sender observed in the email |
| Recipient address | Target mailbox used during the investigation |

---

# Message ID

| Indicator |
|-----------|
| Message-ID extracted from the original email header |

---

# Attachments

No attachments were present in the email.

No file hashes or malware artifacts were generated.

---

# Threat Intelligence Summary

The extracted indicators were verified using multiple OSINT platforms:

- VirusTotal
- URLScan.io
- Cisco Talos Intelligence
- AbuseIPDB
- PhishTank

The shortened URL and Firebase-hosted page exhibited characteristics consistent with phishing infrastructure, while the supporting IP addresses belonged to legitimate cloud providers.

---

# Analyst Assessment

The phishing email employed a common credential harvesting technique by combining:

- URL shortening
- Trusted cloud infrastructure
- Social engineering

No malware delivery or attachment-based execution was observed.

---

# Related Files

Machine-readable IOC formats are available in:

- `iocs.csv`
- `iocs.json`

Additional raw artifacts are stored in the `Artifacts/` directory.
