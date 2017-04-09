---
layout: post 
title:  "Get Hyper-V guest serial number with PowerShell - PowerShell - Sysadmins of the North" 
date:   2017-04-09T08:42:36.763Z 
categories: hyper-v powershell
link: https://www.saotn.org/get-hyper-v-guest-serial-number-with-powershell/?utm_source=reddit&utm_medium=website&utm_term&utm_content=redditlink&utm_campaign=social 
tags:
  - links
ogtype: article 
---

> Get Hyper-V guest serial number with PowerShell
Reading Time: 2 Minutes
Click to share on Facebook (Opens in new window)Click to share on Twitter (Opens in new window)Click to share on Google+ (Opens in new window)Click to share on LinkedIn (Opens in new window)Click to share on Telegram (Opens in new window)Click to share on WhatsApp (Opens in new window)Click to share on Pocket (Opens in new window)Click to email this to a friend (Opens in new window)
Retrieve the Hyper-V virtual machine’s serial number with PowerShell. Sometimes you need to have the serial number of a Hyper-V virtual machine (VM, or guest). We, for instance, use this serial number in our automatic, unattended deployment of the guest operating system. But then you need to know how to find this serial number…


And that’s where PowerShell comes in. The following PowerShell snippets print out all virtual machines on a Hyper-V server, with the Hyper-V serial numbers (a.k.a BIOSSerialNumber) for the VM’s:

Advertisement:
Get-WmiObject -ComputerName hyper-v_server -Namespace ` 
root\virtualization\v2 -class Msvm_VirtualSystemSettingData `
| select elementname, BIOSSerialNumber
Note: To use this PowerShell snippet on the PowerShell command line, remove the backticks (`) and place the command on one line.

The output is:

elementname  BIOSSerialNumber
-----------  ----------------
hyperv-vm-01 1111-2222-3333-4444-5555-6666-77
hyperv-vm-02 1112-2223-3334-4445-5556-6667-77
This PowerShellcode utilizes the Get-WmiObject Cmdlet. System administrators will likely rely heavily on Get-WmiObject to help them with their routine management tasks. Because at this time there are only a few cmdlets designed for carrying out system administration tasks (Get-Process, Get-Service, and Get-EventLog).

You can see Get-Service in action when monitoring Windows services with PowerShell.

The Hyper-V virtual machine’s instance ID (GUID) is retrieved requesting InstanceID:

Get-WmiObject -ComputerName hyper-v_server -Namespace ` 
root\virtualization\v2 -class Msvm_VirtualSystemSettingData `
| select elementname, InstanceID