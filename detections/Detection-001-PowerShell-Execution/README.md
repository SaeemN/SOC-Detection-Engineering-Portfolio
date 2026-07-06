# Detection-001: PowerShell Execution

## Detection Summary

| Field | Value |
|-------|-------|
| Detection ID | D001 |
| Detection Name | PowerShell Execution |
| Platform | Windows |
| Data Source | Windows Security Event Log |
| Event ID | 4688 |
| MITRE ATT&CK | T1059.001 – PowerShell |
| Severity | Medium |
| Status | ✅ Completed |

---

## Objective

Detect the execution of PowerShell on Windows endpoints using Windows Security Event ID 4688 (Process Creation).

PowerShell is a legitimate administrative tool that is also widely abused by attackers for executing malicious commands, downloading payloads, performing reconnaissance, and establishing persistence.

---

## Detection Components

| Document | Description |
|----------|-------------|
| attack-simulation.md | Steps used to generate the event |
| event-analysis.md | Analysis of Windows Event ID 4688 |
| splunk-query.spl | Splunk detection query |
| mitre-mapping.md | MITRE ATT&CK mapping |
| alert-configuration.md | Splunk alert configuration |
| investigation-guide.md | SOC investigation process |
| false-positives.md | Common false positives and tuning recommendations |

---

## Detection Workflow

Attack Simulation

↓

Windows Event ID 4688 Generated

↓

Splunk Universal Forwarder

↓

Splunk Enterprise

↓

Detection Query

↓

Alert Triggered

↓

SOC Investigation
