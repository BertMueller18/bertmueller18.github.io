---
layout: post 
published: true 
title: "Citrix Personal vDisk: Troubleshooting and Fixing Misbehaving Applications | Citrix Techs" 
date: 2016-09-26T13:50:09.533Z 
link: http://citrixtechs.com/blog/citrix-personal-vdisk-troubleshooting-and-fixing-misbehaving-applications-2/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Citrix Personal vDisk: Troubleshooting and Fixing Misbehaving Applications
Posted on December 26, 2012 by greg

Background Info

At a client site recently I found myself troubleshooting an issue with an Oracle JD Edwards (JDE) application that was installed on the Windows 7 master image in a XenDesktop 5.6 environment utilizing Machine Creation Services (MCS) along with Personal vDisk (PvD). The client was getting very frustrated with Citrix XenDesktop since PvD was not saving their user’s settings and work they performed within the JDE application after either an administrator or the user restarted their VM. These particular users were developers and at times would code for hours or even days. So, losing days’ worth of work was not acceptable not to mention the main reason the client invested in Citrix XenDesktop was to utilize PvD in lieu of dedicated desktops to save on management and storage cost. For some reason Personal vDisk was not capturing everything they did within the JDE application. Yet, it was working as it should for all other applications. So, I went on a mission to find out why.