---
layout: post 
title:  "Introducing Project Sauron – Centralised Storage of Windows Events – Domain Controller Edition – Practical Windows Security" 
date:   2017-10-19T21:18:11.160Z 
categories: security 
link: https://blogs.technet.microsoft.com/russellt/2017/05/09/project-sauron-introduction/ 
tags:
  - links
ogtype: article 
---

> Introducing Project Sauron – Centralised Storage of Windows Events – Domain Controller Edition
★★★★★★★★★★★★★★★
Russell Tomkins [MSFT]May 9, 20178 
0
0
(Nearly) every customer I visit is lacking comprehensive security auditing in their downlevel DEV and UAT environments and sometimes even in their production environment. This scenario exists for a number of reasons. For some larger customers, the security logs roll so quickly that it's considered "too hard" to even bother trying to archive them without a SIEM in place. Sometimes they have a project already "planned" or "in-flight" to deploy <insert product name here> that will capture all the required events but it is still months away (or longer). One that i'm hearing a lot more of lately "we used to store everything but our SIEM is now to expensive and we can only store some of it". I find this one so amusing since the cost of large volume storage has dropped so dramatically.

 

Without an effective security audit trail, the ability to discover when changes were made or possibly even track a breach during a security incident response becomes near impossible.
 

Project Sauron aims to resolve a number of these issues using the built-in security capabilities of Windows to store the appropriate events.

 

Windows Event Forwarding is in no way new, however the ability to create custom destination for forwarded events has always been difficult. My previous blog post explained how to create custom event logs for this purpose however it was quite tedious to build anything greater than a few destinations and I wanted to create lots of destinations, not just a few.

Using the Project Sauron Framework, the deployment of centralised Windows Event Collector (WEC) server becomes almost simple. Using custom WEC subscriptions, the required events are forwarded into dedicated event channels and dedicated .evtx file. Creation and deployment of your own custom solution (would love to hear your ideas) or re-using one the pre-built solutions can have you operational in matter of hours not months. The diagram below gives an example of how the framework can be used.

