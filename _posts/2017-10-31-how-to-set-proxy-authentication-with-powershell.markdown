---
layout: post 
title:  "How to set proxy authentication with PowerShell" 
date:   2017-10-31T10:49:27.927Z 
categories: powershell proxy
link: http://www.networkadm.in/how-to-set-proxy-authentication-with-powershell/ 
tags:
  - links
ogtype: article 
---

> How to set proxy authentication with PowerShell
11 OCTOBER 2017 by Mike Kanakos
I have struggled in the past to get my PowerShell sessions to connect online at work because my employer uses ZScaler as our web proxy. For those unfamiliar with ZScaler, it is an off-prem (cloud-based) proxy that requires authentication. Our proxy settings are configured via GPO which points to a PAC file set in the IE control panel.

For most things, it just works because most apps these days just pick up the IE control settings and away we go. But not so much with PowerShell...

So after much googling, I came across a blog post from a blogger in Europe named the "Angry Admin". His solution was spot on!

I have posted the code here and modified it with the proxy address for one of the Zscaler web proxies based on the US east coast. You can modify my code with another cloud-based proxy and it should work without any issues.

You can save this to your PowerShell profile or save it to a PS1 file and simply run it on-demand. I saved my code to a script named Set-PSWebProxy.ps1