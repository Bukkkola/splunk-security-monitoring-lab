

# Privilege Monitoring Detections

## Overview

This document contains Splunk Search Processing Language (SPL) detection queries used to monitor privileged account activity, administrative logons, and changes to security group memberships. These detections help identify privilege escalation, unauthorized administrative actions, and misuse of elevated permissions.

---

## Detection Summary

| Event ID | Detection | Status |
|----------|-----------|:------:|
| 4672 | Special Privileges Assigned to New Logon | ✅ Validated |
| 4732 | User Added to Local Security Group | ✅ Validated |
| 4733 | User Removed from Local Security Group | ✅ Validated |
