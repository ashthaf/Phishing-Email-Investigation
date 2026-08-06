# Content Analysis

## Objective

The purpose of this phase was to analyze the extracted HTML email body to identify phishing indicators, embedded content, external resources, and any malicious elements used to deceive the recipient.

---

# Email Body Extraction

The email body was extracted from the original `.eml` file using `ripmime`.

### Command

```bash
ripmime -i sample-1407.eml -d ~/CyberLab/Cases/Case-02-paypal/Evidence/Email-body
```

### Screenshot

![Email Body Extraction](../Screenshots/content-analysis/Body-files.png)

---

# HTML File Verification

The extracted file was verified using the `file` command.

### Command

```bash
file phishing-email.html
```

### Observation

The extracted email body is an HTML document encoded in UTF-8 with CRLF line terminators.

### Screenshot

![HTML File Verification](../Screenshots/content-analysis/html-file-found.png)

---

# Original Email Verification

The original email sample was verified before extraction.

### Command

```bash
file sample-1407.eml
```

### Observation

The sample is a valid RFC 822 email message containing HTML content.

### Screenshot

![Original Email Information](../Screenshots/content-analysis/file-information.png)

---

# Rendered Email Analysis

The extracted HTML email was opened locally inside Firefox for visual inspection.

### Command

```bash
firefox phishing-email.html
```

### Observations

- The email is written in German.
- It impersonates a PayPal promotional campaign.
- The recipient is informed that they have won a **1000€ PayPal Gift Card**.
- The email contains personalized information ("phishing@pot") to increase credibility.
- Multiple hyperlinks encourage the victim to claim the prize.

### Screenshot

![Rendered Email](../Screenshots/content-analysis/email-full.png)

---

# Call-to-Action Analysis

The email contains several hyperlinks encouraging the victim to claim the advertised reward.

Examples include:

- "HIER bestätigen"
- "100% Gratis mitmachen"

These links are intended to redirect victims to an external phishing website.

### Screenshot

![Call To Action](../Screenshots/content-analysis/cta.png)

---

# Footer Analysis

The email footer contains an unsubscribe-style message intended to appear legitimate.

Displayed text:

> click here to remove yourself from our emails list

Although it resembles a legitimate unsubscribe option, the hyperlink points to an external domain unrelated to PayPal.

### Screenshot

![Footer](../Screenshots/content-analysis/footer.png)

---

# Footer Hyperlink Analysis

Inspection of the HTML source shows the unsubscribe link redirects to:

```
http://easilett.com/oop/531_md/31/2/82/23/2459859
```

This domain is unrelated to PayPal and represents another phishing indicator.

### Screenshot

![Footer Hyperlink](../Screenshots/content-analysis/footer-hreflink.png)

---

# Embedded Hyperlinks

Hyperlinks embedded within the email were extracted using:

```bash
grep -i href phishing-email.html
```

### Findings

Several hyperlinks reference the same external domain:

```
http://easilett.com/
```

instead of legitimate PayPal infrastructure.

This strongly indicates phishing activity.

### Screenshot

![Embedded Links](../Screenshots/content-analysis/email-href.png)

---

# Embedded Images

Embedded image references were extracted using:

```bash
grep -i img phishing-email.html
```

### Findings

The email loads externally hosted images from:

```
http://easilett.com/media/
```

instead of PayPal servers.

These images are used to imitate a legitimate promotional email while keeping malicious content hosted remotely.

### Screenshot

![Embedded Images](../Screenshots/content-analysis/email-img.png)

---

# HTML Form Analysis

The email was examined for embedded HTML forms.

### Command

```bash
grep -i form phishing-email.html
```

### Finding

No HTML forms were identified inside the email.

The phishing campaign relies on redirecting victims to an external website rather than collecting credentials directly within the email.

*(Insert screenshot if available.)*

---

# JavaScript Analysis

The HTML was inspected for JavaScript.

### Command

```bash
grep -i script phishing-email.html
```

### Finding

No JavaScript was identified.

The phishing email depends entirely on embedded hyperlinks rather than client-side scripting.

*(Insert screenshot if available.)*

---

# Content Analysis Summary

| Indicator | Result |
|-----------|--------|
| HTML Email | ✅ Present |
| Personalized Content | ✅ Present |
| PayPal Impersonation | ✅ Present |
| External Hyperlinks | ✅ Present |
| External Images | ✅ Present |
| Call-to-Action Links | ✅ Present |
| Fake Unsubscribe Link | ✅ Present |
| HTML Forms | ❌ Not Present |
| JavaScript | ❌ Not Present |

---

# Conclusion

The content analysis confirms that this is a phishing email impersonating a PayPal promotional campaign.

Key phishing characteristics include:

- Impersonation of a trusted brand (PayPal)
- Personalized recipient information
- Multiple call-to-action hyperlinks
- External resources hosted on an unrelated domain (`easilett.com`)
- Fake unsubscribe mechanism
- HTML formatting designed to appear legitimate

Although the email does not contain embedded forms or JavaScript, it attempts to lure recipients to an attacker-controlled website where further phishing activity is expected to occur.
