# 🛡️ SOC Detection Engineering Portfolio

A hands-on Detection Engineering project focused on building, testing, and documenting security detections using Splunk Enterprise in a home lab.

## 🎯 Project Goal

The objective of this project is to simulate real-world attacks, collect Windows security logs, develop Splunk detections, configure alerts, map detections to the MITRE ATT&CK framework, and document the complete investigation process.

This repository serves as a practical portfolio demonstrating SOC Analyst and Detection Engineering skills.

## 🖥️ Lab Environment

| Component | Technology |
|-----------|------------|
| Host Machine | Windows 11 Pro |
| SIEM | Splunk Enterprise 10.4.1 |
| Log Forwarder | Splunk Universal Forwarder |
| Victim Machine | Windows 10 VM |
| Attack Machine | Kali Linux VM |
| Virtualization | VMware Workstation |
| Log Source | Windows Security Event Logs |

## 🏗️ Lab Architecture

```text
                    +------------------+
                    | Kali Linux VM    |
                    | (Attack Machine) |
                    +--------+---------+
                             |
                             |
                    +--------v---------+
                    | Windows 10 VM    |
                    | (Victim Machine) |
                    | Splunk Universal |
                    | Forwarder         |
                    +--------+---------+
                             |
                             | TCP 9997
                             |
                    +--------v---------+
                    | Windows 11 Host  |
                    | Splunk Enterprise|
                    | SIEM             |
                    +------------------+
```
## 🛠️ Tools & Technologies

| Category | Technology |
|----------|------------|
| SIEM | Splunk Enterprise 10.4.1 |
| Log Collection | Splunk Universal Forwarder |
| Operating Systems | Windows 11 Pro, Windows 10, Kali Linux |
| Virtualization | VMware Workstation |
| Log Source | Windows Security Logs |
| Query Language | SPL (Search Processing Language) |
| Framework | MITRE ATT&CK |
| Version Control | Git & GitHub |

## 📋 Detection Matrix

| ID | Detection | Event ID | MITRE ATT&CK | Severity | Status |
|----|-----------|----------|--------------|----------|--------|
| D001 | PowerShell Execution | 4688 | T1059.001 | Medium | ✅ Completed |
| D002 | Encoded PowerShell | 4688 | T1059.001 | High | ⏳ Planned |
| D003 | CMD Execution | 4688 | T1059.003 | Medium | ⏳ Planned |
| D004 | Failed Logon Detection | 4625 | T1110 | Medium | ⏳ Planned |
| D005 | Successful Logon Detection | 4624 | T1078 | Low | ⏳ Planned |
| D006 | Account Lockout | 4740 | T1110 | High | ⏳ Planned |
