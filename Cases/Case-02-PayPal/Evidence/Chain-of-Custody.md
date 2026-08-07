# 🔒 Chain of Custody

![Evidence](https://img.shields.io/badge/Evidence-Chain%20of%20Custody-blue)
![Integrity](https://img.shields.io/badge/Integrity-Preserved-brightgreen)
![Status](https://img.shields.io/badge/Status-Complete-green)

---

# 📖 Overview

This document records the handling of digital evidence throughout the PayPal phishing email investigation. Maintaining a documented chain of custody helps ensure the integrity, authenticity, and traceability of evidence used during the investigation.

---

# Investigation Information

| Item | Value |
|------|-------|
| Case ID | CASE-02 |
| Case Name | PayPal Phishing Email Investigation |
| Incident Type | Credential Harvesting Phishing |
| Primary Evidence | sample-1407.eml |
| Investigator | Abdull Ashthaf CK |
| Investigation Platform | Kali Linux Virtual Machine |

---

# Evidence Handling Log

| Date / Phase | Action | Evidence | Performed By |
|--------------|--------|----------|--------------|
| Initial Triage | Original phishing email received and preserved | sample-1407.eml | Abdull Ashthaf CK |
| Header Analysis | Email headers extracted for forensic analysis | email-header.txt | Abdull Ashthaf CK |
| Routing Analysis | Received headers analyzed | Received-header.txt | Abdull Ashthaf CK |
| Content Analysis | HTML body extracted | phishing-email.html | Abdull Ashthaf CK |
| URL Analysis | URLs and domains extracted | extracted_urls.txt, domains.txt | Abdull Ashthaf CK |
| DNS Analysis | DNS lookup performed | dig.txt | Abdull Ashthaf CK |
| WHOIS Analysis | WHOIS information collected | whois.txt | Abdull Ashthaf CK |
| IOC Extraction | Indicators of Compromise documented | IOC Summary | Abdull Ashthaf CK |
| Threat Intelligence | External validation completed | VirusTotal, URLScan, Talos, AbuseIPDB | Abdull Ashthaf CK |
| Final Reporting | Incident documentation completed | Investigation Report | Abdull Ashthaf CK |

---

# Evidence Integrity

Throughout the investigation:

- The original phishing email remained preserved.
- Analysis was performed using extracted artifacts where applicable.
- No evidence was intentionally modified.
- Findings were documented immediately after each analysis phase.
- Supporting screenshots were captured throughout the investigation.

---

# Evidence Storage

| Evidence Type | Location |
|---------------|----------|
| Original Email | Evidence/Original-Email |
| Headers | Headers |
| URL Artifacts | Artifacts/URL-Analysis |
| Investigation Notes | Evidence |
| Screenshots | Screenshots |

---

# Conclusion

The chain of custody was maintained throughout the investigation. Evidence was preserved, documented, and analyzed in a controlled environment, ensuring the integrity and reproducibility of the investigation.
