---
layout: post 
title:  "Configuration Management with Octopus and PowerShell DSC - Octopus Deploy" 
date:   2017-02-26T08:08:12.870Z 
categories: mdt deployment powershell
link: https://octopus.com/blog/octopus-and-powershell-dsc 
tags:
  - links
ogtype: article 
---

> Configuration Management with Octopus and PowerShell DSC
Published on: 1 Dec 2016 by Paul Stovell
Comment(s) Walkthrough
PowerShell Desired State Configuration (DSC) is the PowerShell team's take on a declarative approach to configuring servers, and is an alternative to the imperative approach of standard PowerShell scripts. PowerShell DSC can be used for many of the common configuration tasks that need to run when a new server is provisioned. Some useful examples:

Installing Windows features, like IIS for web servers
Setting environment variables
Setting file and folder permissions
While Octopus focuses on continually delivering new versions of an application (the applications you are building yourself), these kinds of tasks are one-off and are usually done by a different set of tools. Over the last 6 months we've been working on a number of features that actually combine together to make Octopus a really effective configuration management tool when combined with PowerShell DSC.