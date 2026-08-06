# CASE-02 – PayPal Gift Card Phishing Investigation

## Case Information

| Field | Value |
|--------|-------|
| Case ID | CASE-02 |
| Incident Type | Phishing |
| Category | Credential Harvesting |
| Impersonated Brand | PayPal |
| Delivery Method | Email |
| Sample | sample-1407.eml |
| Analyst | Abdull Ashthaf CK |
| Investigation Platform | Kali Linux |
| Status | In Progress |

---

## Detection Source

User-reported phishing email submitted for security analysis.

---

## Initial Severity

**High**

Reason:

- Brand impersonation
- Social engineering
- Suspicious external URLs
- Potential credential theft

---

## Investigation Objectives

- Preserve evidence
- Verify sender authenticity
- Analyze email headers
- Reconstruct mail route
- Validate SPF/DKIM/DMARC
- Extract Indicators of Compromise (IOCs)
- Perform threat intelligence enrichment
- Map attacker behavior to MITRE ATT&CK
- Produce containment recommendations
