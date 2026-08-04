
# Phase 4 – Windows Event Collection & Analysis

## Overview

After deploying and configuring the Splunk Universal Forwarder, Windows Event Logs were successfully collected and forwarded to Splunk Enterprise. This phase validates the end-to-end log collection pipeline by demonstrating that Windows Security events were successfully ingested, indexed, and made available for searching and analysis using Splunk Search Processing Language (SPL).

The collected events provide valuable visibility into authentication activity, privileged access, credential usage, and user session management, forming the foundation for security monitoring and threat detection.

## Windows Security Events

![Windows Security Events](../screenshots/search-security-events.jpg)

Windows Security Event Logs were successfully ingested into Splunk Enterprise and indexed in the **main** index. Searches returned multiple security events, including:

- Event ID 4624 – Successful Logon
- Event ID 4634 – User Logoff
- Event ID 4648 – Logon Using Explicit Credentials
- Event ID 4672 – Special Privileges Assigned to New Logon

This confirms that the end-to-end log collection pipeline—from the Windows endpoint, through the Splunk Universal Forwarder, to Splunk Enterprise—is functioning correctly.
## Security Events Collected

| Event ID | Description | Security Use Case |
|----------|-------------|-------------------|
| 4624 | Successful Logon | Monitor successful user authentication and establish authentication timelines. |
| 4634 | User Logoff | Track user session termination and correlate authentication activity. |
| 4648 | Logon Using Explicit Credentials | Detect alternate credential usage and potential lateral movement. |
| 4672 | Special Privileges Assigned | Monitor privileged account activity and administrative logons. |

## Event ID 4624 – Successful Logon

![Event ID 4624 successful-logon](../screenshots/event-4624.jpg)

Event ID **4624** records a successful user authentication on a Windows system. This event is generated whenever a user or service successfully logs on and is one of the most frequently analyzed security events during incident investigations.

Monitoring Event ID 4624 enables security analysts to:

- Verify successful user authentication
- Identify interactive, network, or remote logons
- Correlate user activity with other security events
- Establish authentication timelines during investigations
- Detect unusual login patterns and potential unauthorized access

In this lab, Splunk successfully ingested Event ID 4624 from the Windows endpoint, confirming that authentication events were collected and indexed correctly.

---
## Event ID 4634 – User Logoff

![Event ID 4634 Logoff](../screenshots/event-4634.jpg)



Event ID **4634** is generated when a user logs off from a Windows system, indicating that a logon session has ended. This event helps complete the authentication lifecycle by identifying when user sessions are terminated.

Monitoring Event ID 4634 enables security analysts to:

- Track user session termination
- Correlate logoff events with successful logons (Event ID 4624)
- Build user activity timelines during investigations
- Identify abnormal session durations
- Support forensic analysis by reconstructing user activity

In this lab, Splunk successfully collected and indexed Event ID 4634, demonstrating the ability to monitor user session activity and correlate authentication events from the Windows endpoint.

## Event ID 4648 – Logon Using Explicit Credentials

![Event ID 4648 Explicit Credentials](../screenshots/event-4648.jpg)


Event ID **4648** is generated when a user or process attempts to log on using credentials that are explicitly provided rather than the credentials of the currently logged-on user. This event commonly occurs when administrative tools, remote management utilities, scheduled tasks, or applications authenticate using alternate credentials.

Monitoring Event ID 4648 enables security analysts to:

- Identify the use of alternate or explicit credentials
- Detect potential lateral movement between systems
- Monitor administrative and remote management activities
- Investigate suspicious authentication attempts
- Correlate credential usage with other security events during incident investigations

In this lab, Splunk successfully ingested Event ID 4648 from the Windows endpoint, confirming that explicit credential authentication events were collected and indexed correctly.


## Event ID 4672 – Special Privileges Assigned to New Logon

![Event ID 4672 special priviledges](../screenshots/event-4672.jpg)

Event ID **4672** is generated when a user logs on with administrative or other highly privileged rights. This event is commonly associated with administrator accounts and privileged service accounts.

Monitoring Event ID 4672 helps security analysts:

- Detect privileged account activity
- Identify administrative logins
- Monitor the use of elevated permissions
- Investigate potential privilege escalation attempts
- Correlate privileged logons with authentication events such as Event ID 4624

During this lab, Splunk successfully collected and indexed Event ID 4672, demonstrating the ability to monitor privileged authentication activity from the Windows endpoint

## Phase Summary

This phase successfully validated the collection and analysis of Windows Security Event Logs within Splunk Enterprise.

The deployment successfully ingested and indexed key authentication and privilege-related events, including successful logons, user logoffs, explicit credential usage, and privileged logons.

These events provide the foundation for security monitoring, threat detection, dashboard creation, and incident investigations in subsequent phases of the project.

### Skills Demonstrated

- Windows Event Log Analysis
- Splunk Search Processing Language (SPL)
- Windows Authentication Monitoring
- Privileged Access Monitoring
- Security Event Correlation
- Security Monitoring
- SIEM Operations
