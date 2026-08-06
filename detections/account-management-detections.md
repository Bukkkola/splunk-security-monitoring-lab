
# Account Management Detections

## Overview

This document will contain Splunk SPL detection queries for monitoring Windows account management activities, including user creation, account deletion, password changes, account lockouts, and group membership modifications.

These detections will be added after generating and collecting the corresponding Windows Security Events during the attack simulation phase of this project.

## Planned Detections

- Event ID 4720 – User Account Created
- Event ID 4722 – User Account Enabled
- Event ID 4723 – Password Change Attempt
- Event ID 4724 – Password Reset
- Event ID 4725 – User Account Disabled
- Event ID 4726 – User Account Deleted
- Event ID 4732 – User Added to Privileged Group
- Event ID 4733 – User Removed from Group
- Event ID 4740 – User Account Locked Out

# Account Management Detections

## Overview

This document contains Splunk Search Processing Language (SPL) detection queries used to monitor Windows account management activities. These detections provide visibility into the lifecycle of user accounts, including account creation, modification, deletion, lockout events, and other administrative changes that may indicate unauthorized activity or privilege abuse.

---

# Detection Status

| Event ID | Detection | Status |
|----------|-----------|:------:|
| **4720** | User Account Created | ✅ Completed |
| **4722** | User Account Enabled | ⏳ Planned |
| **4723** | Password Change Attempt | ⏳ Planned |
| **4724** | Password Reset | ⏳ Planned |
| **4725** | User Account Disabled | ⏳ Planned |
| **4726** | User Account Deleted | ✅ Completed |
| **4732** | User Added to Privileged Group | ⏳ Planned |
| **4733** | User Removed from Group | ⏳ Planned |
| **4738** | User Account Changed | ✅ Completed |
| **4740** | User Account Locked Out | ✅ Completed |

---

## Completed Detections

The following detections have been implemented, validated, and documented using Windows Security Event Logs collected by Splunk.

- ✅ Event ID 4720 – User Account Created
- ✅ Event ID 4726 – User Account Deleted
- ✅ Event ID 4738 – User Account Changed
- ✅ Event ID 4740 – User Account Locked Out

Each completed detection includes:

- Detection Objective
- SPL Query
- Security Use Case
- MITRE ATT&CK Mapping
- Investigation Checklist
- Validation
- Evidence
- Outcome

---

## Planned Detections

The following account management detections will be implemented in future phases of this project.

- Event ID 4722 – User Account Enabled
- Event ID 4723 – Password Change Attempt
- Event ID 4724 – Password Reset
- Event ID 4725 – User Account Disabled
- Event ID 4732 – User Added to Privileged Group
- Event ID 4733 – User Removed from Group

These detections will expand monitoring coverage for Windows account lifecycle events and privileged account management.
