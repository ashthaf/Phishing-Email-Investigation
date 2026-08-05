# Phase 14 – Incident Report

# Incident Summary

| Field | Value |
|--------|-------|
| Case ID | Case-01-Microsoft365 |
| Incident Type | Credential Phishing |
| Investigation Status | Completed |
| Severity | High |
| Overall Risk | High |
| Analyst | Abdull Ashthaf CK |
| Investigation Date | August 2026 |

---

# Executive Summary

A phishing email impersonating a Microsoft 365 password reset notification was investigated to determine its legitimacy and potential impact.

The investigation confirmed that the email was a credential phishing attempt designed to redirect victims to a password reset page hosted on Google Firebase infrastructure.

Although the email successfully passed SPF, DKIM, and DMARC authentication checks, the embedded shortened URL and phishing content demonstrated malicious intent.

No malicious attachments were identified, and no evidence indicated that credentials had been successfully compromised during this investigation.

---

# Investigation Scope

The investigation included:

- Initial Email Triage
- Header Analysis
- Routing Analysis
- Authentication Analysis
- Sender Analysis
- Content Analysis
- URL Analysis
- Attachment Analysis
- IOC Extraction
- Threat Intelligence
- MITRE ATT&CK Mapping
- Risk Assessment

---

# Key Findings

## Email Authentication

The email successfully passed:

- SPF
- DKIM
- DMARC

This confirms that the email originated from authorized infrastructure but does **not** confirm that the email is legitimate.

---

## Sender Infrastructure

The investigation identified that the sender leveraged trusted Google infrastructure.

Observed infrastructure included:

- Google Mail Servers
- Google Firebase Hosting
- URL shortening service (is.gd)

These services were abused to increase the credibility of the phishing campaign.

---

## Email Content

The phishing email impersonated a Microsoft 365 password reset notification.

Observed social engineering techniques included:

- Password reset lure
- Sense of urgency
- Credential harvesting
- Microsoft branding
- URL shortening

---

## URL Analysis

One shortened URL was identified.

```
https://is.gd/...
```

The shortened URL redirected toward a Firebase-hosted password reset workflow.

Threat intelligence platforms identified the URL as suspicious, with phishing detections reported by multiple security vendors.

---

## Attachment Analysis

No attachments were identified.

The phishing campaign relied entirely on social engineering rather than malware delivery.

---

# Threat Intelligence Summary

External intelligence sources used during the investigation included:

- VirusTotal
- Cisco Talos
- AbuseIPDB
- URLScan.io
- PhishTank
- EmailRep

Key findings:

- Firebase infrastructure owned by Google
- Google SMTP infrastructure
- URL detected as phishing by multiple vendors
- Sending IP had no malicious reputation
- Infrastructure itself was legitimate but abused

---

# MITRE ATT&CK Mapping

| Technique ID | Technique |
|--------------|-----------|
| T1566.002 | Spearphishing Link |
| T1583.006 | Acquire Infrastructure: Web Services |
| T1204.001 | User Execution: Malicious Link |
| T1036 | Masquerading |

---

# Indicators of Compromise

## Malicious Indicators

- Phishing URL
- is.gd shortened URL
- Credential harvesting page

## Legitimate Infrastructure Abused

- Google Mail
- Google Firebase Hosting
- Google SMTP Server
- Google Cloud Infrastructure

---

# Risk Assessment

| Category | Rating |
|----------|---------|
| Threat Type | Credential Phishing |
| Likelihood | High |
| Potential Impact | High |
| Severity | High |
| Overall Risk | High |

---

# Containment Recommendations

Recommended actions:

- Block phishing URLs
- Remove email from all mailboxes
- Block sender where appropriate
- Monitor Microsoft 365 sign-in activity
- Enable Multi-Factor Authentication
- Update email filtering policies
- Conduct user awareness training

---

# Final Verdict

The investigation concludes that the email is a **credential phishing campaign** targeting Microsoft 365 users.

Rather than relying on malware or malicious attachments, the attacker abused trusted cloud infrastructure—including Google Firebase Hosting and Google Mail—to increase credibility and evade traditional reputation-based detection.

The phishing campaign relied on user interaction through a shortened URL that redirected victims to a credential harvesting page.

No evidence of successful credential compromise was identified during this investigation.

---

# Lessons for Security Teams

This investigation demonstrates that:

- Passing SPF, DKIM, and DMARC does not guarantee an email is safe.
- Trusted cloud infrastructure can be abused to host phishing content.
- URL shortening services can conceal malicious destinations.
- Effective phishing detection requires analyzing the complete email, including headers, content, URLs, and external threat intelligence.
- User awareness and layered security controls remain essential defenses against credential phishing attacks.

---

# Incident Status

**Status:** Closed

**Reason for Closure:**

The phishing email was fully investigated, all available evidence was analyzed, indicators of compromise were documented, and appropriate containment recommendations were identified. No evidence of successful account compromise or malware execution was observed during the investigation.

---

**End of Report**
