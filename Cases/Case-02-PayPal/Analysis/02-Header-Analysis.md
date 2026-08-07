# 📧 Phase 02 – Header Analysis

![Status](https://img.shields.io/badge/Status-Completed-44CC11)
![Phase](https://img.shields.io/badge/Phase-02-blue)
![Category](https://img.shields.io/badge/Category-Header%20Analysis-red)
![Case](https://img.shields.io/badge/Case-02-blue)
![Evidence](https://img.shields.io/badge/Evidence-Email%20Header-orange)

---

# 📖 Overview

The objective of this phase was to extract and analyze the complete email header from the phishing email. Email headers contain critical forensic metadata that reveal information about the sender, routing path, authentication status, and message origin.

The extracted header serves as the foundation for subsequent routing, authentication, sender, and threat intelligence analysis.

---

# 🎯 Objectives

- Extract the complete email header from the original email.
- Preserve header integrity for forensic analysis.
- Verify successful extraction.
- Identify critical forensic header fields.
- Collect metadata required for subsequent investigation phases.

---

# 📂 Header Extraction

The email header was extracted from the original `.eml` file using the following command:

```bash
sed '/^$/q' sample-1407.eml > ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

The command extracts all content from the beginning of the email until the first blank line, which marks the end of the email header.

### 📸 Screenshot

*Insert screenshot showing successful header extraction.*

---

# ✅ Header File Verification

After extraction, the generated header file was verified to ensure the evidence had been successfully preserved.

**Command Used**

```bash
head ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

The output confirmed that the extracted file contained the expected SMTP header information.

### 📸 Screenshot

*Insert verification screenshot.*

---

# 📏 Header Size Verification

The total number of header lines was checked to verify that the extraction process completed successfully.

**Command Used**

```bash
wc -l ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

Verifying the line count helps ensure that the header was extracted completely without truncation.

### 📸 Screenshot

*Insert screenshot.*

---

# 🔍 Important Header Fields Identified

Manual inspection identified several forensic artifacts that are essential for subsequent investigation phases.

| Header Field | Observation |
|--------------|-------------|
| From | Present |
| Subject | Present |
| MIME-Version | Present |
| Content-Type | Present |
| Date | Present |
| Message-ID | Present |
| Return-Path | Present |
| Authentication-Results | Present |
| Received | Multiple entries present |

---

# 👤 From Header

The visible sender address identified within the email header was:

```text
service@stayfriends.de
```

This represents the address displayed to the recipient and will be validated during the Sender Analysis phase.

### 📸 Screenshot

*Insert screenshot.*

---

# 📨 Subject Header

The email subject identified during header analysis was:

```text
Ihre einmalige Chance
```

The subject uses persuasive language intended to encourage user interaction and is consistent with phishing and social engineering campaigns.

### 📸 Screenshot

*Insert screenshot.*

---

# 📄 MIME Information

The email contains standard MIME headers used for formatting HTML email content.

MIME metadata will be referenced later during the Content Analysis phase.

### 📸 Screenshot

*Insert screenshot.*

---

# 📬 Return-Path Analysis

The extracted Return-Path was:

```text
return@messaggerocappuccino.it
```

The Return-Path differs from the visible sender address (`service@stayfriends.de`).

Although this configuration can be legitimate, it is an important forensic indicator because it demonstrates that the bounce address belongs to a different domain than the address displayed to the recipient.

This discrepancy requires additional validation through:

- SPF
- DKIM
- DMARC
- SMTP Routing Analysis

### 📸 Screenshot

*Insert screenshot.*

---

# 🔐 Authentication Results

The **Authentication-Results** header contained the following results:

```text
SPF   = Pass
DKIM  = Pass
DMARC = Pass
```

These results indicate that Microsoft's mail gateway successfully validated the authentication mechanisms for the sending domain.

However, successful authentication **does not guarantee legitimacy**. Threat actors frequently abuse compromised or legitimately configured third-party infrastructure capable of passing SPF, DKIM, and DMARC validation.

A detailed examination of these authentication mechanisms is provided in **Phase 04 – Authentication Analysis**.

### 📸 Screenshot

*Insert screenshot.*

---

# 🌐 Received Headers

Multiple **Received** headers were identified during inspection.

These headers record each mail server involved in delivering the message and provide valuable evidence for reconstructing the complete delivery path.

A dedicated routing investigation is documented in **Phase 03 – Routing Analysis**.

---

# 📊 Key Findings

| Finding | Result |
|----------|--------|
| Header Extraction | Successful |
| Header Integrity | Verified |
| Multiple Received Headers | Yes |
| Return-Path Present | Yes |
| Return-Path Matches Sender | No |
| Authentication Header Present | Yes |
| SPF | Pass |
| DKIM | Pass |
| DMARC | Pass |

---

# 💡 Analyst Notes

The header extraction process successfully recovered all critical forensic metadata without altering the original evidence.

Several observations made during this phase guided the remainder of the investigation:

- Multiple routing entries are available for delivery path reconstruction.
- The Return-Path differs from the visible sender address.
- Authentication records are present and valid.
- Sufficient metadata was recovered to support sender validation, routing analysis, authentication verification, and threat intelligence enrichment.

---

# ✅ Conclusion

The email header was successfully extracted and verified, providing a complete forensic record for subsequent investigation.

The recovered metadata establishes the foundation for:

- Routing Analysis
- Sender Analysis
- Authentication Analysis
- Content Analysis
- URL Analysis
- Threat Intelligence

The presence of multiple routing entries, a distinct Return-Path domain, and complete authentication records provides valuable evidence for determining the legitimacy of the email and identifying attacker infrastructure.

---

# ➡️ Next Phase

Continue to **03-Routing-Analysis.md** to reconstruct the complete email delivery path and identify the infrastructure used to transmit the phishing email.
