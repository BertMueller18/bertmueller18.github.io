---
layout: post 
title:  "Use PowerShell to Determine if Specific Windows Updates are Installed on Remote Servers – Mike F Robbins" 
date:   2017-06-27T13:16:25.567Z 
categories: powershell remoting
link: http://mikefrobbins.com/2017/05/18/use-powershell-to-determine-if-specific-windows-updates-are-installed-on-remote-servers/ 
tags:
  - links
ogtype: article 
---

## Use PowerShell to Determine if Specific Windows Updates are Installed on Remote Servers

MIKE F ROBBINS MAY 18, 2017 5
It has been a crazy week to say the least. If you’re like me, you wanted to make sure that the specific Windows updates that patch the WannaCry ransomware vulnerability have been installed on all of your servers. I’ve seen a lot of functions and scripts this week to accomplish that task, but most of them seem too complicated in my opinion.

While it’s personal preference, I also always think about whether I should use a PowerShell one-liner, script, or function. Usually one-liners are something I type into the PowerShell console using all the aliases and positional parameters that I want since I’ll simply close out of the console when I’m done and the code is gone. Code with aliases and positional parameters shouldn’t be saved as scripts or shared with others.