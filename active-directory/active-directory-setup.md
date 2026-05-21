# Active Directory Setup

## Overview
This document covers the Active Directory setup used in the Enterprise Security Lab. Windows Server is used as the domain controller to simulate a small enterprise identity environment.

## Purpose
The purpose of Active Directory in this lab is to:

- Simulate centralized user and computer management
- Create a domain-based Windows environment
- Practice domain-joined endpoint administration
- Generate realistic Windows authentication events for Splunk analysis
- Support future SOC investigation and detection scenarios

## Lab Configuration

| Component | Configuration |
|---|---|
| Server OS | Windows Server |
| Role | Domain Controller |
| Domain | Lab.local |
| IP Address | 10.0.0.3 |
| Default Gateway | 10.0.0.1 |
| DNS | Domain Controller / AD DNS |

## Completed Configuration

- Installed Windows Server as a virtual machine in VMware Workstation
- Configured static IP address `10.0.0.3`
- Installed Active Directory Domain Services (AD DS)
- Promoted the server to a domain controller
- Created the domain `Lab.local`
- Configured Windows 10 VM to use the domain controller for DNS
- Joined Windows 10 VM to the `Lab.local` domain
- Verified domain login from the Windows 10 VM

## Verification

| Test | Result |
|---|---|
| Windows Server reachable from lab network | Successful |
| Domain `Lab.local` created | Successful |
| Windows 10 VM joined to domain | Successful |
| Domain login tested from Windows 10 VM | Successful |
| AD environment ready for log generation | Successful |

## Screenshots

Screenshots to be added:

- Windows Server static IP configuration
- Server Manager AD DS role installation
- Domain controller promotion screen
- Active Directory Users and Computers
- Windows 10 domain join confirmation
- Domain login screen

## Notes
Active Directory provides the identity layer for this lab. It allows the environment to generate realistic authentication, login, and domain-related security events that can later be forwarded to Splunk for SOC-style analysis.
