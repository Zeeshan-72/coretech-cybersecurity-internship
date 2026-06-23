# Task 10: Incident Response and Digital Forensics

## Student Information

**Name:** Zeeshan Haider  
**Course:** Information Security  
**Task:** Incident Response and Digital Forensics

---

# Project Overview

This project demonstrates the concepts of Incident Response and Digital Forensics. It includes the Incident Response Lifecycle, a ransomware incident response plan for CoreTech Innovation, digital forensics fundamentals, FTK Imager practical work, log analysis and SIEM concepts, and a post-incident report template.

---

# Objectives

- Understand the Incident Response Lifecycle.
- Develop an Incident Response Plan for a ransomware attack.
- Learn Digital Forensics fundamentals.
- Practice forensic imaging using FTK Imager.
- Understand Log Analysis and SIEM systems.
- Create a Post-Incident Report Template.

---

# Incident Response Lifecycle

The Incident Response Lifecycle consists of six phases:

## 1. Preparation
Preparation involves creating policies, procedures, backups, and training employees before incidents occur.

## 2. Detection and Analysis
Identify suspicious activities, investigate alerts, and determine whether a security incident has occurred.

## 3. Containment
Limit the spread of the attack by isolating affected systems and preventing further damage.

## 4. Eradication
Remove malware, patch vulnerabilities, and eliminate the root cause of the incident.

## 5. Recovery
Restore systems and services from backups and return them to normal operation.

## 6. Lessons Learned
Review the incident, document findings, and improve future response capabilities.

---

# CoreTech Innovation Ransomware Response Plan

## Scenario
CoreTech Innovation experiences a ransomware attack that encrypts company files and demands payment.

## Identification
- Detect encrypted files.
- Identify affected systems.
- Confirm ransomware infection.

## Containment
- Disconnect infected devices from the network.
- Disable shared drives.
- Block malicious communications.

## Eradication
- Remove ransomware.
- Patch exploited vulnerabilities.
- Change compromised passwords.

## Recovery
- Restore data from backups.
- Verify system integrity.
- Monitor systems for reinfection.

## Lessons Learned
- Review the attack.
- Improve employee awareness.
- Strengthen security controls.

---

# Digital Forensics Basics

## Evidence Collection
Evidence collection involves gathering digital evidence such as:

- Hard Drives
- USB Devices
- Emails
- Log Files
- Memory Dumps

## Chain of Custody
Chain of custody is a documented record showing who collected, handled, transferred, and analyzed evidence.

### Importance
- Maintains evidence integrity.
- Ensures legal admissibility.
- Prevents evidence tampering.

## Disk Imaging
Disk imaging is the process of creating an exact bit-by-bit copy of digital evidence.

### Benefits
- Preserves original evidence.
- Enables safe analysis.
- Maintains integrity through hash verification.

---

# FTK Imager Practical

## Tool Used

**Exterro FTK Imager 8.20**

## Objective

To create a forensic image of sample evidence and verify its integrity.

## Sample Evidence

The following files were created inside an Evidence folder:

- secret.txt
- passwords.txt
- notes.txt

## Procedure

1. Installed FTK Imager.
2. Created a sample Evidence folder.
3. Selected "Contents of a Folder" as evidence source.
4. Chose E01/AD1 forensic image format.
5. Entered case information.
6. Selected destination folder.
7. Created forensic image.
8. Verified image integrity.

## Verification Results

### MD5 Hash

Verification Result: **Match**

### SHA1 Hash

Verification Result: **Match**

## Conclusion

The forensic image was successfully created and verified. The verification results confirmed that the image was an exact copy of the original evidence and had not been altered.

---

# Log Analysis

Log analysis is the process of reviewing logs to detect suspicious activities and security incidents.

## Common Log Sources

- Windows Event Logs
- Firewall Logs
- Web Server Logs
- Application Logs
- Authentication Logs

## Benefits

- Detect attacks
- Monitor user activity
- Investigate incidents
- Improve security

---

# SIEM (Security Information and Event Management)

SIEM systems collect, correlate, and analyze security events from multiple sources.

## Functions

- Log Collection
- Event Correlation
- Real-Time Monitoring
- Alert Generation
- Incident Investigation

## Popular SIEM Tools

- Splunk
- IBM QRadar
- Microsoft Sentinel
- Elastic Security

## Benefits

- Centralized monitoring
- Faster incident detection
- Improved security visibility
- Better compliance reporting

---

# Post-Incident Report Template

The repository also contains a reusable post-incident report template including:

- Incident Information
- Incident Summary
- Timeline
- Impact Assessment
- Root Cause Analysis
- Actions Taken
- Lessons Learned
- Recommendations

---

# Screenshots

The screenshots folder contains evidence of practical work performed using FTK Imager.

## Included Screenshots

- FTK Imager Home Screen
- Source Selection
- Case Information
- Destination Configuration
- Imaging Process
- Image Verification Results

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
    ├── case_info.png
    ├── destination_added.png
    ├── imaging_process.png
    └── imaging_complete.png
```

---

# Conclusion

This project successfully demonstrated Incident Response and Digital Forensics concepts through theoretical explanations and practical forensic imaging using FTK Imager. The generated forensic image was successfully verified using hash values, ensuring evidence integrity and authenticity.

---
