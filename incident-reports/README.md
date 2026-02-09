# Incident Reports

This folder contains documented incident reports generated from alerts detected in the SOC Home Lab.
Each report follows a simplified SOC incident response format and is based on validated SIEM alerts.

---

## Available Incident Reports

###  IR-001 — Brute Force Authentication Attempt
- Alert Source: Splunk SIEM
- Detection: Repeated failed authentication attempts (Windows EventCode 4625)
- Attack Type: Credential Access Brute Force
- MITRE ATT&CK: T1110
- Status: Investigated and documented

 File: IR-001-Brute-Force.md

###  IR-002 Successful logon after multiple failed attempts
File: IR-002-Success-After-Failure.md

### IR-003 Suspicious PowerShell execution
File: IR-003-Suspicious-Powershell.md

### IR-004 Privilege Escalation
File: IR-004-Privilege-Escalation.md

## Incident Response Workflow

Each incident report in this lab follows a SOC style response process:

1. Alert triggered by SIEM
2. Initial triage and validation
3. Evidence collection (logs and screenshots)
4. Indicator identification (IP, account, host)
5. Impact assessment
6. Response and containment recommendations
7. Lessons learned and improvement notes

---

## Notes

- All incidents are simulated in a controlled lab environment.
- Reports are written from a SOC analyst perspective, not an attacker perspective.
- The focus is on detection, investigation, and response, not exploitation.


  



