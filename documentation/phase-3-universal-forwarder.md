
## Evidence

### Universal Forwarder Installed

![Universal Forwarder](../screenshots/universal-forwarder.jpg)

The Splunk Universal Forwarder service was successfully installed and configured on the Windows 11 endpoint. The Windows Services console confirms that the **SplunkForwarder** service is running with an **Automatic** startup type, ensuring that log collection continues automatically after system reboots. This verifies that the endpoint is ready to collect and forward Windows Event Logs to the Splunk Enterprise server.

---
### Windows Security Events

Windows Security Event Logs were successfully ingested into Splunk Enterprise and indexed in the **main** index. Searches returned multiple security events, including successful logons (Event ID **4624**), privileged logons (Event ID **4672**), logoff events (Event ID **4634**), and explicit credential usage (Event ID **4648**). This confirms that the end-to-end log collection pipeline—from the Windows endpoint, through the Universal Forwarder, to Splunk Enterprise—is functioning correctly.

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

## Event ID 4672 – Special Privileges Assigned to New Logon

![Event ID 4672 special priviledges](../screenshots/event-4672.jpg)

Event ID **4672** is generated when a user logs on with administrative or other highly privileged rights. This event is commonly associated with administrator accounts and privileged service accounts.

Monitoring Event ID 4672 helps security analysts:

- Detect privileged account activity
- Identify administrative logins
- Monitor the use of elevated permissions
- Investigate potential privilege escalation attempts
- Correlate privileged logons with authentication events such as Event ID 4624

During this lab, Splunk successfully collected and indexed Event ID 4672, demonstrating the ability to monitor privileged authentication activity from the Windows endpoint.
