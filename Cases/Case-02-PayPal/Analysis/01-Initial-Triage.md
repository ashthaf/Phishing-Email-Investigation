# 🚨 Phase 01 – Initial Triage

![Status](https://img.shields.io/badge/Status-Completed-44CC11)
![Phase](https://img.shields.io/badge/Phase-01-blue)
![Category](https://img.shields.io/badge/Category-Initial%20Triage-red)
![Severity](https://img.shields.io/badge/Severity-High-red)
![Case](https://img.shields.io/badge/Case-02-blue)

---

# 📖 Overview

The **Initial Triage** phase focused on performing a safe preliminary assessment of the suspicious email while preserving the integrity of the original evidence. During this stage, no interaction with embedded hyperlinks, remote content, or external resources was performed.

The email was examined inside an isolated **Kali Linux** virtual machine using **Mozilla Thunderbird** to identify visible phishing indicators before proceeding with detailed forensic analysis.

---

# 🎯 Objectives

- Preserve the original email evidence.
- Perform a safe visual inspection of the email.
- Identify obvious phishing indicators.
- Determine whether further forensic investigation is required.
- Prevent accidental interaction with attacker-controlled infrastructure.

---

# 🖥️ Investigation Environment

| Item | Value |
|------|-------|
| Case ID | CASE-02 |
| Investigation Type | PayPal Phishing Email |
| Analysis Platform | Kali Linux |
| Email Client | Mozilla Thunderbird |
| Sample | sample-1407.eml |
| Isolation | Virtual Machine |

---

# 🔍 Initial Visual Inspection

The phishing email was opened within **Mozilla Thunderbird** in an isolated virtual environment.

Immediately upon opening the message, Thunderbird displayed a warning indicating that **remote content had been blocked**. This security feature prevents external images, tracking pixels, and other remote resources from loading automatically, reducing the risk of accidental communication with attacker-controlled infrastructure.

The email impersonated **PayPal**, claiming that the recipient had won a **€1000 PayPal Gift Card** and encouraging immediate action by clicking embedded hyperlinks to claim the reward.

No file attachments were present within the message.

---

# 🚩 Initial Findings

| Observation | Result |
|-------------|--------|
| Brand Impersonation | PayPal |
| Language | German |
| Theme | Gift Card / Prize |
| Social Engineering | Reward-Based Lure |
| Urgency | High |
| Remote Content | Blocked |
| Attachments | None |
| Embedded Hyperlinks | Present |
| HTML Email | Yes |

---

# 📊 Initial Risk Assessment

The preliminary assessment identified several characteristics commonly associated with phishing campaigns.

- PayPal branding was used to establish credibility.
- The email promised a high-value monetary reward.
- Recipients were encouraged to take immediate action.
- Multiple embedded hyperlinks were present.
- Generic recipient targeting was observed.
- The message relied heavily on social engineering techniques.

Based on these observations, the email was classified as **High Risk** and escalated for comprehensive forensic analysis.

---

# 📂 Evidence Collected

The following evidence was preserved during the Initial Triage phase:

- Original phishing email (.eml)
- Email subject line
- Sender information
- Thunderbird remote content warning
- HTML email body
- Embedded hyperlinks (visual inspection)
- Raw email preview

---

# 📸 Screenshots

## Investigation Workspace

Shows the isolated Kali Linux environment used to safely investigate the phishing email.

---

## Original Email Opened

Displays the phishing email opened in Mozilla Thunderbird.

---

## Sender Information

Shows the sender address, recipient, subject line, and visible email metadata.

---

## Remote Content Protection

Illustrates Thunderbird blocking remote content to prevent communication with external resources.

---

## Email Body (Upper Section)

Displays the PayPal branding and fraudulent gift card notification.

---

## Email Body (Lower Section)

Shows the embedded call-to-action hyperlink and footer section of the phishing email.

---

## Raw Email Preview

Displays the original email content viewed from the command line prior to detailed header analysis.

---

# 💡 Analyst Notes

The investigation was conducted entirely within an isolated virtual machine to preserve evidence and prevent accidental interaction with attacker infrastructure.

During this phase:

- No hyperlinks were clicked.
- No remote content was loaded.
- No attachments were executed.
- Evidence integrity was maintained throughout the investigation.

These precautions ensured that the original evidence remained unaltered and suitable for subsequent forensic analysis.

---

# ✅ Conclusion

The initial triage confirmed multiple indicators consistent with a phishing campaign, including PayPal brand impersonation, reward-based social engineering, urgent call-to-action messaging, and embedded hyperlinks intended to encourage user interaction.

Although no technical analysis was performed during this phase, the preliminary findings justified escalation to a full forensic investigation, including detailed examination of the email headers, routing path, authentication mechanisms, embedded URLs, and associated attacker infrastructure.

---

# ➡️ Next Phase

Continue to **02-Header-Analysis.md** to analyze the SMTP headers, sender information, message routing, and email authentication records.
