---
layout: post 
published: true 
title: "PowerOPS: PowerShell for Offensive Operations | Portcullis Labs" 
date: 2016-07-17T08:58:49.740Z
categories: powershell pentest security
link: https://labs.portcullis.co.uk/blog/powerops-powershell-for-offensive-operations/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## PowerOPS: PowerShell for Offensive Operations
Published 03/06/2016 | By RFR
At Portcullis, one of the most frequent assessments we perform are breakouts. One of the main challenges we face during these assessments is to get command execution that can either help escalate our privileges or allow us to gain access to different systems on the network. Sometimes we find harsh group policy restrictions in place that block access to the Windows Command Prompt, PowerShell, among others. These, however, are not always properly implemented, i.e. they do not block access to all executables (and allow only certain programs to run).

After getting command execution, we want to attack other systems on the network. However it isn’t always easy to get a flexible toolbox in the system that allow us to gather information and launch further attacks. PowerShell is our preferred post-exploitation language and powershell.exe access is usually blocked (as .ps1 scripts). However since the block is often incorrectly implemented, i.e. the DLLs used by PowerShell aren’t usually blocked, this can open some doors. On top of that some AVs started implementing some basic signatures that will pick some well known PowerShell scripts. The bypass is trivial but we want to be as stealthy as possible and it still delay us a bit.

How can we bypass some of these “security mitigations” and speed up our tests? PowerOPS is an application written in C# that does not rely on powershell.exe but runs PowerShell commands and functions within a PowerShell runspace environment (.NET). Besides this, it includes multiple offensive PowerShell modules to make the process of post-exploitation easier.

It tries to follow the KISS principle, being as simple as possible. The main goal is to make it easy to use PowerShell offensively and help to evade anti-virus and other mitigations.