# Project: Detecting Suspicious Login Attempts Using Splunk SIEM

## Overview
This simulated cybersecurity project demonstrates how a SOC (Security Operations Center) Analyst can detect brute-force login attempts using Splunk SIEM. It involves analyzing failed login events, identifying suspicious IPs, creating alerts, and documenting incident response steps.

## Tools Used
- Splunk SIEM (Simulated)
- Windows Security Logs (Event ID 4625)

## Objectives
- Monitor failed login attempts using Event ID 4625
- Create detection rules and alerts in Splunk
- Identify potentially malicious IP addresses
- Recommend incident response and remediation steps

## Key Detection Logic
```spl
sourcetype="WinEventLog:Security" EventCode=4625 
| stats count by src_ip, user 
| where count > 10
```

## Screenshots
📸 **Included in repository**:
- Splunk Dashboard - Failed Logins by IP
- Splunk Alert Configuration Screen
- Sample Alert Trigger

## Incident Response Plan
- Investigate source IP via OSINT (e.g., VirusTotal, AbuseIPDB)
- Disable or lock compromised user accounts
- Notify IT/Security teams
- Add IP to blocklist or firewall
- Educate users if phishing involved

## Outcome
This project demonstrates core skills required in entry-level SOC Analyst roles:
- Log analysis
- Alert creation
- MITRE ATT&CK understanding
- Writing IR documentation

## Author
Manisha Luthra  
[LinkedIn](https://www.linkedin.com/in/manishaluthra12)  
📧 manishaluthra03@gmail.com
