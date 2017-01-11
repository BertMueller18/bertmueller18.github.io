---
layout: post
published: true
title: "Configuring the PowerShell ISE for use with Git and GitHub – Mike F Robbins"
date: 2016-11-09T19:40:23.116Z
categories:  powershell programming
link: http://mikefrobbins.com/2016/02/09/configuring-the-powershell-ise-for-use-with-git-and-github/
tags:
  - links
ogtype: article
bodyclass: post
---

## Configuring the PowerShell ISE for use with Git and GitHub

The goal of this blog article is to configure the PowerShell ISE (Integrated Scripting Environment) so the management of Git version control can be performed from it. Most tutorials you’ll find will attempt to lead you down the path of using SSH instead of HTTPS to synchronize your repositories to GitHub from the command-line but that’s really over-complicated and unnecessary if you’re using a Windows based machine.

The client machine used in this blog article runs the 64 bit version of Windows 10 Enterprise Edition. Windows 10 has PowerShell version 5 installed by default. Git for Windows version 2.7.0 and Posh-Git version 0.5.0.2015 are the third party software versions used in this blog article.

The first question you may ask is why not just use the Git Shell that’s installed as part of GitHub Desktop? While it’s true that you can launch Git Shell and then the ISE from it, the problem is that Git Shell uses the x86 (32 bit) version of PowerShell on a machine with a 64 bit operating system which means you won’t have all of your PowerShell modules available and that’s a solution that ends up being a sub-par experience. What I want to accomplish is simple, to launch a PowerShell ISE session as I always do and then to be able to manage both local Git repositories as well as remote ones on GitHub.
