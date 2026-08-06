# Evidence Summary

## CASE Information

| Field | Value |
|--------|-------|
| Case ID | CASE-02 |
| Case Name | PayPal Gift Card Phishing Investigation |
| Evidence ID | EVID-001 |
| Analyst | Abdull Ashthaf CK |
| Investigation Platform | Kali Linux |
| Status | Preserved |

---

# Evidence Overview

This document provides a summary of the primary evidence collected during **CASE-02**.

The evidence consists of the original phishing email preserved in its native `.eml` format and a password-protected archive created for safe storage and distribution.

The integrity of the evidence was verified using cryptographic hash functions prior to analysis.

---

# Primary Evidence

| Property | Value |
|----------|-------|
| Original File | sample-1407.eml |
| Investigation Copy | phishing-email.eml |
| Archive | phishing-email.zip |
| File Format | RFC 822 Email (.eml) |
| Archive Password | infected |

---

# Evidence Location

| Evidence | Location |
|----------|----------|
| Original Email | Evidence/Original-Email/phishing-email.eml |
| Password-Protected Archive | Evidence/Original-Email/phishing-email.zip |
| Chain of Custody | Evidence/chain-of-custody.md |
| Evidence Notes | Evidence/notes.md |

---

# Integrity Verification

Evidence integrity was verified before any forensic analysis.

| Algorithm | Status |
|-----------|--------|
| MD5 | ✅ Verified |
| SHA256 | ✅ Verified |

The generated hash values matched during verification, confirming that the evidence remained unchanged throughout the preservation process.

---

# Evidence Metadata

The following information was collected from the original email before analysis:

- File type
- File size
- File permissions
- File ownership
- File timestamps
- MD5 hash
- SHA256 hash

Metadata collection was performed using standard Linux forensic utilities.

---

# Preservation Activities

The following actions were completed during the evidence preservation phase:

- Original phishing email preserved.
- Working copy created.
- MD5 hash generated.
- SHA256 hash generated.
- Hash values verified.
- Password-protected archive created.
- Chain of custody documented.
- Evidence metadata collected.

---

# Initial Assessment

The email appears to impersonate the **PayPal** brand using a promotional gift card theme.

At the time of preservation, no modifications were made to the original evidence.

Technical analysis of the email content, sender infrastructure, authentication mechanisms, URLs, and Indicators of Compromise (IOCs) will be performed during subsequent investigation phases.

---

# Related Documentation

- chain-of-custody.md
- notes.md
- Original-Email/
- Headers/
- Artifacts/
- IOCs/
- Analysis/

---

# Evidence Status

| Item | Status |
|------|--------|
| Original Email Preserved | ✅ |
| Working Copy Created | ✅ |
| MD5 Generated | ✅ |
| SHA256 Generated | ✅ |
| Hashes Verified | ✅ |
| Archive Protected | ✅ |
| Metadata Collected | ✅ |
| Ready for Technical Analysis | ✅ |

---

**Prepared By:** Abdull Ashthaf CK

**Project:** Phishing Email Investigation & Incident Response Lab

**Case:** CASE-02 – PayPal Gift Card Phishing Investigation
