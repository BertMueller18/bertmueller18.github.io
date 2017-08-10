---
layout: post
title:  "ESXi 5.5 – Automating VMFS UNMAP w/ PowerCLI and PowerShell – Pragmatic IO"
date:   2017-01-01T13:32:04.837Z
categories: vmware powercli powershell
link: http://www.pragmaticio.com/2016/12/esxi-5-5-automating-vmfs-unmap-w-powercli-and-powershell/?utm_source=ReviveOldPost&utm_medium=social&utm_campaign=ReviveOldPost
tags:
  - links
ogtype: article
---

## ESXi 5.5 – Automating VMFS UNMAP w/ PowerCLI and PowerShell
 Brett Sinclair    December 4, 2016    No Comments on ESXi 5.5 – Automating VMFS UNMAP w/ PowerCLI and PowerShell
With vSphere 6.5 recently released, a nice feature was the automated execution of the UNMAP command against thin provisioned datastores to reclaim space. This requires no user interaction, it’s fully automated for you and can free up significant amounts of space from your datastores.

There’s some good information regarding the v6.5 release  on these blogs;

ESX Virtualization Vladan Seget

VirtualizationIsLife  Anthony Spiteri

But you don’t necessarily have to upgrade to 6.5 to avail yourself of this cool enhancement, it’s possible, with a little effort to get it working in your existing environment, as long as you are running Esxi 5.5 or 6.0x.
