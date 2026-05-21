# pfSense Firewall Setup

## Overview
This document covers the pfSense firewall setup used in the Enterprise Security Lab. pfSense is used as the main firewall and default gateway for the internal lab network.

## Purpose
The purpose of pfSense in this lab is to:

- Route traffic between the internal lab network and the internet
- Act as the default gateway for lab machines
- Provide firewall control for the virtual environment
- Simulate an enterprise-style perimeter firewall

## Lab Network Configuration

| Interface | Network | IP Address | Purpose |
|---|---|---|---|
| WAN | VMware NAT | DHCP | Internet access |
| LAN | Internal lab network | 10.0.0.1 | Default gateway for lab VMs |
| Management | Host-only network | 172.16.0.2 | Direct access from host machine |

## Completed Configuration

- Installed pfSense as a virtual machine in VMware Workstation
- Assigned network adapters for WAN, LAN, and management access
- Configured LAN IP address as `10.0.0.1`
- Configured management access through host-only network
- Verified pfSense web interface access from Windows 10 VM
- Confirmed internet connectivity from the internal lab network

## Verification

The following checks were completed:

| Test | Result |
|---|---|
| Access pfSense web GUI from Windows 10 VM | Successful |
| Ping pfSense LAN IP `10.0.0.1` | Successful |
| Internet access from Windows 10 VM | Successful |
| pfSense acting as default gateway | Successful |

## Screenshots

Screenshots to be added:

- pfSense VM settings
- pfSense interface assignments
- pfSense dashboard
- Windows 10 VM accessing pfSense web GUI
- Windows 10 VM internet connectivity test

## Notes
pfSense is the central network device in this lab. All internal lab machines are placed behind pfSense to simulate a controlled enterprise network environment.
