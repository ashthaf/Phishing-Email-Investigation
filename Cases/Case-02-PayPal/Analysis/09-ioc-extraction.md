# IOC Extraction

## Objective

The objective of this phase is to identify and document all Indicators of Compromise (IOCs) extracted from the phishing email. These indicators can be used for threat hunting, detection engineering, blocking malicious infrastructure, and future incident response activities.

---

# IOC Summary

| IOC Type          | Value                                                                      | Assessment              |
| ----------------- | -------------------------------------------------------------------------- | ----------------------- |
| Sender Email      | [service@stayfriends.de](mailto:service@stayfriends.de)                    | Suspicious              |
| Return-Path       | [return@messagsgerocappuccino.it](mailto:return@messagsgerocappuccino.it)  | Suspicious              |
| Reply-To          | Not Present                                                                | N/A                     |
| Subject           | 1.000€ Gratis Paypal Guthabenkarte, phishing@pot                           | Social Engineering Lure |
| Source IP         | 77.91.100.118                                                              | Suspicious              |
| Internal Relay IP | 10.167.8.70                                                                | Internal Infrastructure |
| Domain            | easilett.com                                                               | Suspicious              |
| Domain            | fonts.googleapis.com                                                       | Legitimate              |
| Attachment        | None                                                                       | No Attachment Found     |
| MIME Type         | text/html                                                                  | HTML Email              |
| Message-ID        | Not Present                                                                | N/A                     |

---

# Sender Email

The sender address was extracted from the email header.

```bash
grep "^From:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Output

- **Sender:** `service@stayfriends.de`

### Screenshot

![From Header](../Screenshots/IOC-extraction/from-header.png)

### Observation

The sender claims to originate from **stayfriends.de**, which is unrelated to PayPal and indicates possible sender spoofing or abuse of a compromised mail server.

---

# Return-Path

The Return-Path identifies the envelope sender used during SMTP delivery.

```bash
grep "^Return-Path:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Output

- **Return-Path:** `return@messagsgerocappuccino.it`

### Screenshot

![Return Path](../Screenshots/IOC-extraction/rp.png)

### Observation

The Return-Path domain differs from the visible sender address, which is a common phishing characteristic.

---

# Reply-To Header

The Reply-To header was searched to determine whether replies would be redirected to another mailbox.

```bash
grep "^Reply-To:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Result

No Reply-To header was present.

### Observation

Although many phishing emails abuse the Reply-To field, this email does not include one. This is recorded as an investigative finding.

---

# Email Subject

The subject line was extracted from the header.

```bash
grep "^Subject:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Output

- **Subject:** `1.000€ Gratis Paypal Guthabenkarte, phishing@pot`

### Screenshot

![Subject Header](../Screenshots/IOC-extraction/subject-header.png)

### Observation

The subject uses a financial reward ("Free PayPal Gift Card") to entice recipients into opening the email.

---

# Message-ID

The Message-ID field was examined.

```bash
grep "^Message-ID:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Screenshot

![Message-ID Header](../Screenshots/IOC-extraction/Message-ID-header.png)

### Observation

No Message-ID value was found in the extracted header, which is unusual and worth documenting.
---

# Received Headers

The Received headers were reviewed to identify the originating mail server.

```bash
grep "^Received:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Screenshot

![Received Headers](../Screenshots/IOC-extraction/Received-headers.png)

### Observation

Analysis indicates the email ultimately originated from:

- **77.91.100.118**
- Internal Relay: **10.167.8.70**
- Associated Domain: **messagsgerocappuccino.it**

The external IP address is considered suspicious and represents the originating mail infrastructure used to deliver the phishing email.

---

# Extracted IP Addresses

The IP addresses were extracted from the email.

```bash
grep -Eo '([0-9]{1,3}\.){3}[0-9]{1,3}' sample-1407.eml | sort -u
```

### Screenshot

![IP Addresses](../Screenshots/IOC-extraction/ip-addresses.png)

### Extracted IPs

- 77.91.100.118
- 10.167.8.70

### Observation

The external IP (**77.91.100.118**) is considered the primary IOC, while **10.167.8.70** belongs to the internal mail infrastructure and is not considered malicious.

---

# URL Extraction

URLs embedded within the HTML email were extracted.

### Screenshot

![URL Extraction](../Screenshots/IOC-extraction/url-extraction.png)

### Observation

The investigation identified both legitimate and suspicious URLs within the email.

Extracted resources include:

- https://fonts.googleapis.com/
- http://easilett.com/

The Google Fonts URL is a legitimate resource used to render the HTML email.

The **easilett.com** domain was identified within the phishing email body and footer. It is unrelated to PayPal and is considered the primary suspicious URL associated with this phishing campaign.

---

# Domain Extraction

Domains were extracted from the identified URLs.

### Screenshot

![Domain Extraction](../Screenshots/IOC-extraction/domain-extraction.png)

### Extracted Domains

- easilett.com
- fonts.googleapis.com

### Observation

Two domains were identified during the investigation.

**easilett.com**

- Unrelated to PayPal
- Embedded within the phishing email
- Used as the primary phishing infrastructure
- Investigated during the URL Analysis phase using:
  - WHOIS
  - DNS
  - VirusTotal
  - URLScan
  - Cisco Talos
  - MXToolbox
  - AbuseIPDB

**fonts.googleapis.com**

- Legitimate Google-hosted service
- Used only for loading web fonts
- Not considered malicious

---

# Attachment Check

The email was examined for attachments.

### Screenshot

![Attachment Search](../Screenshots/IOC-extraction/Attachement-search.png)

### Observation

No attachments were found within the email.

The phishing campaign relied entirely on HTML content and embedded hyperlinks rather than malicious file attachments.

---

# MIME Type

The Content-Type header was examined.

### Screenshot

![Content Type](../Screenshots/IOC-extraction/content-type.png)

### Result

- text/html
- charset=UTF-8

### Observation

The phishing email consists solely of HTML content and does not contain any attached files.

---

# IOC Summary

| IOC | Classification |
|------|----------------|
| service@stayfriends.de | Suspicious Sender |
| return@messagsgerocappuccino.it | Suspicious Return-Path |
| 77.91.100.118 | Suspicious External IP |
| easilett.com | Suspicious Domain |
| fonts.googleapis.com | Legitimate Domain |
| HTML Email | Email Format |
| No Attachment | Verified |

---

# Conclusion

The IOC extraction phase successfully identified multiple indicators associated with this phishing campaign.

The following indicators should be retained for detection, threat hunting, and future investigations:

- **Sender Email:** service@stayfriends.de
- **Return-Path:** return@messagsgerocappuccino.it
- **External Source IP:** 77.91.100.118
- **Suspicious Domain:** easilett.com

The domain **easilett.com** was identified as the primary phishing infrastructure after URL analysis and is considered the most significant IOC extracted from this investigation.

The domain **fonts.googleapis.com** is a legitimate Google-hosted resource used for rendering HTML content and does not represent malicious activity.

No malicious attachments were identified. Instead, the phishing campaign relied on HTML formatting and embedded hyperlinks to redirect victims to attacker-controlled infrastructure.

The extracted IOCs will be validated further during the **Threat Intelligence** phase to determine their reputation, historical activity, and association with known phishing campaigns.

