---
layout: post 
title:  "PS without BS: Removing WMI Queries from GPMC – Lee Stevens: Technical Blogs" 
date:   2018-03-25T15:21:23.550Z 
categories: powershell gpo activedirectory wmi
link: https://blogs.technet.microsoft.com/leesteve/2018/02/05/ps-without-bs-removing-wmi-queries-from-gpmc/ 
tags:
  - links
ogtype: article 
---

> PS without BS: Removing WMI Queries from GPMC
leecstevensFebruary 5, 20180 
0
0
One of the neat features back in (cough) Windows Server 2003 was the addition of WMI filters to Group Policy. I'm not going to waste a lot of time this morning on a history lesson, but WMI filters in GPO have some valuable benefits, but unfortunately nothing in this life is free.

The answer a lot of enterprises employ is to get "OU happy" and move the object around OUs at will. I don't recommend this as a general practice for a few reasons:

You may not be applying the same policy base and may unknowingly creating a security hole or violating company policy.
You could be no longer employing GPOs needed by some applications or services to work.
This theory holds up until the object needs to land in 2 OUs at the same time (can't do that). So, your option is to create a worse management headache: a third OU that likely turns abandoned by administrators future who saw it as "always been there".
Good news, people - there is a better way.  

The key advantage to WMI filters in GPOs as I see it is for testers, say you are migrating Windows 7 to Windows 10 or an admin that logs inbetween workstation and server and you want to have different policy settings. You have a few options:

Configuring loopback in replace mode is certainly one way this can be accomplished, however, multiple policies generally apply to a user account, so this may be a bit more difficult to master. If all you need is a single user policy (and I recommend consolidating as much as possible where it makes sense), this is for you.

Configuring WMI filters can also be useful, since when you are on one operating system, you have one experience, and on another, have a different experience.

So, why no love for WMI?
It's not that I don't love WMI. Most of you who know me also know I have a strong SMS (SCCM) background, and SMS is what introduced WMI into the world. WMI makes you look smart, when you can whip out a query like "select name from win32_operatingsystem where name... blah blah" versus a boring old security group filter. Let's be honest with ourselves here also, WMI filters are far more easy to set up in GPO than security group membership.

The simple truth of WMI filters in GPO is that it can significantly impact the time it takes to process for these simple facts: WMI has to spin up and if you process GPOs synchronously, can slow down processing. I know Microsoft has pushed this as "the go-to thing" for a long time, and then backed off of it. Technology changes, and although this solution has always existed in Active Directory (yes, Windows 2000 AD could do this), wasn't really seen as a "go-to" after WMI queries.

So I promised a fix, and here it is: Security Filtering. I wrote a PowerShell script that will look into Active Directory, pull out computer accounts which have the proper OS and drop them into an AD Group. It will also clean out any systems that may be there in error, or could have been upgraded (like Win7 to Win10).

But wait, there's more in that you can also use these same security groups in item level targeting with Group Policy Preferences. This also would limit the WMI calls being made by using Security Group settings rather than spinning extra cycles in WMI.

Is this immediate? Well, no. You can set this as a scheduled task, but keep in mind you will need to have your domain controllers replicate as well. The client will not be considered part of the security group until the DC they are connected to received the group membership update and they have rebooted. Once this has happened, it won't have to happen again (unless the computer is somehow removed from the group). Otherwise, this is a "once and done" scenario.

Enough, this is the PS without BS series, so let's get to the code. Some noteables:

You can call the group whatever you like, that was my name.
The OS Filter (say Windows 10*) is intended to catch multiple editions, like Pro and Enterprise. Same goes for Windows 7 and 8.
Some characters like * and $ are reserved in PowerShell. I'd love to remove these but lacked the patience to troubleshoot if it was possible. I'll take the heat if someone actually benchmarks this per 100,000 users taking 4.11 seconds longer. 
I chose Yellow and Cyan as colors if you want to see output. Could I make this more annoying? Well, it's bright and visible. Possibly, magenta and lime is more annoying.