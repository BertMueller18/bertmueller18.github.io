---
layout: post
published: true
title: "Remote PowerShell Proxying Behavior in Exchange 2013 CU12 and Exchange 2016 – You Had Me At EHLO…"
date: 2016-10-12T20:37:34.429Z
categories: exchange exchange2013
link: https://blogs.technet.microsoft.com/exchange/2016/03/01/remote-powershell-proxying-behavior-in-exchange-2013-cu12-and-exchange-2016/
tags:
  - links
ogtype: article
bodyclass: post
---

> Remote PowerShell Proxying Behavior in Exchange 2013 CU12 and Exchange 2016
★★★★★★★★★★★★★★★
Ross Smith IVMarch 1, 20167
0
22
0
In Exchange 2013 CU11, we introduced a change to the way Remote PowerShell (RPS) functioned.

Prior to CU11, Exchange 2013 routed Remote PowerShell requests by finding a random mailbox that is either higher than the ExchClientVer that is specified in the URL, or if the ExchClientVer is not specified, by using the current CAS version in which the client connected. We refer to this behavior as server version-based routing.

With CU11, we changed Remote PowerShell to route requests to an anchor mailbox. Typically, this anchor mailbox would be the mailbox of the user attempting the connection. In the event the user attempting the connection did not have a mailbox, the request would be routed to the organization arbitration mailbox.
