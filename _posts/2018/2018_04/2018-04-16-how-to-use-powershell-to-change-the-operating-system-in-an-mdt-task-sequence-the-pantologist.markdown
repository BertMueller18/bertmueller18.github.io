---
layout: post 
title:  "How to Use PowerShell to Change the Operating System in an MDT Task Sequence – The Pantologist" 
date:   2018-04-16T13:39:09.095Z 
categories: deployment referenceimage mdt powershell
link: https://thepantologist.com/how-to-use-powershell-to-change-the-operating-system-in-an-mdt-task-sequence/ 
tags:
  - links
ogtype: article 
---

> OW TO USE POWERSHELL TO CHANGE THE OPERATING SYSTEM IN AN MDT TASK SEQUENCE
Home / Technology & Applied Sciences / Computer Science / Information Technology / How to Use PowerShell to Change the Operating System in an MDT Task Sequence
12
JAN 2017
 8 COMMENTS
I’ve been working on completely automating the creation, capture, and testing of reference images using the Microsoft Deployment Toolkit (at version 2013 Update 2 as of this writing). The first two parts are straightforward and it’s easy to find guides on how to do that. However, I wanted to automate my process even more by having my newly captured image deployed to a test virtual machine and an email sent to let me know when it’s ready to check. At this point, all I need to do is verify that things work as expected in the VM and adjust my production task sequences to use the new OS if it all checks out.

Importing a new OS is easy. There’s a PowerShell commandlet for that included in the MDT tools. Importing a new task sequence is easy, too. There’s a commandlet for that.

What’s not so easy is editing a task sequence that already exists using PowerShell. In fact, I found very little online about how to do this – and nothing about how to change the OS of a task sequence. Nickolaj Andersen has a good post on using PowerShell to modify settings in MDT where he does change a task sequence, but he was simply turning Windows Updates off. And this guy asked how to modify the OS of a task sequence using PowerShell on TechNet but did not get a satisfactory answer in my opinion. But between Nickolaj’s post and some tinkering, I was able to get it working and finish automating those final bits of my process.