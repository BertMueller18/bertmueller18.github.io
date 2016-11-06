---
layout: post 
published: true 
title: "How to add a progress bar to your PowerShell script – Communary" 
date: 2016-07-23T19:35:54.666Z 
link: https://communary.net/2015/01/19/how-to-add-a-progress-bar-to-your-powershell-script/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> How to add a progress bar to your PowerShell script
POSTED ON JANUARY 19, 2015 BY ØYVIND KALLSTAD
[Update] If you want to learn how to calculate seconds remaining when using progress bars, head on over to this post!

A very typical workflow when working with PowerShell, is to iterate through a collection of data. Inside each loop, you would perform some action, like getting or setting some data for instance. Depending on the size of the array, and the particular work you are doing within each iteration, this might often be a part of your script where users get little-to-none feedback that the script is still running.

Usability-wise this is bad, and you should strive to give the user some feedback that ‘stuff is happening‘. In this post I will show you how you can use the Write-Progress cmdlet to add a progress bar to your script, to give the user the needed visibility to know it’s running.

