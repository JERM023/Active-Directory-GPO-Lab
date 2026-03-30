# Active-Directory-GPO-Lab
Configured an Active Directory lab environment and implemented Group Policy to manage user restrictions. Troubleshot domain logon issues and applied OU-based GPO targeting.

### Active Directory GPO Lab

## Overview

This project demonstrates the setup of an Active Directory environment and the implementation of Group Policy Objects (GPOs) to control user permissions.

The lab includes creating users, organizing them into Organizational Units (OUs), applying GPOs, and troubleshooting real-world domain issues.
---
## Environment

- Windows Server (Domain Controller)
- Active Directory Domain Services (AD DS)
- Group Policy Management
- VirtualBox
---
## Objectives
- Create and manage Active Directory users
- Organize users using Organizational Units (OUs)
- Apply Group Policy to restrict user access
- Troubleshoot domain login and policy issues
---
## Steps Performed

## 1. User Creation
- Created a domain user (john)
- Configured password settings

## 2. Organizational Unit (OU)
- Created an OU named TestUsers
- Moved user into OU for policy targeting

## 3. Group Policy Configuration
- Created GPO: Block Control Panel
- Linked GPO to TestUsers OU
- Enabled:
Prohibit access to Control Panel and PC settings

## 4. Policy Deployment
- Applied policy using: 
gpupdate /force

- Verified functionality by testing user restrictions
---
### Troubleshooting (Key Learning)

Encountered an issue where domain users could not log in.

# Root Cause:
- Misconfigured logon rights in Default Domain Controllers Policy

## Resolution:
- Modified:

- Allow log on locally → added Domain Users
- Cleared Deny log on locally

- Forced policy update and rebooted system
---
### Results
- Successfully restricted Control Panel access for targeted users
- Maintained proper domain functionality
- Resolved domain-level authentication issue
---
### Key Skills Demonstrated
- Active Directory administration
- Group Policy management
- Troubleshooting domain login issues
- OU-based policy scoping
- Windows Server environment setup
