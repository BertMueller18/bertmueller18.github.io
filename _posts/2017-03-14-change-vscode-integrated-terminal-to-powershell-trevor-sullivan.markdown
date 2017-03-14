---
layout: post 
title:  "Change VSCode Integrated Terminal to PowerShell - Trevor Sullivan" 
date:   2017-03-14T21:52:09.285Z 
categories: powershell programming vscode
link: https://trevorsullivan.net/2017/03/11/change-vscode-integrated-terminal-powershell/ 
tags:
  - links
ogtype: article 
---

> Change VSCode Integrated Terminal to PowerShell
 Trevor Sullivan March 11, 2017 powershell
Visual Studio Code is an excellent developer tool for PowerShell projects. However, regardless of which type of project you’re developing (C#, Node.js, Python, etc.), you can benefit from changing your default shell to the powerful, object-oriented PowerShell shell. Now, you may not want to change your default shell for the entire operating system. VSCode thankfully exposes a configuration option that allows you to change the default shell only for the VSCode Integrated Terminal. This won’t affect the default shell for your host operating system.

To change your default shell for VSCode to PowerShell Core, simply:

Install Visual Studio Code
Install PowerShell Core
Hit CMD + , (Mac OS X) to open your User Settings, or search for it via the Command Palette (F1 key)
Add the terminal.integrated.shell.osx option to your JSON configuration
Set the value of the option to /usr/local/bin/powershell