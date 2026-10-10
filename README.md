# Windows Server Active Directory Home Lab

![Windows Server](https://img.shields.io/badge/Windows%20Server-2022-blue)
![Active Directory](https://img.shields.io/badge/Active%20Directory-AD%20DS-blue)
![Windows 11](https://img.shields.io/badge/Windows-11-blue)
![DNS](https://img.shields.io/badge/DNS-Configured-blue)
![Group Policy](https://img.shields.io/badge/Group%20Policy-GPO-blue)

## Introduction

This project is a hands-on Windows Server 2022 Active Directory home lab built using Oracle VirtualBox. The goal of the lab was to practice common IT support and system administration tasks in a Windows domain environment.

Throughout the project, I configured Active Directory Domain Services, DNS, organizational units, users, security groups, a domain-joined Windows 11 client, file sharing and permissions, Group Policy, and common help desk tasks.

This lab also gave me experience troubleshooting networking, authentication, permissions, and domain connectivity issues.

## Lab Environment
<img width="607" height="305" alt="Screenshot 2026-04-03 130722" src="https://github.com/user-attachments/assets/3973dd93-f3fd-4b7c-a64e-b3b0407895d3" />  

- **Hypervisor:** Oracle VirtualBox
- **Server OS:** Windows Server 2022
- **Client OS:** Windows 11
- **Domain:** `mylab.local`
- **Server Roles:** Active Directory Domain Services (AD DS), DNS
- **Client Computer:** `ITPC1`

## Project Documentation

### [01 - Server Manager](01_ServerManager.md)
Windows Server setup, installation of Active Directory Domain Services, DNS, and domain controller configuration.

### [02 - Organizational Units, Users, and Security Groups](02-CreatingUsersAndOrganizationUnits.md)
Creation of department OUs, user accounts, and security groups for IT, HR, Engineering, and Sales.

### [03 - Domain Join and Computer Management](03-DomainJoinAndComputerManagement.md)
Windows 11 networking, DNS configuration, domain joining, authentication testing, and management of the `ITPC1` computer object.

### [04 - File Sharing and Permissions](04-FileSharingAndPermissions.md)
Creation of department shared folders, SMB share permissions, NTFS permissions, and allowed/denied access testing.

### [05 - Help Desk Tasks](05-HelpDeskTasks.md)
Password resets, account disabling and re-enabling, password changes, account lockouts, and authentication troubleshooting.

### [06 - Group Policy](06-GroupPolicy.md)
Creation and management of Group Policy Objects, account lockout settings, and the IT Workstation Policy.

## Skills Demonstrated

- Windows Server 2022
- Active Directory Domain Services
- DNS
- Organizational Units
- User Account Management
- Security Groups
- Windows Domain Authentication
- Domain Joining
- Group Policy
- SMB File Sharing
- NTFS Permissions
- Help Desk Troubleshooting
- Network Troubleshooting
- Oracle VirtualBox

## What I Learned

This lab helped me understand how Active Directory, DNS, users, groups, computers, permissions, and Group Policy work together in a Windows domain environment. I also gained hands-on experience troubleshooting authentication, networking, and file access issues. Overall, the project helped me build practical skills related to Help Desk, IT Support, and junior system administration roles.
