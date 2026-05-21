# Kali Linux Setup

## Overview
This document covers the Kali Linux setup used in the Enterprise Security Lab. Kali Linux is used as the security testing machine for controlled testing inside the virtual lab environment.

## Purpose
The purpose of Kali Linux in this lab is to:

- Perform controlled security testing
- Validate firewall and network visibility
- Test connectivity to internal lab systems
- Generate security events for Splunk analysis
- Practice basic reconnaissance and enumeration techniques

## Lab Configuration

| Component | Configuration |
|---|---|
| Operating System | Kali Linux |
| Platform | VMware Workstation |
| IP Address | 10.0.0.4 |
| Default Gateway | 10.0.0.1 |
| Network | Internal lab network |
| Purpose | Security testing machine |

## Completed Configuration

- Installed Kali Linux as a virtual machine in VMware Workstation
- Connected Kali Linux to the internal lab network
- Configured network connectivity through pfSense
- Verified access to internal lab systems
- Used Kali Linux for basic network testing and enumeration
- Generated test activity for future Splunk analysis

## Verification

| Test | Result |
|---|---|
| Kali Linux VM installed | Successful |
| Connected to internal lab network | Successful |
| pfSense reachable from Kali Linux | Successful |
| Internal systems reachable from Kali Linux | Successful |
| Kali ready for controlled testing | Successful |

## Tools Used

| Tool | Purpose |
|---|---|
| ping | Basic connectivity testing |
| nmap | Network scanning and service discovery |
| rpcclient | Active Directory enumeration testing |

## Screenshots

Screenshots to be added:

- Kali Linux VM settings
- Kali Linux IP configuration
- Ping test to pfSense
- Nmap scan results
- rpcclient enumeration results

## Notes
Kali Linux is used only within the isolated lab environment. All testing is performed against lab-owned virtual machines for learning and professional development purposes.
