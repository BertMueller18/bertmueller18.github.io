---
layout: post
published: true
title: "How to use PowerShell and PsExec to change the RDS license server name on all your XenApp servers – JasonSamuel.com"
date: 2016-09-08T08:31:27.021Z
categories: powershell automation xenapp 
link: http://www.jasonsamuel.com/2013/03/07/how-to-use-powershell-and-psexec-to-change-the-rds-license-server-name-on-all-your-xenapp-servers/
tags:
  - links
ogtype: article
bodyclass: post
---

## How to use PowerShell and PsExec to change the RDS license server name on all your XenApp serversBy Jason Samuel
onMarch 7, 2013
SHARE TWEET SHARE SHARE 0 COMMENTS
Let’s say you decide to decommission your Remote Desktop Services (RDS)/Terminal Services Licensing Server or you moved your TS/RDS CALs to a different server. That means you need to change the name to the new server under Remote Desktop Session Host Configuration on all your XenApp servers.



This is a pain to do manually when you have several hundred XenApp servers. You can do it through group policy but you may only want to change it on a subset of servers in an OU and not all of them. So I used PowerShell and PsExec to precisely target all my XenApp servers I wanted to change. It’s a very quick option when you are pressed for time.
