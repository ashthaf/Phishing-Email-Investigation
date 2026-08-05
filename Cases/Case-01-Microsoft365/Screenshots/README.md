# Investigation Screenshots

## Overview

This directory contains all screenshots collected during the investigation of **CASE-01 – Microsoft 365 Phishing Email**.

The screenshots document every stage of the investigation and provide visual evidence supporting the findings documented throughout the case.

---

# Purpose

These screenshots serve as supporting evidence for:

- Evidence preservation
- Email extraction
- Header analysis
- Routing analysis
- Sender verification
- Authentication verification
- Content analysis
- URL investigation
- Threat intelligence enrichment
- MITRE ATT&CK mapping
- Final incident documentation

---

# Screenshot Inventory

## Evidence Preservation

| Screenshot | Description |
|------------|-------------|
| case-workstation.png | Investigation workspace preparation |
| working-copy.png | Working copy creation |
| md5.png | MD5 hash generation |
| md5-verified.png | MD5 hash verification |
| sha256.png | SHA256 hash generation |
| sha256-verified.png | SHA256 hash verification |
| chain-of-custody-1.png | Chain of custody documentation |
| chain-of-custody-2.png | Chain of custody verification |

---

## Initial Analysis

| Screenshot | Description |
|------------|-------------|
| initial-triage.png | Initial phishing email assessment |
| original-email.png | Original email evidence |
| ripmime-extraction.png | Email extraction using ripMIME |

---

## Header Analysis

| Screenshot | Description |
|------------|-------------|
| header-extraction.png | Header extraction process |
| subject-analysis.png | Subject field analysis |
| content-type.png | MIME Content-Type analysis |
| body-files.png | Extracted email body files |
| email-text-1.png | Plain text email content |
| email-text-2.png | HTML email content |

---

## Routing Analysis

| Screenshot | Description |
|------------|-------------|
| mail-route-numbered.png | Numbered mail route |
| hop-analysis.png | Mail hop analysis |
| received-hops.png | Received header collection |
| routing-analysis.png | Email routing reconstruction |
| host-analysis.png | Host analysis |
| host-information.png | Host information |

---

## Sender & Authentication

| Screenshot | Description |
|------------|-------------|
| sender-analysis.png | Sender analysis |
| sender-information.png | Sender details |
| authentication-analysis.png | Authentication overview |
| spf.png | SPF verification |
| dkim.png | DKIM verification |
| dmarc.png | DMARC verification |
| dns-a-record.png | DNS A record lookup |
| dns-txt-record.png | TXT record lookup |
| dns-mx-record.png | MX record lookup |
| reverse-dns.png | Reverse DNS lookup |
| reverse-ip-analysis.png | Reverse IP investigation |
| whois.png | WHOIS lookup |
| domain-analysis.png | Domain investigation |
| domain-information.png | Domain information |

---

## URL Analysis

| Screenshot | Description |
|------------|-------------|
| extracted-urls.png | Extracted URLs |
| url-analysis.png | URL investigation |
| urlscan-summary.png | URLScan summary |
| urlscan-transactions.png | URLScan HTTP transactions |

---

## Threat Intelligence

| Screenshot | Description |
|------------|-------------|
| virustotal-url.png | VirusTotal URL analysis |
| virustotal-domain.png | VirusTotal domain reputation |
| virustotal-ip.png | VirusTotal IP reputation |
| abuseipdb.png | AbuseIPDB lookup |
| cisco-talos.png | Cisco Talos reputation |
| phishtank.png | PhishTank verification |
| emailrep.png | Email reputation lookup attempt |

---

## MITRE ATT&CK Mapping

| Screenshot | Description |
|------------|-------------|
| mitre-spearphishing-link.png | T1566.002 – Spearphishing Link |
| mitre-acquire-infrastructure.png | T1583.006 – Acquire Infrastructure: Web Services |
| mitre-masquerading.png | T1036 – Masquerading |
| mitre-user-execution.png | T1204 – User Execution |

---

# Notes

This investigation primarily relied on command-line forensic tools and OSINT platforms to preserve evidence and perform technical analysis.

Future investigations will additionally include:

- Thunderbird visual email rendering
- MXToolbox authentication validation
- Email client visual inspection
- Additional DNS verification

These improvements have been incorporated into the investigation workflow for subsequent cases.

---

# Summary

This directory contains the complete visual evidence collected during the investigation of **CASE-01** and supports every major phase of the phishing email investigation lifecycle.
