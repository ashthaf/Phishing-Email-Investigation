# Investigation Screenshots

## Overview

This directory contains all screenshots collected during the investigation of **CASE-01 – Microsoft 365 Phishing Email**.

The screenshots document each stage of the investigation, from evidence preservation through header analysis, routing analysis, authentication verification, content analysis, URL investigation, threat intelligence enrichment, and MITRE ATT&CK mapping.

These images serve as supporting evidence for the findings documented throughout the case.

---

# Investigation Coverage

The screenshots in this directory include evidence for:

- Case preparation
- Evidence preservation
- Email extraction
- Header analysis
- Mail routing analysis
- Authentication analysis
- Sender verification
- Content analysis
- URL analysis
- Threat intelligence lookups
- MITRE ATT&CK mapping
- IOC validation

---

# Screenshot Inventory

| Screenshot | Description |
|------------|-------------|
| caseworkstation.png | Investigation workspace preparation |
| workingcopy.png | Working copy creation |
| md5.png | MD5 hash generation |
| md5verified.png | MD5 hash verification |
| sha256.png | SHA256 hash generation |
| sha256verified.png | SHA256 hash verification |
| chain1.png | Chain of custody documentation |
| chain2.png | Chain of custody verification |
| InitialTriage.png | Initial email triage |
| og mail.png | Original email evidence |
| ripmime.png | Email extraction using ripMIME |
| headerextraction.png | Header extraction process |
| subject.png | Subject header analysis |
| contenttype.png | MIME Content-Type analysis |
| bodyfiles.png | Extracted email body files |
| textfile1.png | Plain text email content |
| textfile2.png | HTML email content |
| hopanalysis.png | Mail hop analysis |
| hopscollected.png | Collected Received headers |
| Mailroutenumbered.png | Numbered mail route |
| routinganalysis.png | Mail routing analysis |
| host.png | Host information |
| hostanalysis.png | Host analysis |
| domain.png | Domain lookup |
| domainanalysis.png | Domain investigation |
| senderanalysis.png | Sender analysis |
| senderinformation.png | Sender information |
| authenticationanalysis.png | Authentication overview |
| spf.png *(if present)* | SPF verification |
| dkim.png | DKIM verification |
| dmarc.png | DMARC verification |
| arecord.png | DNS A record lookup |
| TXT.png | TXT record lookup |
| mx.png | MX record lookup |
| reversedns.png | Reverse DNS lookup |
| reversevirus.png | Reverse IP investigation |
| whois.png | WHOIS lookup |
| url.png | URL extraction |
| url1.png | URL analysis |
| url2.png | URL investigation |
| urllimit1.png | URL expansion |
| urllimit2.png | URL redirect analysis |
| virustotalurl.png | VirusTotal URL analysis |
| virusip.png | VirusTotal IP reputation |
| virusdomain.png | VirusTotal domain lookup |
| abuseip.png | AbuseIPDB lookup |
| talosdomain.png | Cisco Talos reputation lookup |
| emailrep.png | Email reputation lookup attempt |
| phishtank.png | PhishTank verification |
| m1.png | MITRE ATT&CK mapping – Spearphishing Link |
| m2.png | MITRE ATT&CK mapping – Acquire Infrastructure |
| m3.png | MITRE ATT&CK mapping – Masquerading |
| m4.png | MITRE ATT&CK mapping – User Execution |

---

# Notes

Some screenshots represent intermediate investigation steps and are included for documentation completeness.

Future investigations will also include:

- Thunderbird email rendering
- MXToolbox authentication verification
- Additional DNS analysis
- Email client visual inspection

These enhancements have been incorporated into the investigation methodology and will be used in future cases.

---

# Total Investigation Evidence

This folder contains visual documentation covering every major phase of the investigation and serves as supporting evidence for the final incident report.
