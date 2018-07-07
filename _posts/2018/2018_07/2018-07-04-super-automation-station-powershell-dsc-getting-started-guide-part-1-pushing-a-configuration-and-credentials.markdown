---
layout: post 
title:  "Super Automation Station: PowerShell DSC Getting Started Guide - Part 1, Pushing a configuration and Credentials" 
date:   2018-07-03T22:03:33.059Z 
categories: psdsc powershell dsc howto
link: https://blog.superautomation.co.uk/2016/12/powershell-dsc-getting-started-guide.html 
tags:
  - links
ogtype: article 
---

> Super Automation Station
Powershell, Automation and Infrastructure.

Saturday, 3 December 2016
PowerShell DSC Getting Started Guide - Part 1, Pushing a configuration and Credentials
Part 1 - Pushing a configuration and Credentials
Part 2 - Pull Server Setup
Part 3 - Custom Scripts
Part 4 - Partial Configurations.

What is PowerShell DSC

PowerShell DSC - Desired State Configuration - is a declarative platform for provisioning Windows (and non Windows) machines with configuration information. Under the covers, there is PowerShell code which enforces the configuration on the machine.

PowerShell DSC can be used to install and configure software and enforce configuration of the Operating System.

PowerShell DSC is idempotent, which means a configuration can be run against a machine over and over and if the machine is already in the described state, then nothing will be changed.

Included in-box are 'modules' which contain 'resources' that allow installation of packages and Windows features, copying of files and folders, ensuring registry entries are set to specific values and more.