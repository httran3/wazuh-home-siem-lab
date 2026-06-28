\# Wazuh Home SIEM Lab



## Summary
This project documents a home SIEM lab built with Wazuh, a Windows 11 endpoint, Sysmon, PowerShell, and Kali Linux. The lab simulates common security events, validates Wazuh alerting, and documents detection evidence, security relevance, and remediation steps.



## Lab Environment
\- SIEM: Wazuh 4.14.5
\- Wazuh Server VM: 192.168.0.207
\- Windows 11 Endpoint: 192.168.0.118
\- Kali Linux VM: attacker/testing system
\- Virtualization: VMware Workstation Pro
\- Test Method: Simulated local activity and network reconnaissance in a controlled lab environment



## Detection Scenarios
| Detection | Description | Documentation |
| File Integrity Monitoring | Detected file creation, modification, and deletion in a monitored Windows directory. | \[View detection](file-integrity-monitoring.md) |
| Kali Nmap Scan | Detected possible network reconnaissance against a Windows endpoint. | \[View detection](kali-nmap-scan.md) |
| Suspicious PowerShell Commands | Detected suspicious PowerShell execution patterns using Sysmon logs collected by Wazuh. | \[View detection](suspicious-powershell.md) |
| Windows Local User Creation | Detected local account creation and administrator group modification. | \[View detection](windows-local-user-creation.md) |



## Skills Demonstrated
\SIEM deployment and endpoint onboarding
\Wazuh agent configuration
\Windows event monitoring
\Sysmon log collection
\File Integrity Monitoring
\PowerShell-based detection testing
\Network reconnaissance detection with Nmap
\Alert validation and documentation
\Basic incident response and remediation writing



## Evidence
Example Wazuh dashboard and alert evidence are stored in the `screenshots/` directory.
!\[Wazuh Agent Active](screenshots/agents-active.png)



\## Notes
All activity was performed in a local, controlled lab environment for defensive security learning and documentation.
