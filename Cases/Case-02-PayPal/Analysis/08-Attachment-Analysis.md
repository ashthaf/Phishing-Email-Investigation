# 📎 Phase 08 – Attachment Analysis

![Status](https://img.shields.io/badge/Status-Completed-44CC11)
![Phase](https://img.shields.io/badge/Phase-08-blue)
![Category](https://img.shields.io/badge/Category-Attachment%20Analysis-red)
![Case](https://img.shields.io/badge/Case-02-blue)
![Evidence](https://img.shields.io/badge/Evidence-Email%20Attachments-orange)

---

# 📖 Overview

The purpose of this phase was to determine whether the phishing email contained any malicious file attachments that could be used to deliver malware. The investigation focused on identifying common attachment types such as PDF documents, Microsoft Office files, archives, executables, scripts, and other potentially malicious files.

The extracted email contents and MIME headers were examined to verify whether the phishing campaign relied on file-based malware delivery or solely on embedded HTML content.

---

# 🎯 Objectives

The objectives of this phase were to:

- Identify any extracted attachment files.
- Search for common malicious attachment types.
- Review MIME headers for attachment indicators.
- Verify the email's Content-Type.
- Determine whether the phishing campaign relied on malware attachments or credential harvesting.

---

# 🔍 Methodology

The extracted email contents were examined using Linux command-line utilities. The investigation included:

- Listing extracted files.
- Searching for common attachment types.
- Reviewing MIME headers.
- Checking for attachment-related headers.

---

# 📂 Step 1 – List Extracted Files

The extracted email directory was inspected.

### Command

```bash
ls -lah
```

### Result

Only one HTML file was extracted.

### Screenshot

![Attachment Files](../Screenshots/Attachement-analysis/Attachemnt-files.png)

---

# 📂 Step 2 – Search for Attachments

A recursive search was performed to identify all extracted files.

### Command

```bash
find . -type f
```

### Result

Only the HTML email body was present.

```text
./phishing-email.html
```

### Screenshot

![Attachment Search](../Screenshots/Attachement-analysis/Attachement-search.png)

---

# 📄 Step 3 – Search for Common Attachment Types

The following attachment types were searched:

- PDF
- Microsoft Word
- Microsoft Excel
- ZIP archives
- RAR archives
- Executable files
- JavaScript
- VBScript
- ISO images
- Windows shortcut files

### Example Commands

```bash
find . -name "*.pdf"
find . -name "*.doc"
find . -name "*.xls"
find . -name "*.zip"
find . -name "*.exe"
```

### Result

No attachment files were identified.

### Screenshot

![Attachment Types](../Screenshots/Attachement-analysis/Attachement-types.png)

---

# 📑 Step 4 – Check Content-Disposition

The email headers were inspected to determine whether any MIME attachment sections were present.

### Command

```bash
grep -i "Content-Disposition" sample-1407.eml
```

An additional search for the keyword **attachment** was also performed.

```bash
grep -i "attachment" sample-1407.eml
```

### Result

No attachment-related headers were found.

### Screenshot

![Content Disposition](../Screenshots/Attachement-analysis/content-disposition.png)

---

# 📧 Step 5 – Verify MIME Content-Type

The MIME type of the email was examined.

### Command

```bash
grep -i "Content-Type" sample-1407.eml
```

### Result

The email contains:

```text
Content-Type: text/html; charset="UTF-8"
```

This confirms that the email consists solely of an HTML message body.

### Screenshot

![Content Type](../Screenshots/Attachement-analysis/content-type.png)

---

# 📊 Findings

| Indicator | Result |
|-----------|--------|
| HTML Email Body | ✅ Present |
| PDF Attachments | ❌ Not Found |
| Microsoft Office Documents | ❌ Not Found |
| ZIP Archives | ❌ Not Found |
| Executable Files | ❌ Not Found |
| JavaScript Attachments | ❌ Not Found |
| VBScript Files | ❌ Not Found |
| ISO Images | ❌ Not Found |
| Windows Shortcut Files | ❌ Not Found |
| MIME Attachments | ❌ Not Present |

---

# 💡 Analyst Assessment

The attachment analysis confirmed that the phishing email does not rely on file-based malware delivery.

No attachments, MIME attachment sections, or executable content were identified during the investigation. Instead, the email consists entirely of HTML content designed to persuade recipients to interact with embedded hyperlinks.

This behavior is consistent with modern **credential harvesting phishing campaigns**, where attackers avoid malicious attachments to reduce detection rates and instead redirect victims to attacker-controlled websites for credential theft.

---

# ✅ Conclusion

The investigation confirmed that the phishing email does **not** contain any file attachments or embedded malware payloads. The message is composed entirely of an HTML email (`text/html`) and does not include MIME attachment sections such as `Content-Disposition: attachment`.

Rather than distributing malware through attached files, the threat actor relies on embedded hyperlinks within the HTML content to redirect victims to external infrastructure. This approach is characteristic of a **credential harvesting phishing campaign**, where the primary objective is to obtain sensitive information rather than execute malicious code on the victim's system.

---

# ➡️ Next Phase

Continue to **Phase 09 – IOC Extraction** to identify and document the Indicators of Compromise (IOCs) collected throughout the investigation for use in threat hunting, detection engineering, and incident response.
