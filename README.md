# Splunk Detection Engineering and Threat Hunting Lab

![Windows Authentication Dashboard](SCREENSHOTS/Figure21_Authentication_Dashboard.png)
![Splunk](https://img.shields.io/badge/SIEM-Splunk%20Enterprise-blue)
![Windows](https://img.shields.io/badge/Platform-Windows%2011-0078D4)
![PowerShell](https://img.shields.io/badge/Logging-PowerShell-5391FE)
![MITRE ATT&CK](https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-red)

## Overview

This project demonstrates the deployment, configuration, and operational use of **Splunk Enterprise 10.4** as a Security Information and Event Management (SIEM) platform for detection engineering and threat hunting.

A Windows 11 endpoint was configured to forward Security, System, Application, and PowerShell Operational event logs into Splunk. Custom SPL detections were developed, validated, and organized into dashboards that simulate common Security Operations Center (SOC) monitoring workflows.

---

## Project Objectives

- Deploy and configure Splunk Enterprise 10.4
- Configure Windows Event Log collection
- Enable PowerShell Script Block Logging
- Develop custom SPL detection queries
- Validate security detections using Windows Event IDs
- Create SOC-focused dashboards
- Perform threat hunting using PowerShell telemetry

---

## Lab Environment

| Component | Technology |
|------------|------------|
| SIEM | Splunk Enterprise 10.4 |
| Operating System | Windows 11 Pro |
| Detection Language | SPL (Search Processing Language) |
| Log Sources | Security, System, Application |
| Additional Logs | Microsoft-Windows-PowerShell/Operational |
| Index | security_lab |

---

## Detection Engineering

The following Windows security events were successfully ingested and validated within Splunk.

| Event ID | Detection |
|----------|-----------|
| **4625** | Failed Logon Detection |
| **4624** | Successful Logon Detection |
| **4720** | New User Account Creation |
| **4104** | PowerShell Script Block Logging |

Each detection has been included as an individual SPL query within the **SPL** directory.

---

## Dashboard Development

Three dashboards were developed to improve analyst visibility into Windows security events.

- Windows Authentication Activity Dashboard
- Account Management Activity Dashboard
- PowerShell Threat Hunting Dashboard

These dashboards provide centralized visibility into authentication activity, account management events, and PowerShell execution telemetry.

---

## Threat Hunting

PowerShell Script Block Logging (Event ID 4104) was enabled through Group Policy and ingested into Splunk.

Threat hunting activities included:

- Verifying PowerShell Operational log collection
- Configuring `inputs.conf`
- Restarting Splunk services
- Validating log ingestion using `btool`
- Developing SPL searches for PowerShell execution activity

---

## MITRE ATT&CK Mapping

| Detection | ATT&CK Technique |
|-----------|------------------|
| Failed Logons | T1110 – Brute Force |
| PowerShell Execution | T1059.001 – PowerShell |
| Create Account | T1136 – Create Account |

---

## Skills Demonstrated

- SIEM Administration
- Detection Engineering
- Threat Hunting
- Windows Event Analysis
- SPL Query Development
- Dashboard Development
- Security Monitoring
- Windows Logging
- PowerShell Logging
- SOC Operations

---

## Repository Structure

```
splunk-detection-engineering-threat-hunting-lab/
│
├── REPORT/
│   └── Splunk_Detection_Engineering_and_Threat_Hunting_Lab.pdf
│
├── SCREENSHOTS/
│   └── Project Figures
│
├── SPL/
│   ├── eventid_4624_detection.spl
│   ├── eventid_4625_detection.spl
│   ├── eventid_4720_detection.spl
│   └── eventid_4104_detection.spl
│
└── README.md
```

---

## Documentation

The complete technical report is available in the **REPORT** folder and documents:

- Splunk deployment
- Windows log ingestion
- Detection engineering
- PowerShell logging configuration
- Threat hunting
- Dashboard development
- Findings and lessons learned

---

## Key Takeaways

This project demonstrates practical SOC analyst skills through the deployment of a SIEM platform, development of custom detections, PowerShell threat hunting, and creation of security monitoring dashboards. It reflects many of the responsibilities performed by security analysts responsible for monitoring, detection engineering, and incident investigation within enterprise environments.

---

## Author

**Eric Johnson**

- GitHub: https://github.com/ericjohnson4
- CompTIA Security+
- CompTIA CySA+
- M.S. Cybersecurity (In Progress)

---
