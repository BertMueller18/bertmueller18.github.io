---
layout: post 
title:  "Deploy Exchange Server 2019 on Windows Server Core – You Had Me At EHLO…" 
date:   2018-07-28T22:19:32.176Z 
categories: exchange exchange2019 server2016 servercore
link: https://blogs.technet.microsoft.com/exchange/2018/07/26/deploy-exchange-server-2019-on-windows-server-core/ 
tags:
  - links
ogtype: article 
---

## Deploy Exchange Server 2019 on Windows Server Core

The Exchange TeamJuly 26, 20184 


Hurrah! If you have not yet heard: Exchange Server 2019 Public preview was announced earlier, and it is the first version of Exchange that you can install on Server Core!

Now, while that’s great news, if you haven’t worked on Server Core, there may be bit of a learning curve. The purpose of this post is to help you install the Exchange Server 2019 on Server Core in your lab.

We are going to assume that you have:

Installed an Active Directory global catalog domain controller. Exchange Server 2019 will work with writable DCs running Windows 2012 R2 and above. Here’s a link to get you going with Active Directory, in case you have not installed it yet.
Installed Windows Server 2019 (or Windows Server 2016) Server Core operating system.
(In case you need help with Server Core deployment, please follow this link).

