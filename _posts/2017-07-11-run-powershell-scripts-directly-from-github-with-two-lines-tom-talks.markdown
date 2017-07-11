---
layout: post 
title:  "Run PowerShell Scripts Directly from GitHub with Two Lines - Tom Talks" 
date:   2017-07-11T07:27:30.744Z 
categories: powershell programming
link: http://tomtalks.uk/2016/02/run-powershell-scripts-directly-github-two-lines/ 
tags:
  - links
ogtype: article 
---

## Run PowerShell Scripts Directly from GitHub with Two Lines
07/02/2016 BY TOM ARBUTHNOT LEAVE A COMMENT

First off, this is a really bad idea most of the time. You shouldn’t run scripts on your system you don’t understand/haven’t reviewed and that someone else could edit at any time.

However, it is possible to pull scripts directly from GitHub and run them on a system. Allowing you to use 2 simple lines to invoke a larger script, and to pull the latest version of a script every time.

What we are doing here is using Invoke-WebRequest to get the GitHub “RAW” file from the master branch, which should always be the “current” script, then we are using Invoke-Expression to run that Script