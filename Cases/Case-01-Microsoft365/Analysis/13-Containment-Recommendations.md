# Phase 13 – Containment Recommendations

## Objective

Provide recommended containment actions to minimize the impact of the phishing email and prevent additional users from interacting with the malicious content.

---

# Containment Summary

| Priority | Recommendation | Status |
|----------|----------------|--------|
| High | Block the phishing URL and associated domains | Recommended |
| High | Quarantine or remove the phishing email from all user mailboxes | Recommended |
| High | Block the sender email address (if applicable) | Recommended |
| High | Block identified IOCs in security solutions | Recommended |
| Medium | Reset passwords for affected users (if credentials were entered) | Conditional |
| Medium | Enable Multi-Factor Authentication (MFA) | Recommended |
| Medium | Monitor Microsoft 365 sign-in activity | Recommended |
| Low | Conduct user awareness training | Recommended |

---

# Recommended Containment Actions

## 1. Block the Phishing URL

Immediately block the following URLs within secure web gateways, DNS filtering solutions, proxy servers, and email security products.

### Indicators

```
https://is.gd/...
lolalhopb.firebaseio.com
```

This prevents users from accessing the phishing infrastructure.

---

## 2. Remove the Email

Search for the phishing email across all organizational mailboxes and:

- Quarantine the message
- Delete copies from inboxes
- Prevent further delivery through email security policies

This reduces the likelihood of additional users interacting with the phishing email.

---

## 3. Block Sender

If organizational policy permits, block the sender email address or create an email filtering rule to prevent similar phishing attempts.

Although the sender passed SPF, DKIM, and DMARC authentication, additional filtering based on sender reputation and message content is recommended.

---

## 4. Block Identified Indicators of Compromise (IOCs)

Update security controls with the identified indicators.

Examples include:

- Shortened URL
- Firebase-hosted phishing domain
- Related IP addresses (where appropriate)
- Email subject
- Sender address

Security solutions include:

- Secure Email Gateway (SEG)
- DNS filtering
- Web proxy
- Endpoint Detection and Response (EDR)
- SIEM detection rules

---

## 5. Reset User Credentials (If Required)

If any user clicked the phishing link and submitted credentials:

- Force an immediate password reset
- Revoke active Microsoft 365 sessions
- Invalidate authentication tokens
- Review recent account activity

No evidence of credential compromise was identified during this investigation; therefore, this action remains precautionary.

---

## 6. Enable Multi-Factor Authentication (MFA)

Ensure all Microsoft 365 accounts are protected with Multi-Factor Authentication.

MFA significantly reduces the likelihood of successful account compromise, even if credentials are stolen.

---

## 7. Monitor Microsoft 365 Logs

Review Microsoft 365 audit logs for:

- Failed login attempts
- Successful logins from unusual locations
- Impossible travel events
- New inbox rules
- OAuth application consent
- Suspicious account activity

Continue monitoring until confidence is established that no compromise occurred.

---

## 8. Increase User Awareness

Notify employees about the phishing campaign and remind them to:

- Verify password reset requests before acting
- Inspect URLs before clicking
- Report suspicious emails to the security team
- Avoid entering credentials on unexpected webpages

Security awareness training reduces the success rate of future phishing campaigns.

---

# Containment Priority

| Action | Priority |
|---------|----------|
| Block URLs | High |
| Remove phishing email | High |
| Block sender | High |
| Block IOCs | High |
| Reset credentials (if compromised) | Medium |
| Enable MFA | Medium |
| Review Microsoft 365 logs | Medium |
| User awareness notification | Low |

---

# Analyst Recommendation

The phishing email should be treated as an active credential harvesting attempt targeting Microsoft 365 users. Immediate containment should focus on preventing additional user interaction with the phishing email by blocking the malicious infrastructure, removing the email from all mailboxes, and monitoring for any signs of account compromise.

Although no evidence of successful credential theft was identified during the investigation, proactive containment measures should be implemented to reduce organizational risk and prevent similar phishing attempts.

---

# Conclusion

The recommended containment actions prioritize preventing further exposure to the phishing campaign while enabling rapid detection of any potential account compromise. Combining technical controls, continuous monitoring, and user awareness provides an effective defense against this type of credential phishing attack.
