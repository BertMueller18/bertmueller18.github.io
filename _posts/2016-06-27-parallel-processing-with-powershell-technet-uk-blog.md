---
layout: post 
published: true 
title: "Parallel processing with PowerShell | TechNet UK Blog" 
date: 2016-06-27T12:20:28.523Z 
link: https://blogs.technet.microsoft.com/uktechnet/2016/06/20/parallel-processing-with-powershell/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Parallel processing with PowerShell
★★★★★★★★★★★★★★★
Harry EaglesJune 20, 20161

By Richard Siddaway, the latest in his PowerShell series

The traditional approach to administering servers is to log into the server – usually via RDP these days as your data centre may be in a different building and often a different city. From there you can then perform your administrative tasks, log out – you’re not one of those people that doesn’t log out of administrator RDP sessions are you – and proceed to the next task on the next server.

If you have a handful of servers this approach is sustainable. By the time you get into the tens (low tens) of servers it just doesn’t work if you have to touch each server. Let me give you an example: a few years ago I heard a colleague grumbling because they had to go through the event logs on 30 servers to check which ones were showing a particular event. That’s not a quick process!

Before they’d finished the first server I’d written a quick and dirty PowerShell script that checked the event log on each server and counted the number of events of interest that were present. In most cases it was zero – which was good – so the support team could concentrate on the servers that actually had the problem. Those few minutes of scripting saved the support team hours of work and enabled the problem to be resolved much quicker. It also had the additional bonus of introducing the support team to PowerShell and got them interested in solving other problems using an automation approach.

Automating administrative tasks is a great time saver as well as bringing other benefits such as repeatability and consistency into your environment. However, there are some issues above and beyond learning how to automate tasks of which you need to be aware. One of those issues is the number of servers you need to deal with.