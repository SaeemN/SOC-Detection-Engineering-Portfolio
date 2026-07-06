# MITRE ATT&CK Mapping

## Detection

PowerShell Execution

---

## MITRE ATT&CK Technique

| Field | Value |
|-------|-------|
| Tactic | Execution |
| Technique | Command and Scripting Interpreter: PowerShell |
| Technique ID | T1059.001 |

---

## Why It Maps to T1059.001

PowerShell is a built-in Windows command and scripting interpreter. Attackers commonly use it to execute commands, download additional payloads, perform reconnaissance, move laterally, and establish persistence.

This detection identifies the creation of the `powershell.exe` process using Windows Security Event ID 4688.

---

## Detection Logic

- Monitor Windows Security Event ID 4688 (Process Creation).
- Identify events where `New_Process_Name` contains `powershell.exe`.
- Generate an alert for analyst investigation.

---

## References

- MITRE ATT&CK Technique: T1059.001 – PowerShell
- Windows Security Event ID 4688 – Process Creation
