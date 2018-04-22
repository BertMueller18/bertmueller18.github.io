---
layout: post 
title:  "	A Step by Step Guide to Connecting to an Azure Virtual Machine with PowerShell Remoting | endjin blog	" 
date:   2018-04-21T11:25:58.781Z 
categories: powershell remoting azure azurerm
link: https://blogs.endjin.com/2014/03/a-step-by-step-guide-to-connecting-to-an-azure-virtual-machine-with-powershell-remoting/ 
tags:
  - links
ogtype: article 
---

> A Step by Step Guide to Connecting to an Azure Virtual Machine with PowerShell Remoting
March 25, 2014 by Howard van Rooijen
Any person tasked with looking after a number of Windows Servers knows that Remote Desktop will only scale so far and that at some point you will need to turn to scripting to manage a server estate of any reasonable size. Two years ago I blogged “An Omega Geek’s Guide to Learning PowerShell“, so it should be pretty obvious what my weapon of choice is.

Theoretically, connecting to an Azure Virtual Machine via PowerShell Remoting should be relatively straight forward, as Windows Server 2012 R2 enables PowerShell Remoting by default and Azure exposes a remoting endpoint by default.  I wanted to script some changes to a TeamCity based Continuous Integration Environment (see my whitepaper for JetBrains “From Chaos, through Fear, to Confidence” for more information), and found that in practice it was actually a tad more involved.

Firstly, you nee