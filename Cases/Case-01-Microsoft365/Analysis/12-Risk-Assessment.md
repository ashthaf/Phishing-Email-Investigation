# Phase 12 – Risk Assessment

## Objective

Assess the overall risk posed by the phishing email based on the findings from previous investigation phases, including header analysis, authentication results, sender analysis, content analysis, URL analysis, attachment analysis, IOC extraction, threat intelligence, and MITRE ATT&CK mapping.

---

# Risk Assessment Summary

| Category | Assessment |
|----------|------------|
| Threat Type | Credential Phishing |
| Likelihood | High |
| Current Impact | Low |
| Potential Impact | High |
| Severity | High |
| Overall Risk | High |

---

# Threat Type

The investigated email is classified as a **Credential Phishing** attack.

The attacker impersonated Microsoft 365 and attempted to trick the recipient into clicking a password reset link that redirected to a credential harvesting page hosted on Firebase.

No malware or malicious attachments were observed during the investigation.

---

# Likelihood Assessment

**Likelihood: High**

### Justification

The attack demonstrates several characteristics commonly associated with successful phishing campaigns:

- Microsoft 365 branding was used to build trust.
- Password reset theme created urgency.
- URL shortening service (is.gd) concealed the destination.
- Phishing page was hosted on Google Firebase, a trusted cloud platform.
- SPF, DKIM, and DMARC authentication passed, making the email appear legitimate.
- The attack required only a single user click to proceed.

These factors significantly increase the probability of a successful compromise if the recipient is not cautious.

---

# Impact Assessment

## Current Impact

**Low**

During this investigation:

- No evidence of credential submission was identified.
- No malware execution occurred.
- No malicious attachment was delivered.
- No confirmed account compromise was observed.

---

## Potential Impact

**High**

If a user entered their Microsoft 365 credentials, the attacker could potentially:

- Compromise the victim's Microsoft 365 account
- Access sensitive emails and documents
- Launch additional phishing emails from the compromised account
- Perform unauthorized access to cloud resources
- Conduct Business Email Compromise (BEC)
- Steal confidential organizational data

---

# Severity Assessment

**Severity: High**

Although no successful compromise was confirmed, the phishing email demonstrated a high level of sophistication by:

- Impersonating Microsoft 365
- Using legitimate cloud infrastructure (Firebase)
- Leveraging a URL shortener to conceal the destination
- Applying social engineering techniques to encourage immediate action

The absence of confirmed credential theft prevents this incident from being classified as Critical.

---

# Overall Risk Rating

## High

The incident presents a **High** organizational risk because:

- The phishing email is convincing.
- Trusted infrastructure was abused.
- The attack targets Microsoft 365 credentials.
- Successful exploitation could lead to significant account compromise and data exposure.

At the time of analysis, no evidence indicated that the phishing attempt was successful; therefore, the overall risk is assessed as **High** rather than **Critical**.

---

# Risk Matrix

| Likelihood | Impact | Overall Risk |
|------------|--------|--------------|
| High | High (Potential) | High |

---

# Analyst Assessment

The investigation determined that this email is a credential phishing campaign targeting Microsoft 365 users. The attacker used a shortened URL that redirected to a phishing page hosted on Firebase, leveraging trusted cloud infrastructure to increase credibility and reduce suspicion.

Email authentication mechanisms (SPF, DKIM, and DMARC) were successfully validated, demonstrating that authentication alone is insufficient to identify sophisticated phishing attempts.

Although no evidence of credential compromise or malware execution was found, the potential impact of a successful attack would be significant. Based on the observed attack techniques and potential business consequences, the incident is classified as **High Risk**.

---

# Conclusion

The phishing email represents a high-risk social engineering attack aimed at stealing Microsoft 365 credentials. While no successful compromise was identified during the investigation, the use of trusted cloud services, URL shortening, and Microsoft impersonation significantly increased the likelihood of user deception.

Continuous user awareness training, enhanced email security controls, and proactive monitoring are recommended to reduce the risk of similar phishing campaigns in the future.
