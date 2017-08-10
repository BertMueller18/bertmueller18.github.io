---
layout: post 
title:  "Powershell Script with Arguments as a Scheduled Task - And Deploy with GPO" 
date:   2017-03-14T21:54:19.808Z 
categories: powershell programming windows
link: https://www.andersrodland.com/powershell-script-with-arguments-as-a-scheduled-task/ 
tags:
  - links
ogtype: article 
---

> Powershell Script with Arguments as a Scheduled Task

March 11, 2017 Anders Rodland
This guide explains how to run a Powershell script with arguments as a scheduled task and how to deploy it with group policy.

I created this blog post as I got several questions how to set up my client health script. Some of the checks it does requires it to run in the system context, and it is also recommended to run it as a startup script. I also run it once a day on my customers. A scheduled task deployed with group policy is the best way to set this up and fulfill all these requirements.

 

POWERSHELL SCRIPT WITH ARGUMENTS AS A SCHEDULED TASK

Local machine: Start “Task Scheduler” and create a new task.

Group Policy: Computer Configuration -> Preferences -> Control Panel Settings – Scheduled Tasks. Create a scheduled task (at least Windows 7).