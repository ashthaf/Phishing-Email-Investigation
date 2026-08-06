# Header Analysis

## Objective

The objective of this phase is to extract the complete email header from the phishing email and identify important metadata required for further forensic investigation.

---

# Header Extraction

The email header was extracted from the original `.eml` file using the following command:

```bash
sed '/^$/q' sample-1407.eml > ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

This command extracts everything from the beginning of the email until the first blank line, which represents the complete email header.

### Screenshot

![Header Extraction](../Screenshots/header-analysis/header-extraction.png)

---

# Header File Verification

After extraction, the generated header file was verified.

Command used:

```bash
head ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

This confirmed that the header was successfully extracted before continuing the investigation.

### Screenshot

![Header Saved](../Screenshots/header-analysis/header-saved.png)

---

# Header Size Verification

The total number of header lines was verified.

Command:

```bash
wc -l ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

This helps ensure that the entire header was extracted successfully.

### Screenshot

![Header Line Count](../Screenshots/header-analysis/header-line-count.png)

---

# Important Header Fields Identified

Several important forensic headers were identified during manual inspection.

| Header | Observation |
|---------|-------------|
| From | Present |
| Subject | Present |
| MIME-Version | Present |
| Content-Type | Present |
| Date | Present |
| Message-ID | Present |
| Return-Path | Present |
| Authentication-Results | Present |
| Received | Multiple headers present |

---

# From Header

The visible sender address identified in the email header is:

```
service@stayfriends.de
```

### Screenshot

![From Header](../Screenshots/header-analysis/from-header.png)

---

# Subject Header

The email subject identified was:

```
Ihre einmalige Chance
```

### Screenshot

![Subject Header](../Screenshots/header-analysis/subject-header.png)

---

# MIME Information

The email uses MIME encoding for formatting.

### Screenshot

![MIME Information](../Screenshots/header-analysis/mime-info.png)

---

# Return-Path

The email contains the following Return-Path:

```
return@messaggerocappuccino.it
```

The Return-Path differs from the visible sender address.

This indicates that although the user sees the email coming from **stayfriends.de**, bounce messages are directed to **messaggerocappuccino.it**, suggesting the email was transmitted through separate mail infrastructure.

A different Return-Path is not unusual by itself, but it is an important indicator that should be validated together with SPF, DKIM, DMARC, and routing analysis.

### Screenshot

![Return Path](../Screenshots/header-analysis/rp.png)

---

# Authentication Results Header

The Authentication-Results header was extracted for detailed analysis.

Observed result:

```
SPF = Pass
DKIM = Pass
DMARC = Pass
```

These authentication results indicate that the email passed domain authentication checks at Microsoft's mail gateway.

However, successful authentication alone does **not** guarantee that an email is legitimate because attackers may send emails from compromised or legitimately configured third-party infrastructure.

Detailed authentication analysis is documented separately in the Authentication Analysis phase.

### Screenshot

![Authentication Results](../Screenshots/header-analysis/Authentication-Results.png)

---

# Received Headers

Multiple Received headers were identified.

These will be analyzed separately during the Routing Analysis phase to reconstruct the email delivery path from the originating server to Microsoft's mail infrastructure.

---

# Initial Findings

The header extraction phase successfully recovered the complete email metadata required for forensic analysis.

Key observations include:

- Complete email header extracted successfully.
- Multiple Received headers identified.
- Return-Path present and differs from the visible sender.
- Authentication-Results header present.
- SPF, DKIM, and DMARC passed.
- Sender information, routing information, and authentication data are available for further investigation.

---

# Conclusion

The header extraction was completed successfully without data loss.

The extracted header provides sufficient forensic evidence to proceed with:

- Routing Analysis
- Sender Analysis
- Authentication Analysis
- Content Analysis
- URL Analysis

The presence of multiple routing headers, a distinct Return-Path domain, and successful authentication records provides a strong foundation for the remaining phases of the investigation.
