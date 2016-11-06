---
layout: post 
published: true 
title: "Using PowerCLI to build multiple VMs - Notes of a scripter" 
date: 2016-06-21T07:38:06.691Z 
link: http://notesofascripter.com/2016/03/28/using-powercli-build-multiple-vms/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Using PowerCLI to build multiple VMs

My first script that I ever wrote was a script to build VMs. I was the newest member on the team, and i was giving the task of building 50 VMs for a new project that was getting started. It was a very daunting task, due to the completion date to have these 50 VMs to be completed. So one of the other members of the team told me about PowerCLI, but didn’t have any knowledge about it. So I started to read about it, and got it installed. I started to run very simple commands, such as Get-Template just to see what it does. The more I got used to running these commands, I started to put together the script. So I started with getting all of the information that I needed to build the VM, the VM specs. So I put all of this information into a CSV file.