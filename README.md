# Splunk Security Monitoring and Threat Detection Lab

## Overview

This project demonstrates how to build an enterprise-style Security Operations Center (SOC) lab using Splunk Enterprise.

The lab collects Windows security logs through the Splunk Universal Forwarder, analyzes events using Splunk Search Processing Language (SPL), and provides real-time security monitoring through dashboards, reports, and alerts.

---

## Objectives

- Install and configure Splunk Enterprise
- Configure the Splunk Universal Forwarder
- Collect Windows Event Logs
- Install and configure Sysmon
- Develop SPL detection queries
- Build custom security dashboards
- Create real-time alerts
- Investigate simulated security incidents
- Map detections to the MITRE ATT&CK framework
- Document the project on GitHub

---

## Lab Environment

| Component | Technology |
|-----------|------------|
| SIEM | Splunk Enterprise 10.4.2 |
| Host Machine | Apple MacBook Pro (M1) |
| Virtualization | UTM |
| Endpoint | Windows 11 |
| Log Collection | Splunk Universal Forwarder |
| Operating System | macOS + Windows |

---

## Repository Structure

```text
splunk-security-monitoring-lab/
│
├── README.md
├── documentation/
│   └── phase-1-installation.md
├── architecture/
├── dashboards/
├── detections/
├── incident-investigations/
└── screenshots/
```

---

## Project Phases

- ✅ Phase 1 – Install Splunk Enterprise
- ⏳ Phase 2 – Configure Log Ingestion
- ⏳ Phase 3 – Install Universal Forwarder
- ⏳ Phase 4 – Install Sysmon
- ⏳ Phase 5 – Develop SPL Detection Rules
- ⏳ Phase 6 – Build Dashboards
- ⏳ Phase 7 – Simulate Security Incidents
- ⏳ Phase 8 – Document Findings

---

## Skills Demonstrated

- Splunk Enterprise Administration
- Splunk Universal Forwarder
- Windows Event Log Analysis
- Search Processing Language (SPL)
- Security Monitoring
- Threat Detection
- Dashboard Development
- Alerting
- Incident Investigation
- MITRE ATT&CK Mapping

---

## Project Outcome

Successfully configured Splunk Enterprise to receive Windows Event Logs from a Windows 11 endpoint using Splunk Universal Forwarder.

Validated successful ingestion of Security, Application, and System event logs.

Successfully collected and searched Windows Security events including:

- Event ID 4624 (Successful Logon)
- Event ID 4634 (Logoff)
- Event ID 4648 (Explicit Credentials)
- Event ID 4672 (Special Privileges Assigned)
- Event ID 5379 (Credential Manager Access)
