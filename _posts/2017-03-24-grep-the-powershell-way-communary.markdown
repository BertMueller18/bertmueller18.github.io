---
layout: post 
title:  "Grep, the PowerShell way – Communary" 
date:   2017-03-24T17:17:08.061Z 
categories: powershell programming grep
link: https://communary.net/2014/11/10/grep-the-powershell-way/ 
tags:
  - links
ogtype: article 
---

> Grep, the PowerShell way
POSTED ON NOVEMBER 10, 2014 BY ØYVIND KALLSTAD
I recently ran across an article about ‘15 Practical Grep Command Examples In Linux/Unix‘, and thought it would be cool to run through each of the examples, and give the PowerShell equivalent for each one.

This is not meant to be a grep vs Select-String (or Linux vs Windows), but look at it as an introduction to Select-String if you are familiar with grep already.
In PowerShell, the command used for string matching is of course Select-String, but since these examples are meant to be run in the console, I will be using the default alias ‘sls‘.