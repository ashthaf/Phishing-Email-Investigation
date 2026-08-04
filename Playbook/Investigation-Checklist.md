# Phishing Email Investigation Checklist

> **Playbook Version:** 1.0
>
> **Case ID:** ______________________
>
> **Analyst:** ______________________
>
> **Investigation Date:** ______________________
>
> **Status Legend**
>
> - [ ] Not Started
> - [x] Completed
> - [-] Not Applicable

---

# Phase 1 – Case Intake

## Objective

Establish the investigation scope and create the case.

### Checklist

- [ ] Assign Case ID
- [ ] Create Case Folder
- [ ] Record Investigation Date
- [ ] Record Analyst Name
- [ ] Acquire Original Email (.eml)
- [ ] Record Email Source
- [ ] Record Reporter (if applicable)

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 2 – Evidence Preservation

## Objective

Preserve evidence integrity before analysis.

### Checklist

- [ ] Preserve Original Email
- [ ] Generate MD5 Hash
- [ ] Generate SHA256 Hash
- [ ] Record Hash Values
- [ ] Verify Evidence Integrity
- [ ] Create Evidence Log
- [ ] Create Chain of Custody

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 3 – Initial Triage

## Objective

Perform a high-level assessment.

### Checklist

- [ ] Review Subject
- [ ] Review Sender
- [ ] Review Recipient
- [ ] Identify Email Theme
- [ ] Identify Suspected Attack Type
- [ ] Assign Initial Classification

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 4 – Header Analysis

## Objective

Extract all relevant email headers.

### Checklist

- [ ] Subject
- [ ] From
- [ ] To
- [ ] Date
- [ ] Return-Path
- [ ] Reply-To
- [ ] Message-ID
- [ ] MIME-Version
- [ ] Content-Type
- [ ] Content-Transfer-Encoding
- [ ] X-Mailer
- [ ] User-Agent
- [ ] Custom X-Headers

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 5 – Routing Analysis

## Objective

Reconstruct the email delivery path.

### Checklist

- [ ] Extract Received Headers
- [ ] Count Mail Hops
- [ ] Number Received Headers
- [ ] Extract Public IP Addresses
- [ ] Identify Internal IP Addresses
- [ ] Identify Originating IP
- [ ] Identify Relay Servers
- [ ] Verify TLS Usage
- [ ] Build Mail Flow Diagram
- [ ] Verify Delivery Timeline

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 6 – Authentication Analysis

## Objective

Verify sender authentication.

### Checklist

- [ ] SPF Checked
- [ ] DKIM Checked
- [ ] DMARC Checked
- [ ] Authentication Alignment Reviewed
- [ ] Authentication Findings Documented

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 7 – Sender Analysis

## Objective

Assess sender legitimacy.

### Checklist

- [ ] Verify Sender Address
- [ ] Verify Display Name
- [ ] Verify Reply-To
- [ ] Verify Return-Path
- [ ] Compare Sender Domains
- [ ] Domain Reputation Checked
- [ ] Domain Age Reviewed

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 8 – Content Analysis

## Objective

Analyze email content.

### Checklist

- [ ] Plain Text Reviewed
- [ ] HTML Reviewed
- [ ] Branding Abuse Identified
- [ ] Urgency Language Identified
- [ ] Credential Harvesting Indicators
- [ ] Social Engineering Indicators
- [ ] Grammar and Spelling Reviewed

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 9 – URL Analysis

## Objective

Investigate embedded links.

### Checklist

- [ ] URLs Extracted
- [ ] Domains Identified
- [ ] Redirects Identified
- [ ] HTTPS Verified
- [ ] WHOIS Performed
- [ ] DNS Lookup Performed
- [ ] URL Reputation Checked
- [ ] URLScan Checked
- [ ] VirusTotal Checked

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 10 – Attachment Analysis

## Objective

Investigate attachments.

### Checklist

- [ ] Attachment Identified
- [ ] File Name Recorded
- [ ] File Type Verified
- [ ] MIME Type Verified
- [ ] MD5 Generated
- [ ] SHA256 Generated
- [ ] Static Analysis Performed
- [ ] Malware Scan Completed

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 11 – IOC Extraction

## Objective

Collect Indicators of Compromise.

### Checklist

- [ ] Email Addresses
- [ ] Domains
- [ ] URLs
- [ ] IP Addresses
- [ ] File Hashes
- [ ] Attachment Names
- [ ] Usernames
- [ ] Hostnames

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 12 – Threat Intelligence

## Objective

Validate collected indicators.

### Checklist

- [ ] VirusTotal
- [ ] AbuseIPDB
- [ ] Cisco Talos
- [ ] AlienVault OTX
- [ ] URLhaus
- [ ] URLScan
- [ ] Google Safe Browsing

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 13 – MITRE ATT&CK Mapping

## Objective

Map attacker behavior.

### Checklist

- [ ] Initial Access
- [ ] Execution
- [ ] Credential Access
- [ ] Collection
- [ ] Exfiltration
- [ ] ATT&CK Techniques Documented

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 14 – Risk Assessment

## Objective

Determine investigation severity.

### Checklist

- [ ] Impact Assessed
- [ ] Likelihood Assessed
- [ ] Risk Level Assigned
- [ ] Business Impact Recorded

### Risk Level

- [ ] Informational
- [ ] Low
- [ ] Medium
- [ ] High
- [ ] Critical

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 15 – Containment Recommendations

## Checklist

- [ ] Block Sender
- [ ] Block Domain
- [ ] Block IP
- [ ] Remove Email
- [ ] Reset Password
- [ ] Notify Users
- [ ] Update Detection Rules

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 16 – Final Report

### Checklist

- [ ] Executive Summary
- [ ] Technical Findings
- [ ] IOC Summary
- [ ] Timeline
- [ ] MITRE Mapping
- [ ] Recommendations
- [ ] Final Review Completed

### Evidence

_____________________________________________________

### Analyst Notes

_____________________________________________________

---

# Phase 17 – Lessons Learned

### Checklist

- [ ] Investigation Reviewed
- [ ] Detection Improvements Identified
- [ ] Playbook Improvements Identified
- [ ] Documentation Updated

### Lessons Learned

_____________________________________________________

_____________________________________________________

_____________________________________________________

---

# Investigation Completion

| Item | Status |
|------|--------|
| Evidence Preserved | ☐ |
| Technical Analysis Completed | ☐ |
| IOC Extraction Completed | ☐ |
| Threat Intelligence Completed | ☐ |
| MITRE Mapping Completed | ☐ |
| Risk Assessment Completed | ☐ |
| Final Report Completed | ☐ |
| Investigation Closed | ☐ |

---

## Final Verdict

**Classification**

- [ ] Legitimate
- [ ] Spam
- [ ] Phishing
- [ ] Malware
- [ ] Business Email Compromise
- [ ] Credential Harvesting
- [ ] Other

---

**Overall Summary**

_____________________________________________________

_____________________________________________________

_____________________________________________________

---

**Analyst Signature**

_________________________

**Date**

_________________________
