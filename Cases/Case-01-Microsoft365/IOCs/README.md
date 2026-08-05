# Indicators of Compromise (IOCs)

## Overview

This directory contains all Indicators of Compromise (IOCs) extracted during the investigation of **CASE-01 – Microsoft 365 Phishing Email**.

The collected indicators are provided in multiple formats to support threat hunting, incident response, SIEM ingestion, and future investigations.

---

# Purpose

The purpose of this directory is to:

- Preserve all identified indicators
- Support IOC sharing between analysts
- Enable threat hunting
- Assist detection engineering
- Facilitate SIEM and EDR enrichment
- Improve future investigations

---

# Contents

| File | Description |
|------|-------------|
| IOC-Report.md | Human-readable IOC summary |
| iocs.csv | IOC list in CSV format |
| iocs.json | IOC list in JSON format |

---

# IOC Categories

The following indicator types were collected during this investigation:

- URLs
- Domains
- IP Addresses
- Email Addresses
- Message IDs

No malicious attachments or file hashes were identified because the phishing email did not contain attachments.

---

# Case Summary

During CASE-01, the phishing email primarily relied on:

- Social engineering
- URL-based credential harvesting
- Legitimate Google infrastructure
- URL shortening services

No malware payloads or malicious attachments were present.

---

# Usage

These indicators can be used for:

- SIEM searches
- Threat hunting
- Firewall blocking
- DNS filtering
- Email security rules
- IOC sharing
- Detection engineering

---

# Notes

Some infrastructure observed during the investigation belongs to legitimate cloud providers (e.g., Google and Cloudflare).

Although these IP addresses and domains appeared in the investigation, they should be treated as contextual infrastructure rather than automatically blocked without additional verification.

---

# Related Artifacts

Additional IOC-related artifacts are available in:

- `Artifacts/domains.txt`
- `Artifacts/urls.txt`
- `Artifacts/ips.txt`
- `Artifacts/email-addresses.txt`
- `Artifacts/message-ids.txt`

These files contain the raw indicators extracted during the investigation.
