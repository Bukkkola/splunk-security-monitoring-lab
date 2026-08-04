
## Evidence

### Universal Forwarder Installation

### Objective

Deploy the Splunk Universal Forwarder on a Windows 11 endpoint to collect Windows Event Logs and securely forward them to the Splunk Enterprise server for centralized monitoring and analysis.

### Installation Summary

The Splunk Universal Forwarder was successfully installed on the Windows 11 virtual machine. After installation, the **SplunkForwarder** Windows service was configured to start automatically and verified to be in the **Running** state using the Windows Services console.

Running the service with an **Automatic** startup type ensures that log collection resumes automatically whenever the system restarts, providing continuous monitoring without manual intervention.

### Verification

The installation was verified by confirming that:

- The **SplunkForwarder** service was installed successfully.
- The service status was **Running**.
- The startup type was set to **Automatic**.
- The endpoint was ready to collect and forward Windows Event Logs.

### Skills Demonstrated

- Splunk Universal Forwarder Deployment
- Windows Service Administration
- Endpoint Log Collection
- SIEM Infrastructure Configuration
- Windows Endpoint Management

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

## Windows Forwarder Connected

![Windows Forwarder Connected](../screenshots/connection-verification.png)

### Objective

Verify that the Splunk Universal Forwarder running on the Windows 11 endpoint has successfully established a connection with the Splunk Enterprise server.


## Connection Verification

![Connection Verification](../screenshots/connection-verification.jpg)


After configuring the Splunk Universal Forwarder, network connectivity between the Windows 11 endpoint and the Splunk Enterprise server was verified using the `netstat` command.

The output confirmed:

- **LISTEN** – Splunk Enterprise is actively listening for incoming connections on TCP port **9997**.
- **ESTABLISHED** – An active TCP session exists between the Windows 11 endpoint (running the Splunk Universal Forwarder) and the Splunk Enterprise server, confirming that the forwarder successfully established a connection to the indexer.

This verification demonstrates that the communication channel required for forwarding Windows Event Logs is operational and that the Splunk Enterprise server is ready to receive security events for indexing and analysis.

### Verification Output

```text
tcp4  <Splunk-Server-IP>.9997     <Windows-Endpoint-IP>.54783     ESTABLISHED
tcp4  *.9997                      *.*                             LISTEN
```

> **Note:** Private IP addresses have been masked for security and privacy purposes.
