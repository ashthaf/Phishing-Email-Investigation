# Investigation Timeline

## Case Information

| Field | Value |
|-------|-------|
| Case ID | CASE-01 |
| Case Name | Microsoft 365 Credential Phishing Investigation |
| Investigation Date | 2026-08-05 |
| Analyst | Abdull Ashthaf CK |

---

## Timeline

| Time | Activity | Result |
|------|----------|--------|
| T+00 | Received phishing email (.eml) | Evidence preserved |
| T+05 | Generated evidence hashes | Integrity verified |
| T+10 | Extracted email headers | Header analysis initiated |
| T+20 | Analyzed routing path | Email originated from Google mail infrastructure |
| T+30 | Verified SPF, DKIM, and DMARC | All authentication checks passed |
| T+40 | Investigated sender identity | Display name impersonation identified |
| T+50 | Reviewed email content | Password reset lure identified |
| T+60 | Extracted embedded URLs | URL shortener redirected to Firebase-hosted page |
| T+70 | Performed URL reputation analysis | Mixed reputation; phishing characteristics observed |
| T+80 | Checked for attachments | No attachments present |
| T+90 | Extracted Indicators of Compromise (IOCs) | URLs, domains, IPs, email addresses documented |
| T+100 | Performed Threat Intelligence enrichment | VirusTotal, Talos, AbuseIPDB, URLScan, PhishTank consulted |
| T+110 | Mapped attacker behavior to MITRE ATT&CK | Relevant techniques identified |
| T+120 | Assessed overall risk | High |
| T+130 | Documented containment recommendations | Investigation completed |
| T+140 | Final incident report prepared | Case closed |

---

## Investigation Outcome

The investigation confirmed that the email was a credential phishing attempt leveraging trusted cloud infrastructure, URL shortening services, and social engineering techniques to impersonate Microsoft 365 password reset notifications.

No malicious attachment was present. The primary attack vector was an embedded phishing URL.
