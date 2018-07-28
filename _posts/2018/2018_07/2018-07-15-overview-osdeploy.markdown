---
layout: post 
title:  "Overview · OSDeploy" 
date:   2018-07-15T21:47:36.578Z 
categories: deployment windows
link: https://www.osdeploy.com/osbuilder/overview.html 
tags:
  - links
ogtype: article 
---

## OSBuilder Overview
OSBuilder is a PowerShell module to help you perform Offline Servicing to a Windows Operating System Image. By using an Offline method of configuring an Operating System, it can then be imported in MDT or SCCM and used like any other OS Deployment. This includes being able to use in an Upgrade Task Sequence, which you cannot do with a Captured Image.
The main difference between OSBuilder and other scripted methods for Servicing a Windows Image Offline is that OSBuilder creates a prompted answer file called a Task (think Task Sequence). Since the Task has all the information it needs to update the Windows Image, there is no interaction necessary, and as long as the content (updates) are updated regularly, the Task can be repeated as needed.
Since the configuration is also saved in a Task, it is possible to select multiple tasks to run, and they will execute one right after another. This makes performing a monthly update take a few minutes to kick off. After a few hours, everything will be complete!