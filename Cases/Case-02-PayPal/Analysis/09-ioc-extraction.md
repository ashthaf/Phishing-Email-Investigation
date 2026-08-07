# IOC Extraction

## Objective

The objective of this phase is to identify and document all Indicators of Compromise (IOCs) extracted from the phishing email. These indicators can be used for threat hunting, detection engineering, blocking malicious infrastructure, and future incident response activities.

---

# IOC Summary

| IOC Type | Value | Assessment |
|----------|-------|------------|
| Sender Email | service@stayfriends.de | Suspicious |
| Return-Path | return@messagsgerocappuccino.it | Suspicious |
| Reply-To | Not Present | N/A |
| Subject | 1.000€ Gratis Paypal Guthabenkarte, phishing@pot | Social Engineering Lure |
| Source IP | 77.91.100.118 | Suspicious |
| Internal Relay IP | 10.167.8.70 | Internal Infrastructure |
| Domain | fonts.googleapis.com | Legitimate |
| Attachment | None | No Attachment Found |
| MIME Type | text/html | HTML Email |
| Message-ID | Not Present | N/A |

---

# Sender Email

The sender address was extracted from the email header.

```bash
grep "^From:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Output

- **Sender:** `service@stayfriends.de`

### Screenshot

![Sender Email](../Screenshots/IOC-extraction/from-header.png)

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

![Return Path](../Screenshots/IOC-extraction/return-path.png)

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

![Subject](../Screenshots/IOC-extraction/subject-header.png)

### Observation

The subject uses a financial reward ("Free PayPal Gift Card") to entice recipients into opening the email.

---

# Message-ID

The Message-ID field was examined.

```bash
grep "^Message-ID:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Screenshot

![Message ID](../Screenshots/IOC-extraction/message-id-header.png)

### Observation

No Message-ID value was found in the extracted header, which is unusual and worth documenting.

---

# Received Headers

The Received headers were reviewed to identify the originating mail server.

```bash
grep "^Received:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

### Screenshot

![Received Headers](../Screenshots/IOC-extraction/received-headers.png)

### Observation

Analysis indicates the email ultimately originated from:

- **77.91.100.118**
- Domain: **messagsgerocappuccino.it**

This infrastructure should be considered suspicious.

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

The external IP (77.91.100.118) is considered the primary IOC, while 10.167.8.70 appears to belong to internal mail infrastructure.

---

# URL Extraction

URLs embedded within the HTML email were extracted.

### Screenshot

![URL Extraction](../Screenshots/IOC-extraction/url-extraction.png)

### Observation

Only one external resource was identified:

- https://fonts.googleapis.com/

This is a legitimate Google-hosted stylesheet used for formatting and is not considered malicious.

---

# Domain Extraction

Domains were extracted from the identified URLs.

### Screenshot

![Domain Extraction](../Screenshots/IOC-extraction/domain-extraction.png)

### Extracted Domain

- fonts.googleapis.com

### Observation

The extracted domain is legitimate and does not indicate malicious activity.

---

# Attachment Check

The email was examined for attachments.

### Screenshot

![Attachment Search](../Screenshots/IOC-extraction/attachment-search.png)

### Observation

No attachments were found within the email.

---

# MIME Type

The Content-Type header was examined.

### Screenshot

![Content Type](../Screenshots/IOC-extraction/content-type.png)

### Result

- text/html
- charset=UTF-8

### Observation

The phishing email consists of HTML content and does not contain any attached files.

---

# IOC Summary

| IOC | Classification |
|------|----------------|
| service@stayfriends.de | Suspicious Sender |
| return@messagsgerocappuccino.it | Suspicious Return-Path |
| 77.91.100.118 | Suspicious External IP |
| fonts.googleapis.com | Legitimate Domain |
| HTML Email | Email Format |
| No Attachment | Verified |

---

# Conclusion

The IOC extraction phase identified several indicators associated with the phishing campaign. The sender email, Return-Path, and originating IP address are considered suspicious and should be retained for further threat intelligence analysis. No malicious attachments were identified, and the only extracted domain (`fonts.googleapis.com`) is a legitimate external resource used for rendering HTML content.

The extracted IOCs will be validated during the Threat Intelligence phase to determine their reputation, historical activity, and potential association with known phishing infrastructure.
