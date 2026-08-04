# Master Phishing Email Investigation Playbook

> Version: 1.0
>
> Project: Phishing Email Investigation & Incident Response Lab
>
> Author: Abdull Ashthaf CK
>
> Status: Active

---

# Purpose

This playbook defines a standardized methodology for investigating phishing emails in a controlled laboratory environment.

The objective is to ensure that every phishing investigation follows a repeatable process for evidence preservation, technical analysis, threat intelligence enrichment, documentation, and reporting.

This playbook is intentionally vendor-neutral and can be applied to Microsoft 365, Gmail, Exchange, Google Workspace, and other email platforms.

---

# Methodology

This playbook is inspired by publicly available industry guidance and best practices, including:

- NIST SP 800-61 Revision 2 – Computer Security Incident Handling Guide
- SANS DFIR Investigation Methodology
- CISA Phishing Guidance
- Microsoft Defender for Office 365 Documentation
- MITRE ATT&CK Framework

This document is an educational investigation framework and is not an official publication from any organization listed above.

---

# Investigation Lifecycle

Every phishing investigation must follow the phases below in order.

```
Case Intake
        ↓
Evidence Preservation
        ↓
Initial Triage
        ↓
Header Analysis
        ↓
Routing Analysis
        ↓
Authentication Analysis
        ↓
Sender Analysis
        ↓
Content Analysis
        ↓
URL Analysis
        ↓
Attachment Analysis
        ↓
IOC Extraction
        ↓
Threat Intelligence
        ↓
MITRE ATT&CK Mapping
        ↓
Risk Assessment
        ↓
Containment Recommendations
        ↓
Incident Report
        ↓
Lessons Learned
```

---

# Phase 1 – Case Intake

## Objective

Initiate the investigation and establish the case scope.

## Analyst Questions

- What was reported?
- Who reported it?
- What evidence is available?
- What is the suspected attack type?

## Evidence Required

- Original email (.eml)
- Reporter information (if available)
- Case ID

## Completion Criteria

A unique case folder has been created and evidence has been received.

---

# Phase 2 – Evidence Preservation

## Objective

Preserve evidence without modification.

## Evidence Required

- Original .eml
- MD5 hash
- SHA256 hash
- Chain of Custody

## Completion Criteria

Evidence integrity has been verified and documented.

---

# Phase 3 – Initial Triage

## Objective

Determine whether the email appears suspicious before deep analysis.

## Analyst Questions

- What is the subject?
- Who sent it?
- Who received it?
- Does the email claim urgency?
- What is the suspected lure?

## Expected Output

Initial assessment of the email.

---

# Phase 4 – Header Analysis

## Objective

Extract and examine all email headers.

## Required Analysis

- Subject
- From
- To
- Return-Path
- Reply-To
- Message-ID
- Date
- MIME Version
- Content-Type

## Completion Criteria

Header fields have been documented.

---

# Phase 5 – Routing Analysis

## Objective

Reconstruct the email delivery path.

## Required Analysis

- Received headers
- Mail hops
- Sender IP
- Relay servers
- TLS information
- Delivery timeline

## Completion Criteria

The email route has been reconstructed.

---

# Phase 6 – Authentication Analysis

## Objective

Determine whether sender authentication succeeded.

## Required Analysis

- SPF
- DKIM
- DMARC
- Alignment

## Completion Criteria

Authentication results have been documented.

---

# Phase 7 – Sender Analysis

## Objective

Verify sender identity.

## Required Analysis

- Sender domain
- Reply-To domain
- Return-Path
- Display Name
- Domain reputation

## Completion Criteria

Sender legitimacy has been assessed.

---

# Phase 8 – Content Analysis

## Objective

Analyze the message body.

## Required Analysis

- Plain text
- HTML
- Social engineering indicators
- Credential harvesting
- Urgency language
- Branding abuse

## Completion Criteria

Message content has been documented.

---

# Phase 9 – URL Analysis

## Objective

Identify and analyze embedded links.

## Required Analysis

- URLs
- Domains
- Redirects
- HTTPS
- WHOIS
- URL reputation

## Completion Criteria

All URLs have been investigated.

---

# Phase 10 – Attachment Analysis

## Objective

Analyze attachments for malicious behavior.

## Required Analysis

- File names
- File types
- MIME
- Hashes
- Static analysis
- Malware scanning

## Completion Criteria

Every attachment has been assessed.

---

# Phase 11 – IOC Extraction

## Objective

Collect Indicators of Compromise.

## IOC Categories

- Domains
- URLs
- IP addresses
- Email addresses
- File hashes
- Attachments

## Completion Criteria

All IOCs have been documented.

---

# Phase 12 – Threat Intelligence

## Objective

Validate collected IOCs using threat intelligence.

## Sources

- VirusTotal
- AbuseIPDB
- Cisco Talos
- AlienVault OTX
- URLhaus
- URLScan

## Completion Criteria

IOC reputation has been verified.

---

# Phase 13 – MITRE ATT&CK Mapping

## Objective

Map attacker behavior to MITRE ATT&CK.

## Example Techniques

- T1566 – Phishing
- T1566.001 – Spearphishing Attachment
- T1566.002 – Spearphishing Link
- T1078 – Valid Accounts
- T1204 – User Execution

## Completion Criteria

Relevant ATT&CK techniques have been identified.

---

# Phase 14 – Risk Assessment

## Objective

Determine the business impact.

## Risk Levels

- Informational
- Low
- Medium
- High
- Critical

## Completion Criteria

Overall severity has been assigned.

---

# Phase 15 – Containment Recommendations

## Examples

- Block sender
- Block domain
- Block IP
- Remove email from mailboxes
- Reset compromised credentials
- Block URLs
- Notify affected users

---

# Phase 16 – Final Incident Report

The final report must include:

- Executive Summary
- Technical Findings
- Timeline
- IOC Summary
- MITRE Mapping
- Risk Rating
- Recommendations

---

# Phase 17 – Lessons Learned

After every investigation document:

- What worked well?
- What indicators were most valuable?
- Could detection rules be improved?
- Should the playbook be updated?

Continuous improvement is part of the investigation process.

---

# Playbook Completion Criteria

An investigation is considered complete only when:

- Evidence has been preserved.
- All playbook phases have been completed or marked as not applicable.
- Findings have been documented.
- Indicators of Compromise have been recorded.
- MITRE ATT&CK mapping has been completed.
- Risk has been assessed.
- Final incident report has been written.
- Lessons learned have been documented.
