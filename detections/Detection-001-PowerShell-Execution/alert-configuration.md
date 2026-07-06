# Alert Configuration

## Alert Details

| Setting | Value |
|---------|-------|
| Alert Name | Detection-001 - PowerShell Execution |
| Alert Type | Scheduled |
| Schedule | Every Minute |
| Time Range | Last 1 Minute |
| Trigger Condition | Number of Results > 0 |
| Trigger Mode | Once |
| Severity | Medium |

---

## SPL Query

```spl
index=windows_logs EventCode=4688
| search New_Process_Name="*powershell.exe"
| table _time ComputerName Account_Name Creator_Process_Name New_Process_Name
| sort - _time
```

---

## Why These Settings?

### Scheduled Alert

The search runs every minute to identify newly created PowerShell processes without requiring a real-time search.

### Last 1 Minute

Only the most recent events are evaluated, reducing duplicate processing and ensuring timely detection.

### Trigger Condition

The alert triggers whenever one or more matching events are found.

### Severity

The severity is set to **Medium** because PowerShell is a legitimate administrative tool. While its execution is not inherently malicious, it is frequently abused by attackers and warrants investigation.

---

## Validation

- [x] Alert created
- [x] Alert triggered successfully
- [x] Results reviewed
