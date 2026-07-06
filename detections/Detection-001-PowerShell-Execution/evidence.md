# Detection Evidence

## Purpose

This document contains evidence demonstrating that the PowerShell execution detection was successfully tested in the lab.

---

## Evidence Collected

### 1. PowerShell Execution

**Description:** PowerShell was launched from Command Prompt on the Windows 10 VM to generate Event ID 4688.

**Screenshot:** *(To be added)*

---

### 2. Windows Security Event 4688

**Description:** Windows Security Log showing the creation of `powershell.exe`.

**Screenshot:** *(To be added)*

---

### 3. Splunk Search Results

**Description:** SPL query successfully detected the PowerShell execution event.

**Screenshot:** *(To be added)*

---

### 4. Splunk Alert

**Description:** Scheduled alert triggered successfully after the detection matched the event.

**Screenshot:** *(To be added)*

---

## Validation Summary

- ✅ PowerShell executed
- ✅ Event ID 4688 generated
- ✅ Universal Forwarder sent the event
- ✅ Splunk indexed the event
- ✅ Detection query matched
- ✅ Alert triggered successfully
