# Enterprise Security Lab

## Overview
This project documents an enterprise-style cybersecurity home lab built using VMware Workstation. The lab is designed to simulate a small corporate network with firewall routing, Active Directory, endpoint logging, SIEM monitoring, and basic attack/testing workflows.

## Lab Objectives
- Build a virtual enterprise network from scratch
- Configure pfSense as the main firewall and router
- Set up Windows Server with Active Directory Domain Services (AD DS)
- Connect Windows endpoints to the internal lab network
- Forward Windows event logs to Splunk
- Use Kali Linux for controlled security testing
- Practice SOC analyst and blue team investigation workflows

## Project Structure

```text
enterprise-security-lab/
├── active-directory/     # Active Directory setup, domain configuration, and related documentation
├── docs/                 # General project documentation
├── kali/                 # Kali Linux testing notes and attack simulation documentation
├── network-diagrams/     # Network topology diagrams and architecture visuals
├── pfsense/              # pfSense firewall configuration and routing documentation
├── screenshots/          # Screenshots captured during lab setup and testing
├── splunk/               # Splunk setup, searches, dashboards, and log analysis notes
└── README.md             # Main project overview
```

## Lab Environment
| Component | Purpose |
|---|---|
| VMware Workstation | Virtualization platform |
| pfSense | Firewall, routing, and network segmentation |
| Windows Server | Active Directory domain controller |
| Windows 10 | Domain-joined endpoint / test workstation |
| Kali Linux | Security testing machine |
| Ubuntu Server | Splunk Enterprise server |
| Splunk Universal Forwarder | Windows log forwarding agent |

## Network Design
| System | IP Address | Role |
|---|---|---|
| pfSense LAN | 10.0.0.1 | Default gateway / firewall |
| Windows 10 VM | 10.0.0.2 | Endpoint |
| Windows Server | 10.0.0.3 | Domain Controller |
| Kali Linux | 10.0.0.4 | Attack/testing machine |
| Ubuntu Server | 10.0.0.5 | Splunk SIEM |

## Current Progress
- Created VMware-based lab environment
- Installed and configured pfSense firewall
- Configured internal LAN network
- Installed Windows Server and Active Directory
- Joined Windows 10 VM to the domain
- Installed Kali Linux for testing
- Installed Splunk Enterprise on Ubuntu Server
- Configured Splunk Universal Forwarder on Windows
- Verified Windows event log forwarding into Splunk

## Skills Demonstrated

| Skill Area | Skills Practiced |
|---|---|
| Virtualization | VMware Workstation, multi-VM lab design, virtual networking |
| Network Security | pfSense firewalling, routing, gateway configuration, network segmentation |
| Windows Administration | Windows 10 endpoint setup, Windows Server configuration, domain join |
| Identity & Access | Active Directory Domain Services, domain authentication, centralized user management |
| SIEM & Logging | Splunk Enterprise, Universal Forwarder, Windows event log ingestion |
| SOC Analysis | Security event review, failed login analysis, authentication monitoring |
| Offensive Security Awareness | Kali Linux testing, Nmap scanning, basic enumeration |
| Documentation | Technical documentation, network topology, screenshot tracking, project structure |

## Screenshots
Screenshots will be added as the lab progresses.

## Disclaimer
This lab is for educational and professional development purposes only. All testing is performed in an isolated virtual environment.
