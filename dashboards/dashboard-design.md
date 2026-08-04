
# Splunk Security Monitoring Dashboards

## Overview

This document describes the dashboards created to visualize Windows Security Events collected by Splunk Enterprise. These dashboards provide security analysts with real-time visibility into authentication activity, privileged access, and event trends.

---

## Planned Dashboards

| Dashboard | Purpose | Status |
|-----------|---------|--------|
| Authentication Overview | Monitor successful and failed logons | ⏳ Planned |
| Top Windows Event IDs | Display the most common Windows Security Events | ⏳ Planned |
| Authentication Timeline | Visualize authentication activity over time | ⏳ Planned |
| Privileged Logons | Monitor Event ID 4672 | ⏳ Planned |
| Explicit Credential Usage | Monitor Event ID 4648 | ⏳ Planned |
| Top Hosts | Identify systems generating the most security events | ⏳ Planned |

---
# Dashboard Design

## Overview

The Windows Security Monitoring Dashboard was designed to provide real-time visibility into Windows authentication activity collected from a monitored Windows endpoint using Splunk Enterprise.

The dashboard consolidates key Windows Security Events into a single interface, enabling security analysts to quickly monitor authentication activity, identify privileged logons, review recent events, and investigate potential security incidents.

---

## Dashboard Layout

The dashboard contains three primary visualizations:

### 1. Authentication Events Over Time

Displays authentication-related Windows Security Events over time.

**Purpose**

- Monitor authentication trends
- Identify spikes in login activity
- Detect unusual authentication patterns
- Correlate events during investigations

**Events Monitored**

- Event ID 4624 – Successful Logon
- Event ID 4634 – User Logoff
- Event ID 4648 – Logon Using Explicit Credentials
- Event ID 4672 – Special Privileges Assigned

---

### 2. Top Windows Security Events

Displays the total number of collected Windows Security Events grouped by Event ID.

**Purpose**

- Identify the most common authentication events
- Establish normal activity baselines
- Detect abnormal increases in specific event types
- Monitor privileged account activity

---

### 3. Recent Authentication Events

Displays the latest authentication events collected by Splunk.

**Fields Displayed**

- Time
- Event ID
- Host

**Purpose**

- Review recent authentication activity
- Verify successful log ingestion
- Support security investigations
- Correlate authentication events

---

## Dashboard Screenshot

![Dashboard Overview](../screenshots/dashboard-overview.png)

---

## Design Goals

The dashboard was designed to:

- Provide centralized authentication monitoring
- Reduce investigation time
- Improve visibility into Windows Security Events
- Support Security Operations Center (SOC) monitoring
- Enable rapid detection of suspicious authentication activity

---

## Technologies Used

- Splunk Enterprise
- Splunk Dashboard Studio
- Windows Event Logs
- Splunk Search Processing Language (SPL)

---

## Skills Demonstrated

- Dashboard Design
- Security Monitoring
- Windows Event Analysis
- Security Data Visualization
- Splunk Dashboard Studio
- SPL Query Development
## Notes

These dashboards will be created during the dashboard development phase using Splunk Search Processing Language (SPL).
