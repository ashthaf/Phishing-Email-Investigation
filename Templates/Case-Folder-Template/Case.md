# SOC Case Investigation Template

> **Case ID:** ______________________
>
> **Case Name:** ______________________
>
> **Investigation Date:** ______________________
>
> **Analyst:** ______________________
>
> **Status:** Open / Closed
>
> **Severity:** Informational / Low / Medium / High / Critical

---

# Executive Summary

Provide a concise summary of the investigation.

- What was reported?
- What was investigated?
- Final verdict.

---

# Case Information

| Field | Value |
|--------|-------|
| Case ID | |
| Investigation Date | |
| Analyst | |
| Email Source | |
| Reporter | |
| Attack Type | |
| Current Status | |

---

# Investigation Timeline

| Time | Activity |
|------|----------|
| | Case Created |
| | Evidence Collected |
| | Analysis Started |
| | IOC Extraction |
| | Threat Intelligence |
| | Investigation Completed |

---

# Phase 1 — Case Intake

## Objective

Establish investigation scope.

### Evidence Collected

-

### Findings

-

### Conclusion

-

---

# Phase 2 — Evidence Preservation

## Objective

Preserve original evidence.

### Evidence Collected

- Original Email (.eml)
- MD5
- SHA256
- Chain of Custody

### Commands Used

```bash
```

### Findings

-

### Conclusion

-

---

# Phase 3 — Initial Triage

## Objective

Perform a preliminary assessment.

### Initial Observations

-

### Initial Classification

-

### Conclusion

-

---

# Phase 4 — Header Analysis

## Objective

Analyze email headers.

### Header Summary

| Header | Value |
|---------|-------|
| Subject | |
| From | |
| To | |
| Date | |
| Return-Path | |
| Reply-To | |
| Message-ID | |

### Commands Used

```bash
```

### Findings

-

### Conclusion

-

---

# Phase 5 — Routing Analysis

## Objective

Reconstruct email delivery.

### Mail Flow

```
Origin
    ↓
Relay
    ↓
Destination
```

### Routing Summary

| Item | Result |
|------|--------|
| Received Headers | |
| Mail Hops | |
| Sender IP | |
| Relay Servers | |
| TLS | |

### Commands Used

```bash
```

### Findings

-

### Conclusion

-

---

# Phase 6 — Authentication Analysis

## Objective

Verify sender authentication.

| Check | Result |
|-------|--------|
| SPF | |
| DKIM | |
| DMARC | |

### Commands Used

```bash
```

### Findings

-

### Conclusion

-

---

# Phase 7 — Sender Analysis

## Objective

Validate sender legitimacy.

### Analysis

| Item | Result |
|------|--------|
| Sender Address | |
| Display Name | |
| Reply-To | |
| Return-Path | |
| Domain Reputation | |
| Domain Age | |

### Findings

-

### Conclusion

-

---

# Phase 8 — Content Analysis

## Objective

Analyze message body.

### Observations

-

### Social Engineering Indicators

-

### Credential Harvesting Indicators

-

### Findings

-

### Conclusion

-

---

# Phase 9 — URL Analysis

## Objective

Investigate embedded URLs.

| URL | Status |
|-----|--------|
| | |

### Threat Intelligence

| Service | Result |
|----------|--------|
| VirusTotal | |
| URLScan | |
| WHOIS | |
| Cisco Talos | |

### Findings

-

### Conclusion

-

---

# Phase 10 — Attachment Analysis

## Objective

Analyze attachments.

| Attachment | Result |
|------------|--------|
| | |

### Hashes

| Algorithm | Value |
|-----------|-------|
| MD5 | |
| SHA256 | |

### Findings

-

### Conclusion

-

---

# Phase 11 — Indicators of Compromise (IOCs)

## Domains

| Domain | Description |
|---------|-------------|
| | |

---

## URLs

| URL | Description |
|-----|-------------|
| | |

---

## IP Addresses

| IP | Description |
|----|-------------|
| | |

---

## Email Addresses

| Email | Description |
|-------|-------------|
| | |

---

## File Hashes

| Hash | Type |
|------|------|
| | |

---

# Phase 12 — Threat Intelligence

| Source | Result |
|---------|--------|
| VirusTotal | |
| AbuseIPDB | |
| Cisco Talos | |
| AlienVault OTX | |
| URLhaus | |
| URLScan | |

### Findings

-

### Conclusion

-

---

# Phase 13 — MITRE ATT&CK Mapping

| ATT&CK ID | Technique |
|------------|-----------|
| | |

### Findings

-

### Conclusion

-

---

# Phase 14 — Risk Assessment

| Category | Assessment |
|-----------|------------|
| Impact | |
| Likelihood | |
| Overall Risk | |

### Justification

-

---

# Phase 15 — Containment Recommendations

- [ ]
- [ ]
- [ ]
- [ ]

---

# Final Verdict

## Classification

- [ ] Legitimate
- [ ] Spam
- [ ] Phishing
- [ ] Credential Harvesting
- [ ] Malware
- [ ] Business Email Compromise

---

## Summary

Provide a final technical summary of the investigation.

---

# Lessons Learned

- What indicators were most useful?
- What detection opportunities were identified?
- What improvements should be made?

---

# Screenshots

| Screenshot | Description |
|------------|-------------|
| | |
| | |
| | |

---

# References

- Master Phishing Investigation Playbook
- Investigation Checklist
- Threat Intelligence Sources

---

# Investigation Closure

| Item | Status |
|------|--------|
| Evidence Preserved | ✅ / ❌ |
| Analysis Completed | ✅ / ❌ |
| IOC Extraction Completed | ✅ / ❌ |
| Threat Intelligence Completed | ✅ / ❌ |
| MITRE Mapping Completed | ✅ / ❌ |
| Risk Assessment Completed | ✅ / ❌ |
| Report Completed | ✅ / ❌ |

---

**Analyst Signature**

_____________________________

**Date**

_____________________________

