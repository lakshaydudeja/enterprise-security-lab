# Splunk SIEM Setup

## Overview
This document covers the Splunk setup used in the Enterprise Security Lab. Splunk is used as the SIEM platform to collect, search, and analyze security logs from lab systems.

## Purpose
The purpose of Splunk in this lab is to:

- Collect logs from Windows systems
- Analyze Windows security events
- Practice SIEM searching and investigation
- Build SOC analyst skills
- Support future threat detection and alerting use cases

## Lab Configuration

| Component | Configuration |
|---|---|
| Splunk Server OS | Ubuntu Server |
| Splunk Role | Indexer / Search Head |
| Splunk Server IP | 10.0.0.5 |
| Forwarding Port | 9997 |
| Log Source | Windows 10 VM |
| Forwarder | Splunk Universal Forwarder |

## Completed Configuration

- Installed Ubuntu Server as a virtual machine in VMware Workstation
- Installed Splunk Enterprise on Ubuntu Server
- Configured Splunk web interface access
- Enabled receiving on port `9997`
- Installed Splunk Universal Forwarder on Windows 10 VM
- Configured Windows 10 VM to forward logs to Splunk server `10.0.0.5`
- Verified Windows event logs appearing in Splunk

## Log Sources

| Source | Log Type | Purpose |
|---|---|---|
| Windows 10 VM | Windows Event Logs | Endpoint monitoring |
| Security Event Log | Authentication events | Login and failed login analysis |
| System Event Log | System events | Troubleshooting and monitoring |
| Application Event Log | Application events | Application-level visibility |

## Verification

| Test | Result |
|---|---|
| Splunk web interface accessible | Successful |
| Receiving port `9997` enabled | Successful |
| Universal Forwarder installed | Successful |
| Windows logs forwarded to Splunk | Successful |
| Security logs searchable in Splunk | Successful |

## Example Searches

```spl
index=* sourcetype=WinEventLog:Security
```

```spl
index=* EventCode=4625
```

```spl
index=* EventCode=4624
```

## Screenshots

Screenshots to be added:

- Splunk web interface
- Receiving port configuration
- Universal Forwarder installation
- Windows event logs in Splunk
- Failed login event search
- Successful login event search

## Notes
Splunk is used as the central log analysis platform in this lab. It allows Windows security events to be collected and searched, helping simulate real SOC monitoring and investigation workflows.
