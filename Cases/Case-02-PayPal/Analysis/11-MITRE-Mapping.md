# MITRE ATT&CK Mapping

## Objective

The objective of this phase is to map the observed attacker behaviors identified during the phishing email investigation to the MITRE ATT&CK framework. This mapping helps categorize the adversary's tactics and techniques using a standardized knowledge base, allowing security analysts to better understand the attack lifecycle and improve detection capabilities.

---

# MITRE ATT&CK Overview

The phishing campaign was analyzed against the MITRE ATT&CK Enterprise Matrix.

Based on the investigation, the attacker employed social engineering techniques, domain infrastructure, email impersonation, and malicious hyperlinks to lure victims into interacting with attacker-controlled infrastructure.

The following techniques were identified during the investigation.

| ATT&CK ID | Technique | Tactic | Status |
|------------|------------------------------|---------------------|---------|
| T1566 | Phishing | Initial Access | ✔ Identified |
| T1566.002 | Spearphishing Link | Initial Access | ✔ Identified |
| T1036 | Masquerading | Defense Evasion | ✔ Identified |
| T1204.001 | User Execution: Malicious Link | Execution | ✔ Identified |
| T1583.001 | Acquire Infrastructure: Domains | Resource Development | ✔ Observed |
| T1585.001 | Establish Accounts | Resource Development | ✔ Possible |

---

# Technique 1 – Phishing (T1566)

The investigation confirmed that the attacker attempted to gain initial access through a phishing email impersonating PayPal.

The email attempted to convince the recipient that they had won a PayPal gift card and encouraged interaction with embedded hyperlinks.

### Supporting Evidence

- Fake PayPal branding
- Social engineering
- HTML phishing email
- Suspicious sender infrastructure
- Malicious landing domain (easilett.com)

This behavior directly maps to **MITRE ATT&CK Technique T1566 – Phishing**.

---

# Technique 2 – Spearphishing Link (T1566.002)

The phishing email relied on embedded hyperlinks directing victims to attacker-controlled infrastructure.

Instead of delivering malware through attachments, the campaign attempted to redirect victims to an external phishing website.

### Screenshot

![MITRE T1566.002](Images/mitre-t1566-002.png)

### Supporting Evidence

- HTML hyperlinks
- URL Analysis
- easilett.com investigation
- No malicious attachment
- Credential harvesting attempt

This behavior matches **MITRE ATT&CK T1566.002 – Spearphishing Link**.

---

# Technique 3 – Masquerading (T1036)

The phishing campaign impersonated the PayPal brand to increase the likelihood that recipients would trust the email and interact with its content.

The email used:

- PayPal branding
- Financial reward lure
- Professional HTML formatting
- Legitimate-looking sender information

Although the sender domain (**stayfriends.de**) is legitimate, the email content falsely represented PayPal, making this a clear case of masquerading.

### Screenshot

![MITRE T1036](Images/mitre-t1036.png)

### Supporting Evidence

- PayPal branding
- HTML email template
- Social engineering language
- Sender identity inconsistent with the claimed organization

This behavior aligns with **MITRE ATT&CK Technique T1036 – Masquerading**.

---

# Technique 4 – User Execution: Malicious Link (T1204.001)

The phishing campaign depended on user interaction.

Rather than exploiting a software vulnerability, the attacker relied on convincing the recipient to voluntarily click a malicious hyperlink embedded within the email.

### Screenshot

![MITRE T1204.001](Images/mitre-t1204.png)

### Supporting Evidence

- Embedded phishing URL
- HTML hyperlink
- External phishing infrastructure
- No malware attachment
- User interaction required

This behavior maps directly to **MITRE ATT&CK Technique T1204.001 – User Execution: Malicious Link**.

---

# Technique 5 – Acquire Infrastructure: Domains (T1583.001)

The investigation identified **easilett.com** as the primary suspicious domain associated with the phishing campaign.

Threat intelligence analysis revealed:

- Active DNS records
- Newly registered infrastructure
- Missing SPF record
- Missing DMARC policy
- VirusTotal phishing detection

These findings indicate that the attacker acquired or controlled domain infrastructure to support the phishing operation.

### Supporting Evidence

- easilett.com
- WHOIS analysis
- MXToolbox analysis
- VirusTotal
- URLScan.io

This behavior aligns with **MITRE ATT&CK Technique T1583.001 – Acquire Infrastructure: Domains**.

---

# Technique 6 – Establish Accounts (T1585.001)

The phishing email was delivered using active email infrastructure and SMTP services.

The investigation identified:

- Sender email address
- Return-Path address
- SMTP routing infrastructure
- Multiple mail servers involved in delivery

Although there is no evidence that the attacker personally created these accounts, the use of email infrastructure to conduct phishing activity makes this technique a possible component of the campaign.

### Supporting Evidence

- Sender analysis
- Return-Path analysis
- Header analysis
- SMTP routing

This behavior is consistent with **MITRE ATT&CK Technique T1585.001 – Establish Accounts**.

---

# ATT&CK Mapping Summary

| ATT&CK ID | Technique | Tactic | Evidence |
|------------|------------------------------|----------------------|--------------------------------|
| T1566 | Phishing | Initial Access | PayPal phishing email |
| T1566.002 | Spearphishing Link | Initial Access | Embedded phishing links |
| T1036 | Masquerading | Defense Evasion | Fake PayPal branding |
| T1204.001 | User Execution: Malicious Link | Execution | Victim required to click hyperlink |
| T1583.001 | Acquire Infrastructure: Domains | Resource Development | easilett.com |
| T1585.001 | Establish Accounts | Resource Development | Sender and Return-Path infrastructure |

---

# Analyst Assessment

The phishing campaign primarily relied on social engineering rather than malware delivery.

The attacker impersonated a trusted financial service, embedded malicious hyperlinks within an HTML email, and directed victims toward attacker-controlled infrastructure.

Unlike malware-based campaigns, this attack depended entirely on user interaction and credential theft rather than exploiting software vulnerabilities.

The MITRE ATT&CK mapping demonstrates that the campaign focused on **Initial Access** through phishing while using masquerading and attacker-controlled infrastructure to increase credibility.

---

# Conclusion

Mapping the investigation findings to the MITRE ATT&CK framework provides valuable insight into the attacker's tactics, techniques, and procedures (TTPs).

The phishing campaign primarily leveraged social engineering, domain infrastructure, and malicious hyperlinks to achieve its objectives.

The identified ATT&CK techniques provide a standardized representation of the observed attacker behavior and can assist security teams in improving detection rules, threat hunting activities, and defensive strategies against similar phishing campaigns.
