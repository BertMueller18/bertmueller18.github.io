---
layout: post 
title:  "How To Create and Invoke Your First DSC Configuration in Azure -- Microsoft Certified Professional Magazine Online" 
date:   2018-03-25T15:18:29.624Z 
categories: azure powershell powershelldsc automation
link: https://mcpmag.com/articles/2018/02/14/dsc-configuration-in-azure.aspx 
tags:
  - links
ogtype: article 
---

> How To Create and Invoke Your First DSC Configuration in Azure
Using Azure Automation DSC gives administrators the same benefits of PowerShell DSC, but with some bonus tooling.

By Adam Bertram02/14/2018
Introduced with PowerShell v4, Desired State Configuration (DSC) was a significant shift in the way that changes are made with PowerShell. Administrators now could declare configuration declaratively rather than procedurally to make changes to their environment.

Although DSC is a powerful tool, Microsoft didn't include much tooling around it. Microsoft has traditionally said that DSC is a platform, rather than a toolset.

Microsoft recognized the benefit, however, of DSC and saw that this technology could be leveraged in the cloud with Azure. Although PowerShell DSC wouldn't work quite right in Azure, another team took on the responsibility to create a different "version" of DSC called Azure Automation DSC. This DSC implementation would provide the same benefits of PowerShell DSC but also give administrators some tooling around DSC such as the pull server.

Integrating DSC into Azure and creating some management tooling around it transformed DSC into something that was easier to use and worked great in the Azure cloud environment.