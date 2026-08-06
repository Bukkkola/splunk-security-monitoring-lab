
# Detection 1 – Special Privileges Assigned to New Logon (Event ID 4672)

## Detection Objective

Detect successful logons where Windows assigns administrative or elevated privileges to a user account. This detection helps identify privileged account usage that could indicate administrative activity or potential privilege escalation.

## SPL Query

```spl
index=main EventCode=4672
```

## Security Use Case

- Monitor privileged logons
- Detect administrative account usage
- Identify privileged sessions
- Support privilege escalation investigations
- Establish administrative activity baselines

## MITRE ATT&CK

| Technique | ID |
|-----------|----|
| Valid Accounts | T1078 |
| Abuse Elevation Control Mechanism | T1548 |

## Investigation Checklist

- Which account received special privileges?
- Is the account expected to have administrative access?
- Did the privileged logon occur during normal business hours?
- Was the logon followed by administrative actions?
- Did the source host match expected administrator activity?

## Validation

A privileged Windows account logged on to the monitored endpoint, generating Windows Security Event ID 4672.

Splunk successfully collected and indexed the event, confirming that privileged logons are monitored and available for security investigations.

## Evidence

**Validation Query**

```spl
index=main EventCode=4672
```

**Screenshot**

![Special Privileges Assigned Detection](../screenshots/special-privileges-detection.jpg)

## Outcome

The detection successfully identified privileged logon activity by monitoring Windows Security Event ID 4672. This provides visibility into administrative account usage and enables security analysts to detect unexpected privileged sessions that may indicate privilege escalation or unauthorized administrative access.
