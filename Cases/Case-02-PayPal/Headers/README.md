# 📧 Email Headers

![Category](https://img.shields.io/badge/Category-Email%20Headers-blue)
![Evidence](https://img.shields.io/badge/Evidence-Forensic-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

# 📖 Overview

This directory contains the email header artifacts extracted from the original phishing email during the forensic investigation.

Email headers provide valuable metadata regarding message origin, routing, authentication, and delivery. These artifacts formed the basis for the Header Analysis, Routing Analysis, Authentication Analysis, and Sender Analysis phases of the investigation.

---

# 📂 Contents

| File | Description |
|------|-------------|
| email-header.txt | Complete email header extracted from the original `.eml` file |
| received-header.txt | Extracted `Received` headers used for SMTP routing analysis |

---

# Investigation Usage

These artifacts were used to:

- Identify the visible sender.
- Analyze the Return-Path.
- Verify SPF, DKIM, and DMARC results.
- Reconstruct the SMTP delivery path.
- Identify the originating mail server.
- Document sender-related metadata.

---

# Related Analysis

- Phase 02 – Header Analysis
- Phase 03 – Routing Analysis
- Phase 04 – Authentication Analysis
- Phase 05 – Sender Analysis

---

# Notes

The header files were extracted directly from the original email sample and preserved without modification to maintain evidence integrity.

---

# Summary

These artifacts represent the primary source of metadata used throughout the technical investigation of the phishing email.
