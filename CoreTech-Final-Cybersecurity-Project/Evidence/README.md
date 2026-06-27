# 🔎 Evidence Collection

---

# Overview

This folder contains the evidence collected during the cybersecurity assessment of the CoreTech Innovation web application.

The evidence supports the findings documented in the final report and demonstrates that the assessment was conducted using ethical and non-intrusive testing techniques.

---

# Evidence Summary

The following evidence was collected during the assessment:

| Evidence | Description |
|-----------|-------------|
| OWASP Testing Guide | Security testing methodology used during assessment |
| Security Testing Process | Workflow followed throughout the assessment |
| Security Headers Report | HTTP Security Header analysis results |
| Risk Assessment | Severity classification of findings |
| Final Report | Complete documentation of the assessment |

---

# Evidence 1 – OWASP Testing Methodology

## Description

The OWASP Web Security Testing Guide (WSTG) served as the primary methodology for planning and performing the assessment.

The methodology provides standardized guidance for identifying common web application security weaknesses.

---

## Screenshot

The screenshot is available in the **Screenshots** folder.

```
Screenshots/Owasp Testing.png
```

---

# Evidence 2 – Security Testing Process

## Description

The following workflow was followed during testing:

1. Information Gathering
2. Reconnaissance
3. Security Header Analysis
4. SSL/TLS Review
5. Vulnerability Identification
6. Risk Assessment
7. Documentation

---

## Screenshot

```
Screenshots/Testing Process.png
```

---

# Evidence 3 – Security Header Analysis

## Description

The HTTP response headers were analyzed to determine whether the application follows current web security best practices.

The analysis identified several implemented headers as well as missing headers that should be configured.

---

## Observations

### Implemented

- HTTPS
- Strict-Transport-Security
- Permissions-Policy
- X-Frame-Options

### Missing

- Content-Security-Policy
- Referrer-Policy
- X-Content-Type-Options

---

## Screenshot

```
Screenshots/Findings.png
```

---

# Risk Summary

| Finding | Risk |
|----------|------|
| Missing Content Security Policy | Medium |
| Missing Referrer Policy | Low |
| Missing X-Content-Type-Options | Low |

Overall Risk Rating:

**Medium**

---

# Integrity of Evidence

The evidence presented in this repository was collected using publicly accessible information and non-destructive assessment techniques.

No unauthorized access was attempted, and no confidential information was obtained.

---

# Conclusion

The collected evidence supports the findings presented in the cybersecurity assessment report.

The screenshots and observations demonstrate that the assessment followed recognized security testing methodologies and identified practical recommendations for improving the application's security posture.

---

# Prepared By

**Zeeshan Haider**

CoreTech Final Cybersecurity Project

Cybersecurity Internship

2026
