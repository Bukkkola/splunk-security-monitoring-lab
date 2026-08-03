# Phase 2 – Configure Log Ingestion

## Objective

Configure Splunk Enterprise to receive Windows security logs from the Splunk Universal Forwarder.

## Steps Completed

- Opened Splunk Settings.
- Navigated to **Forwarding and Receiving**.
- Configured a receiving port.
- Enabled TCP port **9997** for incoming data.

## Why Port 9997?

Port **9997** is the default port used by the Splunk Universal Forwarder to securely send logs to a Splunk Enterprise server.

## Result

Splunk is now configured to receive logs from remote systems.

## Evidence

The screenshot below shows Splunk Enterprise configured to receive incoming data on TCP port **9997**.

![Receiving Port](../screenshots/phase-2-receiving-port.jpg)

## Next Step

Install the Splunk Universal Forwarder on the Windows 11 virtual machine.

