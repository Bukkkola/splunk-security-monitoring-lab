
# Authentication Detections

## Overview

This document contains Splunk Search Processing Language (SPL) detection queries used to monitor Windows authentication activity. These detections help identify normal login behavior, suspicious authentication attempts, credential misuse, and potential account compromise.

---

# Detection 1 – Successful Logons (Event ID 4624)

## Detection Objective

Identify successful Windows logons to establish authentication activity and support user behavior analysis.

### SPL Query

```spl
index=main EventCode=4624
| stats count by Account_Name, host, Logon_Type
| sort -count
```

### Security Use Case

- Monitor successful user authentication
- Establish authentication timelines
- Detect unusual login activity
- Identify user access patterns

### MITRE ATT&CK

| Technique | ID |
|-----------|----|
| Valid Accounts | T1078 |

### Investigation Checklist

- Was the login expected?
- Did it occur during normal working hours?
- Is the account privileged?
- Did the user log off (4634)?
- Was Event ID 4672 generated afterwards?

---

# Detection 2 – Failed Logons (Event ID 4625)

## Detection Objective

Detect repeated failed authentication attempts that may indicate brute-force attacks or password guessing.

### SPL Query

```spl
index=main EventCode=4625
| stats count by Account_Name, host
| where count >=5
| sort -count
```

### Security Use Case

- Detect brute-force attacks
- Detect password spraying
- Identify locked accounts

### MITRE ATT&CK

| Technique | ID |
|-----------|----|
| Brute Force | T1110 |

### Investigation Checklist

- Which account is being targeted?
- Which host generated the failures?
- Was there a successful login afterwards?
- Is the account privileged?

---

# Detection 3 – Explicit Credentials (Event ID 4648)

## Detection Objective

Detect authentication events where alternate credentials are supplied.

### SPL Query

```spl
index=main EventCode=4648
| table _time host Account_Name Process_Name
| sort -_time
```

### Security Use Case

- Detect alternate credential usage
- Monitor administrative tools
- Identify potential lateral movement

### MITRE ATT&CK

| Technique | ID |
|-----------|----|
| Use Alternate Authentication Material | T1550 |

### Investigation Checklist

- Which account supplied the credentials?
- Which process initiated the authentication?
- Was the activity expected?

---

# Detection 4 – User Logoff (Event ID 4634)

## Detection Objective

Track Windows session termination and correlate logoff activity with successful logons.

### SPL Query

```spl
index=main EventCode=4634
| stats count by Account_Name, host
| sort -count
```

### Security Use Case

- Monitor user session activity
- Build authentication timelines
- Support forensic investigations

### Investigation Checklist

- Was there a corresponding Event ID 4624?
- Was the session duration expected?
- Did the user perform privileged actions?

---

# Detection Summary

| Event ID | Detection Purpose |
|----------|-------------------|
| 4624 | Successful Logon Monitoring |
| 4625 | Failed Logon Detection |
| 4634 | User Session Tracking |
| 4648 | Explicit Credential Monitoring |
