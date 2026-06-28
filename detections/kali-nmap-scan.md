\# Detection: Kali Nmap Scan



\## Objective

Detect a possible Nmap SYN scan against a Windows endpoint using Windows Filtering Platform events collected by Wazuh.



\## Lab Setup

SIEM: Wazuh

Endpoint: Windows 11

Attacker/Tester: Kali Linux VM

Detection Source: Windows Security Event ID 5152



\## Test Commands

sudo nmap -sS -Pn --top-ports 100 192.168.0.118



\## Evidence

!\[Wazuh file modification alert](screenshots/kali-nmap-scan.png)

!\[Wazuh file modification alert](screenshots/wazuh-alert-possible-port-scan.png)

!\[Wazuh file modification alert](screenshots/wazuh-local-rules-port-scan.png)



\## Security Relevance

Repeated blocked packets from a single source may indicate network reconnaissance, port scanning, service discovery, or an attacker attempting to identify exposed services on a Windows endpoint.



\## Remediation

Validate whether the scan was authorized, identify the source IP address, review the scanned destination ports, check for related authentication or exploitation attempts, block or isolate unauthorized scanning systems, and tune Wazuh correlation rules to reduce false positives.

