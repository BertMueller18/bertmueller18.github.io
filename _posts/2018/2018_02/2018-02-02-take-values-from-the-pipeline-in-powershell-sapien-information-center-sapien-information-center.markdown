---
layout: post 
title:  "Take Values from the Pipeline in PowerShell - SAPIEN Information Center | SAPIEN Information Center" 
date:   2018-02-02T16:02:05.527Z 
categories: powershell programming
link: https://info.sapien.com/index.php/scripting/scripting-how-tos/take-values-from-the-pipeline-in-powershell 
tags:
  - links
ogtype: article 
---

## Take Values from the Pipeline in PowerShell 

Written by June Blender C Last Updated: 22 February 2017 

User Rating: 4 / 5
Star ActiveStar ActiveStar ActiveStar ActiveStar Inactive
Please Rate Vote 1 Vote 2 Vote 3 Vote 4 Vote 5   

In Windows PowerShell, the command pipeline is magic that lets us string together simple, easily understood commands into a complex command with significant power. It makes generic commands, like Get-Item, Sort-Object, and Set-Content function like true reusable parts, so custom commands never need to create them.

To make a pipeline work, the output of one command must be the input to the next command. This article explains how to write parameters that take input from other commands in the pipeline. We'll go step-by-step and explain the details.
