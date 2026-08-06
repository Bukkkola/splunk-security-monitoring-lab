# Phase 7 – Account Management Monitoring

## Overview

This phase focused on monitoring Windows account management events using Splunk Enterprise. Security detections were created to identify user account creation, deletion, modification, and lockout events.

## Objectives

- Monitor user account creation
- Monitor user account deletion
- Detect account lockouts
- Track account modifications
- Validate detections using real Windows Security Events

## Activities Performed

- Created a temporary local user account
- Verified Event ID 4720 in Event Viewer
- Confirmed Event ID 4720 was forwarded to Splunk
- Created an SPL detection query
- Captured validation screenshots

## Results

- Successfully collected Event ID 4720
- Validated account creation monitoring
- Confirmed Windows Security logs were indexed in Splunk


![User Account Created](../screenshots/account-created-detection.jpg)
