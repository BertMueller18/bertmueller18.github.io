---
layout: post 
title:  "How to Use Your Command History in Windows PowerShell – Movenergy" 
date:   2017-03-26T06:22:13.038Z 
categories: powershell programming
link: http://movenergy.net/how-to-use-your-command-history-in-windows-powershell/ 
tags:
  - links
ogtype: article 
---

## Windows PowerShell has a built-in command history feature that provides detailed information about the commands you’ve run. Like the Command Prompt, PowerShell only remembers your command history for the current session.

How to Use the Command-Line Buffer
PowerShell technically has two types of command history. First, there’s the commandline buffer, which is actually part of the graphical PowerShell terminal application and not part of the underlying Windows PowerShell application. It provides a few basic features:

Up Arrow: Recall the previous command you typed. Press the key repeatedly to walk through your command history.
Down Arrow: Recall the next command you typed. Press the key repeatedly to walk through your command history.
F8: Search your command history for a command matching the text on the current command line. So, if you wanted to search for a command that began with “p”, you’d type “p” on the command line and then repeatedly tap F8 to cycle through commands in your history that begin with “a”.
By default, the buffer remembers the last 50 commands you typed. To change this, right-click the title bar of the PowerShell prompt window, select “Properties”, and change the value of “Buffer Size” under Command History.