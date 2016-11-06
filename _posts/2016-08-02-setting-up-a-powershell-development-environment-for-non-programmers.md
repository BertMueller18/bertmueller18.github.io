---
layout: post 
published: true 
title: "Setting up a powershell development environment for non-programmers" 
date: 2016-08-02T06:57:49.587Z 
link: https://vxsan.com/setting-up-a-powershell-development-environment-for-non-programmers/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Setting up a powershell development environment for non-programmers
By Sjors Robroek · a month ago in Powershell, PowerCLI, Pester, Test driven development ·  0 Comments 0Shares    
In most of my projects, powershell and its vendor-specific modules such as VMware's powercli is usually a necessity to work effectively. In addition, most customers appreciate it greatly if you can leave them with a handful of examples on how to run standard procedures through a script, even though it might not always be part of the deliverables.

Most of the time however, those scripts are written as one-offs, tend to require major rewriting for a different use case and don't have any kind of error handling or input validation. As such, i usually tend to rewrite a new script from scratch for a new project, which kind of defeats the purpose of the reusability of scripts.

Last week i sat down and decided to think up a proper development environment for powershell related tasks. While it's only a beginning, it does help with writing clean code allowing you to spend less time coding the next time.