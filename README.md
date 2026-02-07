# SOC HomeLab
SOC home lab simulating real world attacks, SIEM detections, and incident response using Windows Server, Kali Linux, and Splunk.


# Overview
This project simulates a Security Operations Center (SOC) environment where real world attacks are generated and detected using a SIEM. The lab focuses on log analysis, alert creation, and incident response.

# Architecture
- Windows Server (log source)
- Kali Linux (attacker)
- SIEM (Splunk)
- Sysmon and Windows Event Logs

# Objectives
- Generate security telemetry
- Detect malicious activity
- Create SOC-style alerts
- Perform incident investigations
- Documentation

# Attack Scenarios
- Bruteforce authentication attacks
- Suspicious PowerShell execution
- Privilege escalation attempts

## Tools Used
- Windows Server
- Kali Linux
- Splunk
- Sysmon
- VirtualBox

## Sysmon Telemetry Considerations

PowerShell process creation events were observed in Sysmon logs; however,
field extraction varied by environment. To ensure detection accuracy,
PowerShell Image and CommandLine values were extracted from raw Sysmon XML
within Splunk searches. We used a custom sysmon config to log PowerShell
process creation events. This ensured that PowerShell executions were
captured under Sysmon EventCode 1 with full command-line visibility.
