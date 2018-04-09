---
layout: post 
title:  "How-to – Load Remote Exchange PowerShell Session on Exchange 2010, 2013, 2016, Exchange Online (O365) – which ports do you need – Microsoft Exchange pour Tous V2 – Microsoft Exchange made simple" 
date:   2018-04-09T20:49:03.207Z 
categories: powershell remoting exchange o365 office365
link: https://blogs.technet.microsoft.com/samdrey/2018/04/06/how-to-load-remote-powershell-session-on-exchange-2010-2013-2016-exchange-online-o365-2/ 
tags:
  - links
ogtype: article 
---

> How-to – Load Remote Exchange PowerShell Session on Exchange 2010, 2013, 2016, Exchange Online (O365) – which ports do you need
★★★★★★★★★★★★★★★
SammyKrosoftApril 6, 20180 
0
0
1-Intro

In a previous blog post, I exposed the trick to load the Exchange Management Shell on ISE, the Integrated Scripting Environment of PowerShell, just like the Exchange Management Shell shortcut that is installed when you install the Exchange Management Tools. That trick needed the Exchange Management Tools to be installed locally, which is not bad as your ISE will behave exactly like your Exchange Management Shell, but with the benefits of the ISE.

Now, and as George highlighted in a comment in this previous blog post's comments section, you can also load Exchange cmdlets from a remote PowerShell session, using New-PSSession and Import-PSSession. Note that not all Exchange cmdlets and functions are available using that way (what you "lose" is a topic for a future blog post but basically you can just compare Exchange cmdlets list side by side after dumping these using "get-excommand")

As mentioned in the same previous blog post, that PowerShell session import method has its own advantages, like the ability to load Exchange management cmdlets to any workstation or server that has PowerShell and the proper ports opened, without the need to install the Exchange Management Shell. It can be very useful for your applications relying on Exchange Powershell cmdlets for example…

Below I pasted the PowerShell snippets to connect to your Exchange platform (Exchange 2010, 2013, 2016 and Exchange Online), along with the related TechNet links if you need or want more details.

 