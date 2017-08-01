---
layout: post 
title:  "Promoting WSUS approvals" 
date:   2017-06-07T22:06:30.598Z 
categories: wsus powershell
link: https://tech.petewest.org/devops/2017/06/07/promoting-wsus-approvals/ 
tags:
  - links
ogtype: article 
---

> Promoting WSUS approvals
Jun 7, 2017

WSUS release schedules
Like many organisations we have debated automated Windows Server Update Services (WSUS) patch approval versus a more controlled staging/testing deployment schedule in depth. We’ve decided on a tiered release schedule depending on how critical we perceive the risk of leaving devices unpatched.

Critical patches that we believe are serious threat to the business get approved immediately.
Server patches get approved immediately, but the servers are configured to notify for install.
All other patches get released to a ‘Test PCs’ group in WSUS.
After a period of testing all patches will be released to all PCs.

