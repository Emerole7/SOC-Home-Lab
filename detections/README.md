# Detection Engineering

This folder contains security detections developed and validated in a SOC home lab environment.
Each detection is based on simulated real-world attack activity and implemented in Splunk SIEM.

The purpose of these detections is to demonstrate Tier 1 SOC analyst skills, including log analysis,
alert logic development, and incident triage.

---

## Implemented Detections

### Brute Force Authentication Attempt (Windows EventCode 4625)
- Description: Detects repeated failed authentication attempts from the same source IP, indicating potential brute-force activity.
- Data Source: Windows Security Event Logs
- SIEM: Splunk Enterprise
- MITRE ATT&CK: T1110 – Brute Force
- Status: Implemented and validated

 File: `BRUTE_FORCE_4625.md`

---

## Detection Methodology

Each detection in this lab follows a SOC-style workflow:

1. Simulate an attack in a controlled lab environment
2. Verify event generation in Windows Event Viewer
3. Ingest logs into Splunk SIEM
4. Identify reliable fields for detection logic
5. Build and test SPL queries
6. Convert queries into alerts
7. Validate alert firing
8. Document detection logic and analyst response

---

## Notes

- Field names and sourcetypes may vary depending on Splunk configuration and Windows version.
- Thresholds are tuned for lab realism and may require adjustment in production environments.
- All detections are mapped to MITRE ATT&CK techniques where applicable.

---

- Successful logon after multiple failures (4624 following 4625)
File: SUCCESS_AFTER_FAILURE_4624_4625.md

Execution (Sysmon EventCode 1)** — Detects PowerShell abuse using command-line analysis.
File: SUSPICIOUS_POWERSHELL_SYSMON.md

## Planned Detections


- Privilege escalation via new local administrator account

