---
layout: post 
title:  "Building Hyper-V lab environments based on PowerShell DSC" 
date:   2017-07-21T14:47:03.728Z 
categories: powershell automation deployment
link: http://www.powershell.no/hyper-v,/powershell/dsc/2017/07/19/lability.html 
tags:
  - links
ogtype: article 
---

## Building Hyper-V lab environments based on PowerShell DSC
Jul 19, 2017

In this article we will look at how the PowerShell Desired State Configuration (DSC) feature in Windows PowerShell can be leveraged for building lab environments. If you are unfamiliar with DSC, have a look at the DSC overview page on MSDN. As stated there: DSC provides a set of Windows PowerShell language extensions, new Windows PowerShell cmdlets, and resources that you can use to declaratively specify how you want your software environment to be configured.

Background

PowerShell DSC was first released back in 2014 integrated in PowerShell 4.0 as part of the Windows Server 2012 R2 release. Since then, it has first and foremost been leveraged in Windows-based server deployments. However, now that PowerShell is open sourced and available on Linux, it means that DSC is also available on that platform. It can also be leveraged on Nano Server (Microsoft’s container optimized operating system) and Windows Containers, thus it is clearly an important part of Microsoft`s strategy going forward. There is also a number of creative community projects leveraging DSC, one of them which we are going to look at in this article. Imagine if we could leverage the same configuration data structure as DSC for other purposes, such as building a lab environment. At the end, the configuration structure is “just” a PowerShell hash table which can optionally be stored in a PowerShell data file (psd1). This is exactly what the community based Lability module does, in addition to leveraging DSC for configuring the virtual machines being created. The module is specifically written for the Hyper-V virtualization platform, but parts of it can be leveraged in other environments as-is. The module leverages the concept of injecting DSC configurations into the virtual machines hard disk file, typically a VHD or VHDX file. This concept is explained and demonstrated in detail in this Channel 9 video.