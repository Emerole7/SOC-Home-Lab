# SOC Home Lab Architecture

This section documents the architecture of the SOC Home Lab and how security telemetry flows from endpoints to the SIEM.

The architecture is intentionally simple and realistic, mirroring a small enterprise SOC environment.



## Architecture Overview

The lab consists of an attacker system, a monitored Windows server, and a centralized SIEM for detection and alerting.

- Kali Linux simulates attacker activity
- Windows Server 2012 R2 acts as the monitored endpoint and log source
- Splunk Enterprise serves as the SIEM platform

All systems communicate within an isolated internal network.

--

## Components

### Attacker
- Kali Linux
- Simulates bruteforce authentication attempts via RDP

### Log Source
- Windows Server
- Windows Security Event Logs
- Sysmon (enhanced host telemetry)

### SIEM
- Splunk Enterprise
- Ingests Windows Security, System, Application, and Sysmon logs
- Performs detection and alerting

---

## Log Flow

1. Attacker generates malicious activity (failed RDP logins)
2. Windows Server records events (EventCode 4625)
3. Sysmon captures additional host telemetry
4. Logs are ingested into Splunk
5. Splunk correlation logic evaluates events
6. Alert is generated and investigated

---

## Network Design

- VirtualBox Internal Network (`SOC-LAB`)
- No direct internet exposure
- Controlled lab-only communication

---

## Purpose

This architecture supports:
- SOC-style monitoring
- Detection engineering
- Incident investigation
- Alert validation

