---
layout: post
title:  "First Look: XenApp/XenDesktop 7.6 – Part 1 (Overview and Installation) | Pawel Serwan Blog"
date:   2016-11-29T20:07:44.522Z
categories: citrix xenapp deployment
link: https://pawelserwan.wordpress.com/2014/09/30/first-look-xenappxendesktop-7-6-part-1-overview-and-installation/
tags:
  - links
ogtype: article
---

## First Look: XenApp/XenDesktop 7.6 – Part 1 (Overview and Installation)
30 September 2014 by pawelserwan	15 Comments
As you already know from my previous post Citrix finally released new version of XenApp/XenDensktop platform with number 7.6. I have already listed few “new-old” features that were introduced with that version of XenApp/XenDesktop in one of me previous posts:
https://pawelserwan.wordpress.com/2014/08/27/xenapp-7-6-and-xendesktop-7-6-announced-old-features-back/
This is the first in series of blog posts describing new version of XenApp/XenDesktop.
In the first part – we installed first Delivery Controller and setup our new XenDesktop 7.6 site.
In the second part – we have configured first site.
In the third part – we prepared the template image of Windows Server 2012 R2 that will be used by MCS service for creation of new machines that will be hosting user desktops and applications.
In the fourth part – we upgraded XenApp 6.5 server to XenApp 7.6.
In the fifth part – we created machine catalogs and used previously prepared master image. We attached to the site as well upgraded XenApp 6.5 server.
In the sixth part – we delivered applications to the end users by creating delivery groups.
In the seventh part – we will configure StoreFront so that end users could launch their apps.
In the eighth part – we checked how Connection Leasing really works.
Key features in this release

This version of XenApp and XenDesktop includes new features that make it easier for users to access applications and desktops and for Citrix administrator to manage applications:
The session prelaunch and session linger features help users quickly access server-based hosted applications by starting sessions before they are requested (session prelaunch) and keeping application sessions active after a user closes all applications (session linger).
Support for unauthenticated (anonymous) users means users can access server-based hosted applications and server-hosted desktops without presenting credentials to StoreFront or Citrix Receiver.
Connection leasing makes recently used applications and desktops available even when the Site database in unavailable.
Application folders in Studio make it easier to administer large numbers of applications.
Other new features in this release allow you to improve performance by specifying the number of actions that can occur on a Site’s host connection, display enhanced data when you manage and monitor your Site, and anonymously and automatically contribute data that Citrix can use to improve product quality, reliability, and performance.The full list of new features can be found here:
