# Extracted Artifacts

This directory stores all indicators and artifacts extracted from the investigated email.

These files are populated during the investigation and are intended to make correlation, searching, and IOC sharing easier.

---

## Files

### domains.txt

Contains every unique domain identified during the investigation.

Example

```
microsoft.com
login.microsoftonline.com
evil-login.example
```

---

### email-addresses.txt

Contains every unique email address identified.

Example

```
support@microsoft.com
attacker@example.com
victim@company.com
```

---

### filenames.txt

Contains filenames extracted from attachments or URLs.

Example

```
Invoice.pdf
Payment.docm
ResetPassword.html
```

---

### ips.txt

Contains all IPv4/IPv6 addresses discovered.

Example

```
104.26.5.32
185.199.110.153
```

---

### message-ids.txt

Contains Message-ID values extracted from email headers.

Example

```
<CAEP4A....@mail.gmail.com>
```

---

### urls.txt

Contains every extracted URL.

Store one URL per line.

Example

```
https://login.microsoftonline.com/
https://evil-example.com/login
```

---

## Investigation Rules

- Store only unique values.
- Preserve original formatting whenever possible.
- One artifact per line.
- Never modify original evidence while extracting artifacts.
