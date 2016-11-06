---
layout: post 
published: true 
title: "PowerShell Script: Deploy VMs and Configure Guest OS in Hyper-V" 
date: 2016-09-26T19:26:50.245Z 
link: http://www.altaro.com/hyper-v/powershell-script-deploy-vms-configure-guest-os-one-go/?utm_content=buffer9422d&utm_medium=social&utm_source=linkedin.com&utm_campaign=buffer 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> PowerShell Script: Deploy VMs, and Configure the Guest OS in one Go on Hyper-V
 20 Sep 2016 by Andy Syrewicze    0     Hyper-V & PowerShell
Rate this (2 Votes)
 
I’ve been prepping for a lot of different speaking engagements coming up in the next few months and a very hot topic these days is the use of PowerShell and automation, when it comes to Hyper-V. With this in mind, I’ve prepped the below script for some of these upcoming discussions, and wanted to share it with the community so that it’ll be of help to some people.

The Story
Awhile back, I spoke at a VMware VMUG event where I talked about advanced VM provisioning using PowerCLI and templates. In that talk, I taught the group how to provision a virtual machine using the shell, and then reach into the VM and execute a number of commands against the guest OS to achieve even greater amounts of automation and followed up by posting the script HERE.

Well, I wanted to take the goal from that script and apply it to a Hyper-V environment using PowerShell Direct. For those that aren’t aware, PowerShell Direct is a new feature in the Windows Server 2016 feature set, that allows us to inject PowerShell commands into the guest OS of a running VM, without the network for networking. Without getting too into the specifics, it does this via the VMbus on the Hyper-V host, and it works VERY well.