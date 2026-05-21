# Network Topology

## Overview
This document describes the network topology used in the Enterprise Security Lab. The lab is designed to simulate a small enterprise network using VMware Workstation, pfSense, Windows systems, Kali Linux, and Splunk.

## Network Summary

| Network | Purpose |
|---|---|
| VMware NAT | Provides internet access to pfSense WAN |
| Internal Lab Network | Main isolated lab network for virtual machines |
| Host-Only Network | Management access from host machine to pfSense |

## IP Addressing

| System | IP Address | Role |
|---|---|---|
| pfSense LAN | 10.0.0.1 | Firewall / Default Gateway |
| Windows 10 VM | 10.0.0.2 | Domain-joined endpoint |
| Windows Server | 10.0.0.3 | Domain Controller |
| Kali Linux | 10.0.0.4 | Security testing machine |
| Ubuntu Server | 10.0.0.5 | Splunk SIEM server |
| pfSense Management | 172.16.0.2 | Host-only management access |

## Logical Network Diagram

```text
Internet
   |
VMware NAT Network
   |
pfSense Firewall
   |
Internal Lab Network - 10.0.0.0/24
   |
   |-- Windows 10 VM - 10.0.0.2
   |-- Windows Server / Domain Controller - 10.0.0.3
   |-- Kali Linux - 10.0.0.4
   |-- Ubuntu Server / Splunk - 10.0.0.5

Host Machine
   |
Host-Only Network - 172.16.0.0/16
   |
pfSense Management Interface - 172.16.0.2
```

## Traffic Flow

| Source | Destination | Purpose |
|---|---|---|
| Windows 10 VM | pfSense | Default gateway traffic |
| Windows 10 VM | Windows Server | Domain authentication and DNS |
| Windows 10 VM | Ubuntu Splunk Server | Log forwarding |
| Kali Linux | Internal lab systems | Controlled testing and enumeration |
| Host Machine | pfSense Management Interface | Firewall administration |

## Design Notes

- pfSense acts as the central firewall and router for the lab.
- All internal lab systems use `10.0.0.1` as the default gateway.
- Windows Server provides Active Directory and DNS services.
- Windows 10 acts as the primary domain-joined endpoint.
- Ubuntu Server hosts Splunk Enterprise.
- Kali Linux is used only for controlled testing inside the lab.
- Host-only management access allows the host machine to access pfSense directly.

## Screenshots / Diagrams

Screenshots and visual diagrams to be added:

- VMware virtual network settings
- pfSense interface assignments
- pfSense dashboard
- Windows 10 IP configuration
- Windows Server IP configuration
- Splunk server IP configuration
- Full network diagram image
