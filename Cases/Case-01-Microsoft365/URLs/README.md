# URLs

## Overview

This directory contains all URL-related artifacts collected during the investigation of CASE-01.

The URLs extracted from the phishing email were analyzed to determine their purpose, reputation, redirect behavior, and potential malicious intent.

Detailed technical findings are documented in:

> Analysis/07-URL-Analysis.md

---

## Contents

| File | Description |
|------|-------------|
| extracted-urls.txt | URLs extracted directly from the email |
| expanded-urls.txt | Expanded URLs after resolving shortened links |
| url-reputation.md | Threat intelligence and reputation lookup results |

---

## Summary

The investigation identified the use of:

- URL shortening service (is.gd)
- Firebase-hosted phishing infrastructure
- Trusted cloud services abused for credential phishing

Although legitimate infrastructure was used, the URLs exhibited phishing characteristics and were classified as malicious based on the overall investigation.
