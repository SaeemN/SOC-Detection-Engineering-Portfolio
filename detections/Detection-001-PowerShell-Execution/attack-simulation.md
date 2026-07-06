
# Attack Simulation

## Objective

Generate a Windows Security Event ID 4688 by executing PowerShell on the Windows 10 virtual machine.

## Test Environment

| Component | Value |
|----------|-------|
| Host | Windows 10 VM |
| User | Victim Windows 10 |
| Event ID | 4688 |
| Process | powershell.exe |

## Steps Performed

1. Open **Command Prompt**.

```cmd
powershell
```

2. Execute a simple PowerShell command.

```powershell
Get-Date
```

3. Exit PowerShell.

```powershell
exit
```

## Expected Result

Windows generates **Security Event ID 4688** indicating that **powershell.exe** has been created.

The Splunk Universal Forwarder collects the event and forwards it to Splunk Enterprise.

The detection query identifies the event and triggers the configured alert.

## Validation

- [x] Event generated
- [x] Event forwarded to Splunk
- [x] Detection query matched
- [x] Alert triggered
