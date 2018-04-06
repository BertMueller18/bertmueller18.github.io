---
layout: post 
title:  "Tracing the Execution of a PowerShell Script – Hey, Scripting Guy! Blog" 
date:   2018-03-25T15:16:59.218Z 
categories: powershell programming
link: https://blogs.technet.microsoft.com/heyscriptingguy/2015/07/13/tracing-the-execution-of-a-powershell-script/ 
tags:
  - links
ogtype: article 
---


## Tracing the Execution of a PowerShell Script
Summary: Ed Wilson, Microsoft Scripting Guy, talks about using a cmdlet to trace the execution of a Windows PowerShell script.

Hey, Scripting Guy! Question Hey, Scripting Guy! I am having a problem with a script. It does not generate any errors, but dude, it does not seem to work either. Can you help me debug it?

—DR

Hey, Scripting Guy! Answer Hello DR,

Microsoft Scripting Guy, Ed Wilson, is here. When I see a script that doesn’t work, I think, "Cool…it is easy to troubleshoot." Often this is the case because the error message helps locate the source of the error. But if a script simply doesn’t work, it can be more difficult to troubleshoot. If the error is a logic error, it can be very difficult to troubleshoot.

Most of the time, examining the values of variables does not solve the problem because the code itself works fine. The problem often lies in what are called "the business rules" of the script. These are decisions the code makes that have nothing to do with the correct operation of, for example, a switch statement. At times, it may appear that the switch statement is not working correctly because the wrong value is displayed at the end of the code. But quite often the business rules themselves are causing the problem.

