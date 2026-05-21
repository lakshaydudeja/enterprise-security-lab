# Ubuntu Splunk Server Setup

## Overview
This document covers the Ubuntu Server setup used to host Splunk Enterprise in the Enterprise Security Lab. Ubuntu Server acts as the central SIEM server for collecting and analyzing logs from lab systems.

## Purpose
The purpose of the Ubuntu Splunk server in this lab is to:

- Host Splunk Enterprise
- Receive forwarded logs from Windows endpoints
- Provide a central platform for log searching and analysis
- Support SOC-style monitoring and investigation workflows
- Store and analyze Windows event logs

## Lab Configuration

| Component | Configuration |
|---|---|
| Operating System | Ubuntu Server |
| Platform | VMware Workstation |
| IP Address | 10.0.0.5 |
| Default Gateway | 10.0.0.1 |
| Application | Splunk Enterprise |
| Splunk Web Port | 8000 |
| Forwarding Port | 9997 |
| Role | SIEM server |

## Completed Configuration

- Installed Ubuntu Server as a virtual machine in VMware Workstation
- Connected Ubuntu Server to the internal lab network
- Configured network connectivity through pfSense
- Installed Splunk Enterprise on Ubuntu Server
- Configured Splunk web interface access
- Enabled Splunk receiving on port `9997`
- Verified Windows event logs being received from the Windows 10 VM

## Verification

| Test | Result |
|---|---|
| Ubuntu Server installed | Successful |
| Connected to internal lab network | Successful |
| pfSense reachable from Ubuntu Server | Successful |
| Splunk Enterprise installed | Successful |
| Splunk web interface accessible | Successful |
| Receiving port `9997` enabled | Successful |
| Windows logs received in Splunk | Successful |

## Important Ports

| Port | Service | Purpose |
|---|---|---|
| 8000 | Splunk Web | Access Splunk web interface |
| 9997 | Splunk Receiving | Receive logs from Universal Forwarder |

## Screenshots

Screenshots to be added:

- Ubuntu Server VM settings
- Ubuntu Server IP configuration
- Splunk web login page
- Splunk receiving port configuration
- Windows logs visible in Splunk

## Notes
Ubuntu Server is used as the SIEM host in this lab. Splunk Enterprise runs on this server and provides the main platform for log ingestion, searching, and future detection use cases.
