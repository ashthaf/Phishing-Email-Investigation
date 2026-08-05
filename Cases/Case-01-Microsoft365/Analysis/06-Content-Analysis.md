# Phase 6 – Email Body Analysis

## Objective
Analyze the email content for phishing indicators, social engineering techniques, and embedded URLs.

---

## MIME Structure

| MIME Part | Description |
|------------|-------------|
| textfile0 | Empty MIME section |
| textfile1 | Plain text body |
| textfile2 | HTML body |

---

## Email Summary

The email impersonates a password reset notification from a Firebase-hosted application.

The message encourages the recipient to reset their password by clicking an embedded link.

---

## Social Engineering

- Password reset lure
- Sense of urgency
- Trusted service impersonation
- Credential harvesting attempt

---

## Email Body

Hello,

Follow this link to reset your password.

If you didn't request a password reset, ignore this email.

---

## Embedded URL

https://is.gd/...

The email uses a shortened URL, preventing the recipient from immediately identifying the final destination.

---

## Indicators of Compromise

Sender:
noreply@lolalhopb.firebaseapp.com

Subject:
Reset your password for lolalhopb

Recipient:
phishing@pot-fp@hotmail.com

Shortened URL:
https://is.gd/...

---

## Findings

- Plain-text and HTML bodies match.
- HTML contains a clickable hyperlink.
- URL shortening service (is.gd) is used.
- Email attempts credential harvesting through a fake password reset notification.

---
---

# Investigation Evidence

## Plain Text Content

![Plain Text](../Screenshots/email-text-1.png)

Plain text version of the phishing email.

---

## HTML Content

![HTML Content](../Screenshots/email-text-2.png)

HTML version of the phishing email.

---

## Extracted Body

![Body Files](../Screenshots/body-files.png)

Extracted body content reviewed for phishing indicators.

## Conclusion

This email is classified as a credential phishing attempt leveraging social engineering and a shortened URL to disguise the destination.
