---
layout: post 
title:  "DHCP &amp; PXE Test Client - In PowerShell - WTF! - 2Pint Software" 
date:   2017-06-15T09:03:33.519Z 
categories: powershell pxe 
link: https://2pintsoftware.com/dhcp-pxe-test-powershell/ 
tags:
  - links
ogtype: article 
---

> DHCP & PXE Test Client – In PowerShell – WTF!

Had a thought the other day, why do I have to keep PXE booting these devices just to see what file name and other options, if any, I would get from my DHCP, proxyDHCP or IP Relay/Forwarding devices. Surely there must be a PowerShell script that lets you do that? Well there wasn’t. I did find one epic PowerShell script written by a dude called Chris Dent, which was simulating a DHCP client. Close enough, so I did some rework on it to make sure it covered the basic PXE bits as well. Great work BTW Chris!

The PXE Fairy and how she works her magic

So in order to PXE boot a modern client, the standard can be deviated and bastardised quite a bit but will only cover the basics here, typically has to set the following options:

Option 60: This gets set to the string of “PXEClient” which then instructs the PXE servers that this is a machine that is trying to boot.

Option 93: This is set to the actual UUID of the machine

Option 97: Contains some information of what kind of machine it is, like UEFI or not etc.

Okay, so what does it look like?