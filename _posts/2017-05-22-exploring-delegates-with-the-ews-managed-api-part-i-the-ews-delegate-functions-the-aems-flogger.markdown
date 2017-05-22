---
layout: post 
title:  "Exploring Delegates with the EWS Managed API – Part I: The EWS Delegate Functions | The AEMS Flogger" 
date:   2017-05-22T10:07:40.697Z 
categories: exchange exchange2013 ews powershell
link: https://sites.utexas.edu/glenmark/2014/12/27/exploring-delegates-with-the-ews-managed-api-part-i-the-ews-delegate-functions/ 
tags:
  - links
ogtype: article 
---

> Exploring Delegates with the EWS Managed API – Part I: The EWS Delegate Functions
Posted on December 27, 2014
As an Exchange administrator, a long-standing source of frustration for me has been the fact that Microsoft does not provide tools for administratively inspecting and repairing delegate settings.  Apart from granting Full Access permissions on the mailbox and logging into it with Outlook, all an Exchange admin can really do is inspect the GrandSendOnBehalfTo attribute (a.k.a. publicDelegates), tinker with relevant folder sharing permissions, and use MfcMAPI to nuke the hidden delegate forwarding rule when it is misbehaving, which is rather drastic as it stops ALL delegate forwarding for that mailbox.

Well, there is