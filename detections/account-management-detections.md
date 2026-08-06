
# Account Management Detections

## Overview

This document contains Splunk Search Processing Language (SPL) detection queries used to monitor Windows account management activities. These detections provide visibility into the lifecycle of user accounts, including account creation, modification, deletion, and lockout events. Monitoring these events helps identify unauthorized administrative activity, privilege abuse, and potential indicators of compromise.

---
## Detection Summary

| Event ID | Detection | Status |
|----------|-----------|:------:|
| **4720** | [User Account Created](../documentation/phase-7-account-management.md#user-account-created) | ✅ Validated |
| **4726** | [User Account Deleted](../documentation/phase-7-account-management.md#user-account-deleted) | ✅ Validated |
| **4738** | [User Account Changed](../documentation/phase-7-account-management.md#user-account-changed) | ✅ Validated |
| **4740** | [User Account Locked Out](../documentation/phase-7-account-management.md#user-account-locked-out) | ✅ Validated |
## Skills Demonstrated

- Windows Security Event Monitoring
- Splunk Search Processing Language (SPL)
- Windows Account Management Monitoring
- Detection Engineering
- Security Event Analysis
- Windows Security Auditing
- Log Collection and Analysis
- Security Operations (SOC)
- Incident Investigation
- MITRE ATT&CK Mapping

---

## Outcome

This phase successfully implemented and validated four Windows account management detections using Splunk Enterprise.

The completed detections provide visibility into the complete lifecycle of Windows user accounts, including account creation, deletion, modification, and lockout events. By validating each detection with real Windows Security Event Logs, the project demonstrates practical experience in building detection logic, analyzing security events, and documenting investigation procedures commonly performed by Security Operations Center (SOC) analysts.

These detections strengthen the overall Splunk Security Monitoring Lab by expanding coverage beyond authentication events to include account administration and identity-related security monitoring.
 

These detections will expand monitoring coverage for Windows account lifecycle events and privileged account management.
