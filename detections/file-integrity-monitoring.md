\# Detection: File Integrity Monitoring



\## Objective

Detect file creation, modification, and deletion in a monitored Windows directory.



\## Lab Setup

SIEM: Wazuh

Endpoint: Windows 11

Attacker/Tester: Local Administrator PowerShell

Test Path: C:\\WazuhLab\\FIM



\## Test Commands

"Created by Wazuh FIM test" | Out-File C:\\WazuhLab\\FIM\\test.txt

Add-Content C:\\WazuhLab\\FIM\\test.txt "modified content"

Remove-Item C:\\WazuhLab\\FIM\\test.txt



\## Evidence

!\[Wazuh file modification alert](screenshots/wazuh-alert-file-modified.png)

!\[Wazuh file modification alert](screenshots/windows-ossec-conf-fim-config.png)

!\[Wazuh file modification alert](screenshots/windows-fim-test-powershell.png)



\## Security Relevance

Unexpected file mods may indicate tampering, malware, persistence, or unauthorized access of sensitive files.



\## Remediation

Validate the change, identify the user/process responsible, restore known-good files, and investigate related endpoint activity.

