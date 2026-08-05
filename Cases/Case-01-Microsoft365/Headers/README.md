# Email Headers

## Overview

This directory contains the extracted email header information collected during the investigation of **CASE-01 – Microsoft 365 Phishing Email**.

Email headers provide the technical metadata required to reconstruct the delivery path, verify sender authentication, identify infrastructure, and detect spoofing attempts.

---

# Purpose

Header analysis helps analysts:

- Identify the true sending infrastructure
- Verify SPF, DKIM and DMARC authentication
- Reconstruct the email delivery path
- Examine Message-ID values
- Analyze routing information
- Detect spoofing attempts
- Support attribution and threat hunting

---

# Header Fields Examined

The investigation included analysis of the following fields:

- From
- To
- Subject
- Date
- Message-ID
- Return-Path
- Reply-To
- MIME-Version
- Content-Type
- Received headers
- Authentication-Results
- SPF
- DKIM
- DMARC

---

# Findings

The header analysis showed:

- The email originated through Google's mail infrastructure.
- SPF, DKIM, and DMARC authentication passed successfully.
- The sender leveraged legitimate cloud infrastructure rather than spoofing email authentication.
- The phishing campaign relied on trusted infrastructure and malicious embedded URLs instead of malicious attachments.

---

# Related Investigation Phases

The header information supported the following analyses:

- Routing Analysis
- Authentication Analysis
- Sender Analysis
- IOC Extraction
- Threat Intelligence
- MITRE ATT&CK Mapping

---

# Supporting Evidence

Relevant screenshots are available in:

- `../Screenshots/`

Detailed findings are documented in:

- `../Analysis/04-Header-Analysis.md`
- `../Analysis/05-Routing-Analysis.md`
- `../Analysis/06-Authentication-Analysis.md`
