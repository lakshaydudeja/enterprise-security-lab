# Windows 10 Endpoint Setup

## Overview
This document covers the Windows 10 endpoint setup used in the Enterprise Security Lab. The Windows 10 VM is used as a domain-joined workstation and log source for Splunk.

## Purpose
The purpose of the Windows 10 endpoint in this lab is to:

- Simulate an enterprise user workstation
- Join the Active Directory domain
- Generate Windows authentication and security events
- Forward Windows event logs to Splunk
- Support SOC-style log analysis and investigation

## Lab Configuration

| Component | Configuration |
|---|---|
| Operating System | Windows 10 Education |
| Platform | VMware Workstation |
| IP Address | 10.0.0.2 |
| Default Gateway | 10.0.0.1 |
| Domain | Lab.local |
| Log Forwarding | Splunk Universal Forwarder |
| Splunk Server | 10.0.0.5 |

## Completed Configuration

- Installed Windows 10 Education as a virtual machine in VMware Workstation
- Connected Windows 10 VM to the internal lab network
- Configured network connectivity through pfSense
- Joined Windows 10 VM to the `Lab.local` domain
- Verified domain login functionality
- Installed Splunk Universal Forwarder
- Configured Windows event log forwarding to Splunk server `10.0.0.5`
- Verified Windows security logs appearing in Splunk

## Verification

| Test | Result |
|---|---|
| Windows 10 VM installed | Successful |
| Connected to internal lab network | Successful |
| pfSense reachable from Windows 10 | Successful |
| Domain join to `Lab.local` completed | Successful |
| Domain login tested | Successful |
| Splunk Universal Forwarder installed | Successful |
| Windows event logs visible in Splunk | Successful |

## Event Logs Forwarded

| Log Source | Purpose |
|---|---|
| Security | Authentication and security-related events |
| System | Operating system and service events |
| Application | Application-level events |

## Screenshots

Screenshots to be added:

- Windows 10 VM network settings
- IP configuration
- Domain join confirmation
- Domain login screen
- Splunk Universal Forwarder installation
- Windows logs visible in Splunk

## Notes
The Windows 10 endpoint acts as the main workstation in this lab. It provides realistic Windows activity and security logs for Splunk analysis and future SOC investigation scenarios.
