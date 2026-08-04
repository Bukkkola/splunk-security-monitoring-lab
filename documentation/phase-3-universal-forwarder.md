
## Evidence

### Universal Forwarder Installed

![Universal Forwarder](../screenshots/universal-forwarder.jpg)

The Splunk Universal Forwarder service was successfully installed and configured on the Windows 11 endpoint. The Windows Services console confirms that the **SplunkForwarder** service is running with an **Automatic** startup type, ensuring that log collection continues automatically after system reboots. This verifies that the endpoint is ready to collect and forward Windows Event Logs to the Splunk Enterprise server.

## Configure `inputs.conf`

The **inputs.conf** file was created to configure the Splunk Universal Forwarder to monitor Windows Event Logs. Three Windows log sources were enabled:

- Security
- System
- Application

These logs are forwarded to Splunk Enterprise for centralized security monitoring and analysis.

### Configuration

```ini
[WinEventLog://Security]
disabled = 0
index = main
start_from = oldest

[WinEventLog://System]
disabled = 0
index = main
start_from = oldest

[WinEventLog://Application]
disabled = 0
index = main
start_from = oldest
```
## Configure `outputs.conf`

The **outputs.conf** file was configured to forward collected Windows Event Logs to the Splunk Enterprise indexer.

### Configuration

- Destination: Splunk Enterprise
- Protocol: TCP
- Receiving Port: 9997

The Universal Forwarder successfully established communication with the Splunk Enterprise server over TCP port 9997.
