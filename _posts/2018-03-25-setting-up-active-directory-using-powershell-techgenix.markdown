---
layout: post 
title:  "Setting up Active Directory using PowerShell - TechGenix" 
date:   2018-03-25T15:22:14.806Z 
categories: powershell activedirectory automation
link: http://techgenix.com/setting-up-active-directory/ 
tags:
  - links
ogtype: article 
---

> SETTING UP ACTIVE DIRECTORY USING POWERSHELL

Nirmal Sharma FEBRUARY 13, 2018 0 396 Views
SHARE ON FACEBOOK
 
TWEET IT
 
 
 
 

PowerShell is an extremely powerful set of command line tools you can use to manage different aspects of a Windows environment. Most of the roles and features ship with the required PowerShell cmdlets to perform management tasks. For example, complete Windows Failover cluster operation can be managed using the Failover PowerShell cmdlets. Similarly, Active Directory instances can be managed using the Active Directory PowerShell cmdlets. This article focuses on setting up Active Directory domain controllers using the PowerShell commands that ship with Active Directory PowerShell Modules.

Requirements for setting up Active Directory using PowerShell
Before you start to execute any PowerShell commands explained in this article, install Active Directory PowerShell modules on a Windows Server 2012 or later or Windows 10 operating systems. Also, make sure you have administrator privileges to perform the required operation. For example, when installing a domain controller in an Active Directory domain, you would be required to have domain admin credentials. Once you have met these requirements, proceed with the next sections of this article, which explains the necessary steps before implementing a domain controller such as running a health check and how to use PowerShell commands to perform a prerequisite check before installing the domain controller.