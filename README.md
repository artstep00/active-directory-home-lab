# Active-Directory-Home-Lab
Windows Active Directory home lab demonstrating AD DS, DNS, OU design, domain joins, Group Policy, and PowerShell administration.
# Windows Active Directory Home Lab

## Overview

This project documents the design and implementation of a Windows Active Directory home lab using Microsoft Hyper-V.

The lab was built to gain hands-on experience with enterprise Windows administration, including:

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- DNS
- Organizational Units (OUs)
- User and security group administration
- Windows 11 domain joining
- Group Policy
- PowerShell
- Hyper-V networking

The environment consists of a Windows Server 2025 domain controller and a Windows 11 client connected through a private Hyper-V NAT network.

## Lab Environment

| System | Operating System | IP Address | Purpose |
|---|---|---|---|
| DC01 | Windows Server 2025 | 192.168.100.10 | Domain Controller, AD DS, DNS |
| CLIENT01 | Windows 11 Enterprise | 192.168.100.11 | Domain-joined workstation |

### Network Configuration

- Network: `192.168.100.0/24`
- Default Gateway: `192.168.100.1`
- Domain: `lab.example.com`
- NetBIOS Domain: `LAB`
- DNS Server: `192.168.100.10`

## Project Goals

The goals of this lab are to:

- Deploy and configure a Windows Server domain controller
- Configure Active Directory-integrated DNS
- Create and organize users, groups, and computer objects
- Join Windows clients to an Active Directory domain
- Apply and verify Group Policy
- Practice Windows administration with PowerShell
- Document troubleshooting and validation steps

## 1. DC01 Network Configuration

Configured DC01 with a static IPv4 address in order to assure domain controller and DNS server would always be reachable at a predictable address.

- IP Address: '192.168.100.10'
- Subnet: '192.168.100.0/24'
- Default Gateway: '192.168.100.1'
- DNS: configured for external resolution prior to promoting DC01 to a DNS server

Verified network connectivity and DNS resolution using Powershell.
