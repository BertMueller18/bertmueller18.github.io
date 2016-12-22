---
layout: post 
published: true 
title: "How To Configures the SSL/TLS Settings For PowerShell Remoting | Indogeeks" 
date: 2016-08-01T07:34:17.024Z
categories: security pki certificates powershell
link: http://indogeeks.com/how-to-configures-the-ssltls-settings-for-powershell-remoting/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## How To Configures the SSL/TLS Settings For PowerShell Remoting

By indogeek | December 13, 2015 0 Comment
The script will walk the user through the steps necessary to choose a machine certificate and configure WSMan settings necessary to support  PowerShell remoting over an SSL/TLS encrypted channel. The script does not

1) enable PowerShell remoting or

2) create a Windows Firewall rule to allow access to TCP/5986, which is the default for remoting over SSL/TLS.

Enable PowerShell remoting by executing “enable-psremoting -force”.