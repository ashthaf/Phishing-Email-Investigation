# Case 01 – Investigation Notes

## Analyst

**Name:** Abdull Ashthaf CK

---

## Investigation Goal

Determine whether the received Microsoft 365 email is a legitimate message or a phishing attempt by analyzing the email headers, sender information, URLs, attachments, and threat intelligence.

---

# Initial Observations

At the beginning of the investigation, the following assumptions were made:

- The email claims to originate from Microsoft 365.
- The legitimacy of the sender has not yet been verified.
- Email headers require detailed analysis.
- URLs have not yet been validated.
- Attachments have not yet been inspected.
- No Indicators of Compromise (IOCs) have been confirmed.

---

# Working Hypotheses

## Hypothesis 1

The sender address may be spoofed.

**Status:** Pending

---

## Hypothesis 2

The embedded URLs may redirect users to a credential harvesting website.

**Status:** Pending

---

## Hypothesis 3

The email may fail SPF, DKIM, or DMARC validation.

**Status:** Pending

---

## Hypothesis 4

The infrastructure used by the attacker may already be reported in threat intelligence databases.

**Status:** Pending

---

# Investigation Checklist

- [ ] Preserve original email
- [ ] Export email headers
- [ ] Analyze Received headers
- [ ] Identify originating IP address
- [ ] Check SPF record
- [ ] Check DKIM signature
- [ ] Check DMARC policy
- [ ] Extract all URLs
- [ ] Analyze URLs
- [ ] Check domain reputation
- [ ] Perform WHOIS lookup
- [ ] Perform DNS lookup
- [ ] Extract Indicators of Compromise
- [ ] Map MITRE ATT&CK techniques
- [ ] Write final incident report

---

# Evidence Collected

| Evidence | Status |
|-----------|--------|
| Original Email | Pending |
| Email Headers | Pending |
| URLs | Pending |
| Attachments | Pending |
| IOC List | Pending |
| Screenshots | Pending |

---

# IOC Summary

| IOC Type | Value | Status |
|----------|-------|--------|
| Sender Email | Pending | Pending |
| Sender Domain | Pending | Pending |
| Source IP | Pending | Pending |
| URLs | Pending | Pending |
| Domains | Pending | Pending |
| Hashes | Pending | Pending |

---

# Final Notes

This notebook will be updated throughout the investigation as additional evidence is collected, analyzed, and verified.
