# Task 10: Incident Response and Digital Forensics

## Student Information

**Name:** Zeeshan Haider  
**Course:** Information Security

---

# Introduction

This project demonstrates the concepts of Incident Response and Digital Forensics. It covers the Incident Response Lifecycle, a ransomware incident response plan, digital forensics fundamentals, forensic imaging using FTK Imager, log analysis, SIEM concepts, and a post-incident report template.

---

# Incident Response Lifecycle

## 1. Preparation

Preparation involves creating policies, procedures, backups, and security awareness training before an incident occurs.

## 2. Detection and Analysis

Identify suspicious activities and determine whether a security incident has occurred.

## 3. Containment

Limit the spread of the attack by isolating affected systems.

## 4. Eradication

Remove malware and eliminate the root cause of the incident.

## 5. Recovery

Restore systems and services from backups.

## 6. Lessons Learned

Review the incident and improve future security measures.

---

# CoreTech Innovation Ransomware Response Plan

## Scenario

CoreTech Innovation experiences a ransomware attack that encrypts company files and demands payment.

### Identification

- Detect encrypted files
- Identify affected systems
- Confirm ransomware infection

### Containment

- Disconnect infected devices
- Disable network shares
- Block malicious communications

### Eradication

- Remove ransomware
- Patch vulnerabilities
- Reset compromised credentials

### Recovery

- Restore data from backups
- Verify system integrity
- Resume normal operations

### Lessons Learned

- Conduct incident review
- Update policies
- Improve employee training

---

# Digital Forensics Basics

## Evidence Collection

Digital evidence may include:

- Hard Drives
- USB Devices
- Log Files
- Emails
- Memory Dumps

## Chain of Custody

Chain of custody records every individual who handled the evidence.

### Importance

- Maintains evidence integrity
- Prevents tampering
- Supports legal investigations

## Disk Imaging

Disk imaging creates an exact copy of digital evidence for analysis.

### Benefits

- Preserves original evidence
- Enables safe analysis
- Verifies integrity using hashes

---

# FTK Imager Practical

## Objective

To create a forensic image from sample evidence and verify its integrity.

## Sample Evidence Files

- secret.txt
- passwords.txt
- notes.txt

---

# FTK Imager Home Screen

The following screenshot shows FTK Imager after successful installation.

![FTK Home](screenshots/ftk_home.png)

---

# Source Selection

The evidence source was selected using the "Contents of a Folder" option.

![Source Selection](screenshots/source_selection.png)

---

# Destination Configuration

The forensic image destination was configured successfully.

![Destination Added](screenshots/destination_added.png)

---

# Imaging Process

FTK Imager successfully created a forensic image of the evidence folder.

![Imaging Process](screenshots/imaging_process.png)

---

# Verification Results

The generated forensic image was verified using MD5 and SHA1 hashes.

Verification Result: **Match**

![Verification Results](screenshots/imaging_complete.png)

---

# Log Analysis

Log analysis is the process of reviewing system logs to identify suspicious activity.

## Common Log Sources

- Windows Event Logs
- Firewall Logs
- Web Server Logs
- Authentication Logs
- Application Logs

### Benefits

- Detect security incidents
- Monitor user activity
- Investigate attacks
- Improve security visibility

---

# SIEM (Security Information and Event Management)

SIEM systems collect and analyze security events from multiple sources.

## Functions

- Log Collection
- Event Correlation
- Alert Generation
- Incident Investigation
- Compliance Reporting

## Popular SIEM Tools

- Splunk
- IBM QRadar
- Microsoft Sentinel
- Elastic Security

### Benefits

- Centralized monitoring
- Faster incident response
- Improved visibility
- Better compliance management

---

# Post-Incident Report Template

The project includes a reusable post-incident report template containing:

- Incident Information
- Timeline
- Impact Assessment
- Root Cause Analysis
- Actions Taken
- Lessons Learned
- Recommendations

---

# Repository Structure

```text
Task10-Incident-Response-Forensics
│
├── README.md
├── Incident_Response_Lifecycle.md
├── CoreTech_Ransomware_Response_Plan.md
├── Digital_Forensics_Basics.md
├── FTK_Imager_Practice.md
├── Log_Analysis_and_SIEM.md
├── Post_Incident_Report_Template.md
│
└── screenshots
    ├── ftk_home.png
    ├── source_selection.png
    ├── destination_added.png
    ├── imaging_process.png
    └── imaging_complete.png
```

---

# Conclusion

This project successfully demonstrated Incident Response and Digital Forensics concepts through both theoretical explanations and practical forensic imaging using FTK Imager. The generated forensic image was successfully verified using MD5 and SHA1 hash values, confirming evidence integrity and authenticity.

---
