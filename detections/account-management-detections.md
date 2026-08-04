
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
