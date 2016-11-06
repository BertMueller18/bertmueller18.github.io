---
layout: post 
published: true 
title: "LTI/ZTI PowerShell: Accessing Task Sequence Variables  Scriptimus Ex Machina" 
date: 2016-06-14T12:24:23.652Z 
link: https://scriptimus.wordpress.com/2012/09/17/ltizti-powershell-accessing-task-sequence-variables/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

LTI/ZTI PowerShell: Accessing Task Sequence Variables
Posted on September 17, 2012 by Andrew Barnes


In order to create more useful scripts in your Lite/Zero-Touch deployments, you will need access to the deployment variables. In MDT 2012 you can now access these Task Sequence variables from 2 new PSDrives called TSEnv: and TSEnvList:.



Now these drives only exist while a task sequence is running so Microsoft recommend that you add the line

Import-Module .\ZTIUtility.psm1

to your scripts in order to create the drives for testing. You can also populate these drives with variables that you would expect to find when your script runs. It’s possible to access the variables in real time but to do this you will need to pause the Task Sequence while launching a PowerShell console, then import the module. This is how I do it.