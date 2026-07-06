# False Positives & Detection Tuning

## Common False Positives

The following activities may legitimately generate PowerShell execution events:

- System administrators performing maintenance
- IT automation and deployment scripts
- Software installation or updates
- Enterprise management tools (e.g., SCCM, Intune)
- Security products
- Splunk Universal Forwarder scheduled tasks

---

## Tuning Recommendations

To reduce unnecessary alerts, consider:

- Excluding approved administrator accounts.
- Excluding known management servers.
- Monitoring for unusual parent processes.
- Prioritizing encoded PowerShell commands.
- Monitoring PowerShell executed outside business hours.
- Monitoring PowerShell launched from Microsoft Office applications.

---

## Future Improvements

This detection can be enhanced by:

- Detecting `-EncodedCommand`
- Detecting `-ExecutionPolicy Bypass`
- Detecting hidden PowerShell windows
- Detecting suspicious download commands
- Correlating with network connections
- Assigning a higher severity when multiple suspicious indicators are present
