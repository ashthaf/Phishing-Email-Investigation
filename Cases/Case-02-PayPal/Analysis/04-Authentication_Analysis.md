# Authentication Analysis

## Objective

The objective of this phase is to verify whether the sender successfully authenticated using standard email authentication mechanisms and to validate the sender's infrastructure using external DNS intelligence sources.

The following authentication mechanisms were analyzed:

- Authentication-Results Header
- SPF
- DKIM
- DMARC
- MX Records
- WHOIS Information

---

# Authentication Results Header

Microsoft Exchange records the outcome of all authentication checks inside the **Authentication-Results** header.

The extracted header shows:

- SPF = Pass
- DKIM = None
- DMARC = Pass
- Composite Authentication = Pass

This indicates that Microsoft successfully authenticated the sender using SPF and DMARC, while no DKIM signature was present in this particular email.

### Screenshot

![Authentication Results](../Screenshots/authentication-analysis/Authentication-Results.png)

---

# MXToolbox Verification

To validate the DNS configuration independently, MXToolbox was used to examine the sender domains.

### Screenshot

![MXToolbox Home](../Screenshots/authentication-analysis/Mxtoolbox-home.png)

---

# SPF Analysis

Sender Policy Framework (SPF) verifies whether the sending server is authorized to send emails for the sender's domain.

The Authentication-Results header contains:

```
spf=pass
```

This confirms that the sender IP address matched the domain's published SPF policy.

External verification using MXToolbox confirms:

- SPF record published
- Valid SPF syntax
- Microsoft Outlook mail servers authorized
- No deprecated SPF records

### Screenshot

![SPF Lookup](../Screenshots/authentication-analysis/Mxtoolbox-spf.png)

---

# DKIM Analysis

DomainKeys Identified Mail (DKIM) validates a cryptographic signature added by the sending domain.

The Authentication-Results header contains:

```
dkim=none
```

This indicates that the investigated email was transmitted without a DKIM signature.

MXToolbox shows that the domain currently publishes DKIM DNS records. However, the investigated email itself was not signed.

This demonstrates an important forensic distinction:

- DKIM DNS records exist.
- The investigated email did not contain a DKIM signature.

Possible reasons include:

- Selective signing
- Third-party relay
- Legacy mail configuration
- Sender configuration

### Screenshot

![DKIM Lookup](../Screenshots/authentication-analysis/Mxtoolbox-dkim.png)

---

# DMARC Analysis

DMARC combines SPF and DKIM results to determine whether an email satisfies the sender's authentication policy.

The Authentication-Results header shows:

```
dmarc=pass
```

MXToolbox confirms that the sender domain publishes a valid DMARC policy with:

- Policy = reject
- Aggregate reporting enabled
- Forensic reporting enabled
- Valid syntax

### Screenshot

![DMARC Lookup](../Screenshots/authentication-analysis/Mxtoolbox-dmarc.png)

---

# MX Record Verification

MX records determine which mail servers are responsible for accepting email for a domain.

MXToolbox confirms that **stayfriends.de** routes mail through Microsoft Exchange Online Protection.

Observed MX Host:

```
stayfriends-de.mail.protection.outlook.com
```

This matches the mail routing observed in the email headers.

### Screenshot

![MX Lookup](../Screenshots/authentication-analysis/Mxtoolbox-mx.png)

---

# WHOIS Verification

WHOIS lookups were performed to verify ownership and registration of the domains observed during the investigation.

## stayfriends.de

The primary sender domain is registered and publicly resolvable.

### Screenshot

![WHOIS StayFriends](../Screenshots/authentication-analysis/who-is-stayfriends.png)

---

## messaggerocappuccino.it

The originating SMTP domain is also registered.

Although the domain is legitimate from a registration perspective, registration alone does not establish trustworthiness.

### Screenshot

![WHOIS SMTP Domain](../Screenshots/authentication-analysis/smtp-domain-whois.png)

---

# Authentication Summary

| Authentication Mechanism | Result |
|--------------------------|--------|
| SPF | Pass |
| DKIM | None |
| DMARC | Pass |
| MX Record | Valid |
| WHOIS | Registered Domains |

---

# Analyst Assessment

Authentication analysis indicates that the email successfully passed SPF and DMARC validation, while no DKIM signature was present in the investigated message.

Independent DNS verification using MXToolbox confirmed valid SPF, DMX, MX, and DKIM DNS records for the sender's infrastructure. WHOIS lookups verified that both observed domains are registered and publicly resolvable.

Although the sender successfully passed authentication checks, authentication alone does not guarantee legitimacy. Sophisticated phishing campaigns frequently abuse legitimate infrastructure or compromised mail servers.

Further routing, infrastructure, URL, and content analysis is therefore required before determining whether the email is malicious.
