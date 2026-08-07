# 🌐 Phase 03 – Routing Analysis

![Status](https://img.shields.io/badge/Status-Completed-44CC11)
![Phase](https://img.shields.io/badge/Phase-03-blue)
![Category](https://img.shields.io/badge/Category-Routing%20Analysis-red)
![Case](https://img.shields.io/badge/Case-02-blue)
![Evidence](https://img.shields.io/badge/Evidence-Received%20Headers-orange)

---

# 📖 Overview

The purpose of this phase was to reconstruct the delivery path of the phishing email by analyzing the SMTP **Received** headers. Each mail server that processes an email appends its own **Received** header, enabling investigators to trace the route taken from the originating server to the recipient's mailbox.

Routing analysis helps identify the email's origin, intermediate relay servers, and final delivery destination while detecting any unusual or unauthorized routing behavior.

---

# 🎯 Objectives

The objectives of this phase were to:

- Identify the originating mail server.
- Reconstruct the complete email delivery path.
- Identify intermediate mail relays.
- Verify the final delivery server.
- Detect any suspicious or unexpected routing behavior.

---

# 📂 Extracting Received Headers

To isolate the routing information, only the **Received** headers were extracted from the email header.

```bash
grep "^Received:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt \
> ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/Received-header.txt
```

The extracted routing headers were then reviewed for further analysis.

### Screenshot

![Received Headers](../Screenshots/routing-analysis/received-chain.png)

---

# 📊 Counting Mail Hops

The total number of routing hops was determined by counting the **Received** headers.

```bash
grep -c "^Received:" ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/email-header.txt
```

The email traversed **4 routing hops** before reaching the recipient's mailbox.

### Screenshot

![Received Header Count](../Screenshots/routing-analysis/Received-header-count.png)

---

# 🔢 Numbering Routing Hops

Each routing hop was numbered to simplify the reconstruction of the delivery path.

```bash
nl -ba ~/CyberLab/Cases/Case-02-paypal/Evidence/Headers/Received-header.txt
```

### Screenshot

![Routing Hop Numbering](../Screenshots/routing-analysis/Received-hop-numbering.png)

---

# 📨 Mail Flow Reconstruction

Email routing must always be interpreted **from the bottom Received header to the top**, as each receiving mail server appends its own entry during message delivery.

The reconstructed mail flow is shown below.

| Hop | Source Server | Destination | Observation |
|-----|---------------|-------------|-------------|
| 1 | messaggerocappuccino.it (77.91.100.118) | Microsoft Exchange Online Frontend | Originating mail server |
| 2 | DU2PEPF0001E9C1.eurprd03.prod.outlook.com | Microsoft Exchange Online | Internal Microsoft relay |
| 3 | DU2PR04CA0228.eurprd04.prod.outlook.com | Microsoft SMTP | Internal Microsoft transport |
| 4 | SJ0PR19MB5383.namprd19.prod.outlook.com | Recipient Mailbox | Final mailbox delivery |

---

# 🔍 Routing Observations

The routing analysis revealed the following:

- The email originated from **messaggerocappuccino.it** (`77.91.100.118`).
- After being accepted by Microsoft Exchange Online, the message remained entirely within Microsoft's internal mail infrastructure.
- Multiple Exchange Online transport servers processed the email before final delivery.
- No unauthorized third-party relay servers were identified.
- The routing sequence appears consistent with standard Microsoft Exchange Online mail processing.

---

# 📈 Key Findings

| Finding | Result |
|----------|--------|
| Total Routing Hops | 4 |
| Originating Server | messaggerocappuccino.it |
| Originating IP | 77.91.100.118 |
| Microsoft Relay Servers | Multiple |
| Unknown Third-Party Relays | None Identified |
| Final Destination | Recipient Mailbox |

---

# 💡 Analyst Notes

The routing headers provide a clear record of the email's delivery path.

Although the message ultimately traversed legitimate Microsoft Exchange Online infrastructure, the originating server (**messaggerocappuccino.it**) represents the initial point of transmission and becomes an important Indicator of Compromise (IOC) for subsequent threat intelligence analysis.

No evidence of relay manipulation or unauthorized mail forwarding was identified during this phase.

---

# ✅ Conclusion

The routing analysis successfully reconstructed the complete delivery path of the phishing email.

The investigation confirmed that the email originated from **messaggerocappuccino.it** before entering Microsoft Exchange Online infrastructure. Once accepted, the message followed a normal sequence of internal Microsoft transport servers until final delivery to the recipient's mailbox.

The reconstructed routing path provides valuable evidence for identifying the attacker's sending infrastructure and supports the subsequent phases of sender analysis, threat intelligence, and IOC extraction.

---

# ➡️ Next Phase

Continue to **Phase 04 – Authentication Analysis** to verify the email's SPF, DKIM, and DMARC authentication results and assess the legitimacy of the sending infrastructure.
