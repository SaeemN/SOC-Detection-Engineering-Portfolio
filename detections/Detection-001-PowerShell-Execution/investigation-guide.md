# Investigation Guide

## Objective

Determine whether the detected PowerShell execution is legitimate administrative activity or potentially malicious behavior.

---

## Investigation Steps

### 1. Review the User

Check the `Account_Name` field.

Questions to ask:
- Who executed PowerShell?
- Is this a normal user or an administrator?
- Is the account expected to use PowerShell?

---

### 2. Review the Parent Process

Check the `Creator_Process_Name` field.

Examples:

| Parent Process | Assessment |
|---------------|------------|
| cmd.exe | Common and usually expected |
| explorer.exe | User launched manually |
| winword.exe | Suspicious |
| excel.exe | Suspicious |
| outlook.exe | Suspicious |
| wscript.exe | Requires investigation |

---

### 3. Review the Endpoint

Check:
- Computer name
- Asset owner
- Business purpose of the system

Questions:
- Is this a workstation or a server?
- Is PowerShell commonly used on this endpoint?

---

### 4. Review Event Time

Questions:
- Did execution occur during business hours?
- Was the user expected to be active?
- Does the time align with other suspicious events?

---

### 5. Search for Related Activity

Look for:

- Additional PowerShell executions
- Failed logons (4625)
- Successful logons (4624)
- Scheduled Tasks
- Network connections
- Encoded PowerShell commands

---

## Escalation Criteria

Escalate the alert if:

- PowerShell was launched by Microsoft Office.
- Encoded commands are observed.
- Unknown users executed PowerShell.
- Multiple suspicious events occur together.
- Malicious command-line arguments are present.

---

## False Positives

Common legitimate causes include:

- System administrators
- IT automation scripts
- Software updates
- Splunk Universal Forwarder
- Enterprise management tools
