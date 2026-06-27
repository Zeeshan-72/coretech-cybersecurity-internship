# Security Findings

## Overview

The security assessment was performed against the CoreTech Innovation website using the OWASP Web Security Testing Methodology. The objective of the assessment was to identify common security weaknesses, evaluate their impact, and recommend appropriate mitigation strategies.

The assessment focused on HTTP security headers, transport security, browser protections, and overall website configuration.

---

# Summary of Findings

| ID | Finding | Severity | Status |
|----|----------|----------|--------|
| F-01 | Missing Content Security Policy (CSP) | High | Open |
| F-02 | Missing X-Content-Type-Options Header | Medium | Open |
| F-03 | Missing Referrer-Policy Header | Medium | Open |
| F-04 | HTTP Strict Transport Security Enabled | Low | Passed |
| F-05 | X-Frame-Options Configured | Low | Passed |
| F-06 | Permissions Policy Configured | Low | Passed |

---

# Finding F-01

## Missing Content Security Policy (CSP)

### Severity

**High**

### Description

The website does not implement the **Content-Security-Policy (CSP)** HTTP response header.

Content Security Policy helps protect web applications from attacks such as:

- Cross-Site Scripting (XSS)
- Code Injection
- Malicious JavaScript execution
- Data Injection attacks

Without CSP, browsers execute any script delivered to users, increasing the risk of client-side attacks.

---

### Risk

An attacker may inject malicious JavaScript into a vulnerable page.

This can lead to:

- Session Hijacking
- Cookie Theft
- User Impersonation
- Malware Delivery

---

### Evidence

The HTTP Security Header Scanner reported:

❌ Content-Security-Policy : Missing

See screenshot below.

![Finding 1](../Screenshots/Findings.png)

---

### Recommendation

Configure the following HTTP response header:

```
Content-Security-Policy:
default-src 'self';
script-src 'self';
style-src 'self';
img-src 'self';
```

Only allow trusted resources to execute.

---

# Finding F-02

## Missing X-Content-Type-Options Header

### Severity

**Medium**

### Description

The application does not include the following header:

```
X-Content-Type-Options: nosniff
```

Without this protection, browsers may perform MIME type sniffing and incorrectly interpret uploaded files.

---

### Risk

Possible consequences include:

- Execution of malicious files
- Browser content sniffing
- Increased attack surface

---

### Evidence

HTTP Header Scan Result

❌ X-Content-Type-Options : Missing

---

### Recommendation

Configure:

```
X-Content-Type-Options: nosniff
```

This instructs browsers not to guess file types.

---

# Finding F-03

## Missing Referrer Policy

### Severity

**Medium**

### Description

The website does not specify a Referrer-Policy header.

This header controls how much referral information is shared when users navigate between websites.

---

### Risk

Missing Referrer Policy may expose:

- Internal URLs
- Sensitive query parameters
- User navigation history

---

### Evidence

Scanner Result

❌ Referrer-Policy : Missing

---

### Recommendation

Configure one of the following:

```
Referrer-Policy: strict-origin
```

or

```
Referrer-Policy: no-referrer
```

---

# Finding F-04

## HTTP Strict Transport Security

### Severity

**Low**

### Status

Passed

### Description

The website correctly enables HTTP Strict Transport Security (HSTS).

This ensures browsers always communicate over HTTPS.

---

### Evidence

✔ Strict-Transport-Security detected.

---

### Security Benefit

- Prevents SSL stripping attacks
- Forces encrypted communication
- Improves browser security

---

# Finding F-05

## X-Frame-Options

### Severity

**Low**

### Status

Passed

### Description

The website implements the X-Frame-Options header.

This protects users from Clickjacking attacks.

---

### Evidence

✔ X-Frame-Options detected.

---

### Security Benefit

Protects web pages from being embedded inside malicious websites.

---

# Finding F-06

## Permissions Policy

### Severity

**Low**

### Status

Passed

### Description

The Permissions Policy header is properly configured.

This controls browser access to sensitive features.

Examples include:

- Camera
- Microphone
- Geolocation
- USB
- Payment API

---

### Evidence

✔ Permissions-Policy detected.

---

### Security Benefit

Reduces unnecessary browser permissions and improves user privacy.

---

# Findings Statistics

| Severity | Count |
|-----------|------:|
| Critical | 0 |
| High | 1 |
| Medium | 2 |
| Low | 3 |
| Informational | 0 |

---

# Overall Assessment

The website demonstrates a reasonable baseline security posture by enabling HTTPS and implementing several important security headers.

However, several recommended HTTP response headers remain absent. These missing protections increase the application's exposure to browser-based attacks such as Cross-Site Scripting (XSS), MIME type sniffing, and information disclosure.

The identified issues are configuration-related rather than implementation flaws and can be remediated through secure web server configuration without requiring significant application changes.

Overall Security Rating:

**Medium Risk**

The website is suitable for production use but should implement the recommended security headers to improve compliance with OWASP security best practices.
