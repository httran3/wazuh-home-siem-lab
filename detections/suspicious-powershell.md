\# Detection: Suspicious PowerShell Commands



\## Objective

Detect suspicious PowerShell command execution on a Windows endpoint using Sysmon logs collected by Wazuh.



\## Lab Setup

SIEM: Wazuh

Endpoint: Windows 11

Attacker/Tester: Local Administrator PowerShell



\## Test Commands

powershell -ExecutionPolicy Bypass -Command "whoami"

powershell -NoProfile -ExecutionPolicy Bypass -Command "Get-LocalUser"

powershell -EncodedCommand dwBoAG8AYQBtAGkA

powershell -NoProfile -WindowStyle Hidden -Command "Get-Process"



\## Evidence

!\[Wazuh file modification alert](screenshots/windows-sysmon-created.png)

!\[Wazuh file modification alert](screenshots/wazuh-alert-sysmon.png)

!\[Wazuh file modification alert](screenshots/windows-suspicious-commands.png)

!\[Wazuh file modification alert](screenshots/wazuh-alert-suspicious-commands.png)



\## Security Relevance

Suspicious PowerShell commands may indicate probing, enumerating users, bypassing restrictions, and hiding activity through hidden execution.



\## Remediation

Validate whether the PowerShell activity was authorized, identify the user and parent process, review the full command line, investigate related Sysmon events, isolate the endpoint if malicious activity is confirmed, and tune Wazuh rules to reduce false positives.

