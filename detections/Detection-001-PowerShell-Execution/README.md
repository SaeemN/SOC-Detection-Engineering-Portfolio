# Detection-001: PowerShell Execution

## Objective

Detect the execution of PowerShell on Windows endpoints using Windows Security Event ID 4688 (Process Creation).

PowerShell is a legitimate administrative tool that is also widely abused by attackers for executing malicious commands, downloading payloads, performing reconnaissance, and establishing persistence. This detection provides visibility into PowerShell process execution and serves as a foundational detection for identifying suspicious PowerShell activity.

**Detection Status:** ✅ Completed
