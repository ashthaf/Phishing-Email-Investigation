# Email Attachments

## Overview

This directory is reserved for attachments extracted from the phishing email during the investigation.

Each attachment, if present, should be preserved in its original form and analyzed using safe forensic techniques before being opened or executed.

---

## Investigation Summary

During the analysis of **CASE-01 (Microsoft 365 Phishing Email)**, no email attachments were identified.

The phishing attempt relied on embedded links rather than malicious attachments.

---

## Standard Attachment Analysis Workflow

If attachments are present in future investigations, the following analysis should be performed:

1. Preserve the original attachment.
2. Calculate MD5 and SHA256 hashes.
3. Identify the file type and MIME type.
4. Perform static analysis.
5. Scan using VirusTotal or similar reputation services.
6. Analyze metadata.
7. Perform dynamic analysis in an isolated sandbox if required.
8. Document all findings.

---

## Current Status

| Item | Result |
|------|--------|
| Attachments Present | No |
| Static Analysis | Not Applicable |
| Dynamic Analysis | Not Applicable |
| Malware Scan | Not Applicable |

---

**Case:** CASE-01 – Microsoft 365 Phishing Email Investigation

**Project:** Phishing Email Investigation & Incident Response Lab

**Author:** Abdull Ashthaf CK
