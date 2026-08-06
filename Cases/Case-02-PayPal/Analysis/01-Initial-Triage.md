# Phase 01 – Initial Triage

## Objective

The objective of the Initial Triage phase was to perform a safe preliminary assessment of the suspicious email while preserving the original evidence. No interaction with embedded links, remote content, or external resources was performed during this stage.

The email was reviewed inside an isolated Kali Linux virtual machine using Mozilla Thunderbird to identify visible phishing characteristics before proceeding to detailed forensic analysis.

---

# Investigation Environment

| Item | Value |
|------|-------|
| Case ID | CASE-02 |
| Investigation Type | PayPal Phishing Email |
| Analysis Platform | Kali Linux |
| Email Client | Mozilla Thunderbird |
| Sample | sample-1407.eml |
| Isolation | Virtual Machine |

---

# Initial Visual Inspection

The phishing email was opened inside Mozilla Thunderbird.

Immediately after opening the message, Thunderbird displayed a warning indicating that **remote content had been blocked**. This prevents external images or tracking resources from loading automatically and is an important security feature when investigating suspicious emails.

The email impersonates **PayPal** by claiming that the recipient has won a **€1000 PayPal Gift Card** and urges the user to claim the reward by clicking embedded hyperlinks.

No attachments were observed during the initial inspection.

---

# Initial Findings

| Observation | Result |
|------------|--------|
| Brand Impersonation | PayPal |
| Language | German |
| Theme | Gift Card / Prize |
| Social Engineering | Reward Based |
| Urgency | High |
| Remote Content | Blocked |
| Attachments | None |
| Embedded Hyperlinks | Present |
| HTML Email | Yes |

---

# Initial Risk Assessment

Several phishing indicators were identified during the visual inspection.

- Uses PayPal branding without verification.
- Promises a high-value monetary reward.
- Encourages immediate user interaction.
- Contains embedded hyperlinks.
- Uses generic recipient information.
- Relies on social engineering rather than technical exploitation.

Based on these observations, the email was classified as **High Risk** and advanced to detailed forensic analysis.

---

# Evidence Collected

The following evidence was documented during the Initial Triage phase.

- Original phishing email
- Email subject
- Sender information
- Remote content warning
- Email body
- Embedded hyperlinks (visual)
- Raw email preview

---

# Screenshots

## Investigation Workspace

Shows the isolated Kali Linux investigation environment with Thunderbird used to safely examine the phishing email.

![Investigation Workspace](../../Assets/Screenshots/Case-02/investigation-workstation.png)

---

## Original Email Opened

The phishing email opened inside Mozilla Thunderbird for visual inspection.

![Original Email](../../Assets/Screenshots/Case-02/email-opened.png)

---

## Sender Information

Displays the sender address, recipient, subject line, and email metadata visible in Thunderbird.

![Sender Information](../../Assets/Screenshots/Case-02/email-sender-info.png)

---

## Remote Content Protection

Thunderbird automatically blocked external content, preventing remote resources from loading during analysis.

![Remote Content Warning](../../Assets/Screenshots/Case-02/remote-content-warning.png)

---

## Email Body (Upper Section)

Shows the beginning of the phishing email, including the PayPal branding and fraudulent reward notification.

![Email Body Top](../../Assets/Screenshots/Case-02/email-body-top.png)

---

## Email Body (Lower Section)

Displays the embedded call-to-action link and unsubscribe section found near the end of the email.

![Email Body Bottom](../../Assets/Screenshots/Case-02/email-body-bottom.png)

---

## Raw Email Preview

Initial examination of the original email headers and message content from the command line before performing detailed header analysis.

![Raw Email](../../Assets/Screenshots/Case-02/email-raw.png)

---

# Analyst Notes

The email was examined in a controlled virtual environment.

No hyperlinks were clicked.

No remote content was loaded.

No attachments were executed.

Evidence integrity was maintained throughout the initial assessment.

---

# Conclusion

The initial triage confirmed that the message exhibits multiple characteristics commonly associated with phishing campaigns, including PayPal brand impersonation, reward-based social engineering, and embedded hyperlinks designed to encourage user interaction.

The findings from this phase justified proceeding with detailed technical analysis of the email headers, routing information, authentication mechanisms, embedded URLs, and associated infrastructure in the subsequent phases of the investigation.
