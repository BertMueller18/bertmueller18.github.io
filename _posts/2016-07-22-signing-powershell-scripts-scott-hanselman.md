---
layout: post 
published: true 
title: "Signing PowerShell Scripts - Scott Hanselman" 
date: 2016-07-22T18:21:35.989Z
categories: powershell security
link: http://www.hanselman.com/blog/SigningPowerShellScripts.aspx 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Geoff Bard at Corillian (we work together) wrote up a good tutorial on working/playing with Signed PowerShell scripts. He graciously agreed to let me reprint a linted version here:

## Signing PowerShell Scripts

Execution Policies

PowerShell supports a concept called "execution policies" in order to help deliver a more secure command line administration experience.  Execution policies define the restrictions under which PowerShell loads files for execution and configuration.  The four execution policies are Restricted, AllSigned, RemoteSigned, and Unrestricted.

PowerShell is configured to run in its most secure mode by default.  This mode is the "Restricted" execution policy, in which PowerShell operates as an interactive shell only.  The modes are:  Restricted (default execution policy, does not run scripts, interactive only); AllSigned (runs scripts; all scripts and configuration files must be signed by a publisher that you trust; opens you to the risk of running signed (but malicious) scripts, after confirming that you trust the publisher); RemoteSigned (runs scripts; all scripts and configuration files downloaded from communication applications such as Microsoft Outlook, Internet Explorer, Outlook Express and Windows Messenger must be signed by a publisher that you trust; opens you to the risk of running malicious scripts not downloaded from these applications, without prompting); Unrestricted (runs scripts; all scripts and configuration files downloaded from communication applications such as Microsoft Outlook, Internet Explorer, Outlook Express and Windows Messenger run after confirming that you understand the file originated from the Internet; no digital signature is required; opens you to the risk of running unsigned, malicious scripts downloaded from these applications).