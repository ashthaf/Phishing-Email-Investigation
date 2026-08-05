# Investigation Notes

## General Observations

- Email impersonates Microsoft 365.
- Social engineering techniques were used to create urgency.
- A shortened URL redirected the user toward a credential harvesting page.
- Sender authentication (SPF, DKIM, and DMARC) passed, indicating abuse of legitimate infrastructure rather than spoofing.

---

## Technical Notes

- Email headers extracted successfully.
- Mail routing reconstructed.
- URLs expanded and analyzed.
- WHOIS and DNS information reviewed.
- Threat intelligence sources consulted.
- MITRE ATT&CK techniques mapped.
- Risk classified as High.

---

## Lessons During Investigation

- Authentication success does not imply legitimacy.
- URL shortening services can conceal malicious destinations.
- Multiple intelligence sources should be used before reaching a conclusion.
