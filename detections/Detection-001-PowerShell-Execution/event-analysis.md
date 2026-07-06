# Event Analysis

## Windows Security Event

| Field | Value |
|--------|-------|
| Event ID | 4688 |
| Event Name | Process Creation |
| Log Source | Windows Security Log |
| MITRE ATT&CK | T1059.001 - PowerShell |

---

## Important Fields

| Field | Purpose |
|--------|----------|
| EventCode | Identifies the Windows event (4688 = Process Creation). |
| New_Process_Name | The executable that started (e.g., powershell.exe). |
| Creator_Process_Name | The process that launched the new process. |
| Account_Name | The user who started the process. |
| ComputerName | The endpoint where the event occurred. |
| _time | Time when the event was generated. |

---

## Sample Event

New_Process_Name:
C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe

Creator_Process_Name:
C:\Windows\System32\cmd.exe

Account_Name:
Victim Windows 10

EventCode:
4688

---

## Why This Event Matters

Event ID 4688 records every new process created on a Windows system.

By monitoring process creation events, defenders can identify suspicious programs such as:

- PowerShell
- CMD
- Certutil
- WMI
- Rundll32
- Mshta
- Regsvr32

Many attacker techniques begin with the execution of a process, making Event ID 4688 one of the most valuable Windows Security events for detection engineering.
