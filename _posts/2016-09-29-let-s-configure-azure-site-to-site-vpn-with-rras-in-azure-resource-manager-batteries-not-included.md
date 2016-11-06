---
layout: post 
published: true 
title: "Let’s Configure Azure Site-to-Site VPN with RRAS in Azure Resource Manager! – Batteries Not Included" 
date: 2016-09-29T20:38:41.596Z 
link: https://blogs.technet.microsoft.com/jletsch/2016/03/15/lets-configure-azure-site-to-site-vpn-with-rras-in-azure-resource-manager/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> 
Let’s Configure Azure Site-to-Site VPN with RRAS in Azure Resource Manager!
★★★★★★★★★★★★★★★
JLetschMarch 15, 201622
0
0
0
There are several blog posts about configuring an Azure site-to-site VPN with Microsoft RRAS in the old Azure portal.  I did find that Cheryl McGuire wrote an article about creating a site-to-site VPN in Azure Resource Manager with PowerShell here. However this post is more specific about configuring RRAS and Azure site-to-site VPN.

In the old Azure portal once you configured a site-to-site VPN it would generate a script that would configure RRAS on a Windows Server.  I have not been able to find where or even if that script is created in the new Azure portal.  So we are going to manually configure RRAS.

NOTE: In this post I will be disabling IPv6 because it is not used.

Before you begin you will need a Windows Server 2012 R2 that has 2 NICs.