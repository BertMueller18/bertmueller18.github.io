---
layout: post 
published: true 
title: "Deploy WMF5.0 on Windows 7 | &gt;_" 
date: 2016-08-23T13:39:56.071Z 
link: https://p0w3rsh3ll.wordpress.com/2016/05/17/deploy-wmf5-0-on-windows-7/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Deploy WMF5.0 on Windows 7
Posted on May 17, 2016
When the WMF5.0 was republished, I’ve asked the following question in the comments

Can you please explain why WMF 4.0 is a prerequisite on Windows Server 2008 R2 and Windows 7 SP1? Is it related to the WMI repository and/or to DSC?

Krishna C Vutukuri from the Windows PowerShell Team replied

As you may know, WMF 5 uses CBS based technology for installation. Win 7 SP1/W2K8R2 systems contain PowerShell 2.0, WinRM, WMI by default. After Win7/W2K8 R2 released, we shipped WMF 3.0 and WMF 4.0 which contain updates to these features. Installing / Uninstalling these packages uncovered some issues in the upgrade options from inbox -> WMF4 and inbox->WMF3->WMF4. We fixed all those issues in WMF4. Hence we had to make WMF4 as requirement for installing WMF5 on Win7 SP1/W2K8 R2. Here are the specific issues you might face if you do not install WMF4 before upgrading to WMF5:

(a) Forwarded Events log is unavailable and EventCollector log is not displayed in Event Viewer after you uninstall in Windows 7 SP1 and in Windows Server 2008 R2 SP1
(b) Issues with PSModulePath environment when you upgrade directly from inbox to WMF5 or from WMF 3 to WMF5.

Again WMF4 addresses these issues and our internal testing environment uses this matrix for testing WMF5 on Win7 SP1/W2K8R2 SP1.