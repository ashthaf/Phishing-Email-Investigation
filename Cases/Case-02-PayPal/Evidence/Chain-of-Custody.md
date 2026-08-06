# Chain of Custody

## Case Information

| Field | Value |
|--------|-------|
| Case ID | CASE-02 |
| Case Name | PayPal Gift Card Phishing Investigation |
| Evidence ID | EVID-001 |
| Evidence Type | Original Phishing Email (.eml) |
| Original File | sample-1407.eml |
| Stored As | phishing-email.eml |
| Analyst | Abdull Ashthaf CK |
| Investigation Platform | Kali Linux |
| Status | Preserved |

---

# Purpose

This document records the handling, preservation, and integrity verification of the original phishing email throughout the investigation.

Maintaining a documented chain of custody ensures that the evidence remains authentic, unaltered, and traceable during every phase of the investigation.

---

# Evidence Acquisition

| Property | Value |
|----------|-------|
| Source | Public phishing email sample repository |
| Acquisition Method | Copied into the investigation workspace |
| File Format | .eml |
| Preservation Method | Original file retained without modification |
| Working Copy | Created for forensic analysis |
| Password Protected Archive | phishing-email.zip |

---

# Evidence Integrity

Evidence integrity was verified using cryptographic hash functions.

| Algorithm | Status |
|-----------|--------|
| MD5 | Verified |
| SHA256 | Verified |

The generated hash values matched during verification, confirming that the evidence remained unchanged throughout preservation.

---

# Evidence Handling Log

| Date | Time | Action | Analyst |
|------|------|--------|---------|
| YYYY-MM-DD | HH:MM | Original email acquired | Abdull Ashthaf CK |
| YYYY-MM-DD | HH:MM | Working copy created | Abdull Ashthaf CK |
| YYYY-MM-DD | HH:MM | MD5 generated | Abdull Ashthaf CK |
| YYYY-MM-DD | HH:MM | SHA256 generated | Abdull Ashthaf CK |
| YYYY-MM-DD | HH:MM | Hashes verified | Abdull Ashthaf CK |
| YYYY-MM-DD | HH:MM | Password-protected ZIP created | Abdull Ashthaf CK |

> Replace the date and time with the actual values from your investigation.

---

# Storage Information

| Item | Location |
|------|----------|
| Original Email | Evidence/Original-Email/phishing-email.eml |
| Protected Archive | Evidence/Original-Email/phishing-email.zip |

Archive Password:

```text
infected
```

---

# Evidence Handling Notes

- The original phishing email was never modified.
- All analysis was performed using a working copy.
- Cryptographic hashes were generated before analysis.
- The archived sample is password protected to prevent accidental execution or inspection.
- Evidence was handled within an isolated Kali Linux virtual machine.

---

# Conclusion

The integrity of the original phishing email was successfully preserved throughout the investigation.

The evidence is suitable for continued forensic analysis and documentation.
