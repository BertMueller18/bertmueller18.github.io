---
layout: post 
title:  "Monitoring what matters – Windows Event Forwarding for everyone (even if you already have a SIEM.) – Security Stuff" 
date:   2017-10-24T06:32:39.050Z 
categories: eventlog powershell wef eventforwarding
link: https://blogs.technet.microsoft.com/jepayne/2015/11/23/monitoring-what-matters-windows-event-forwarding-for-everyone-even-if-you-already-have-a-siem/ 
tags:
  - links
ogtype: article 
---

## Monitoring what matters – Windows Event Forwarding for everyone (even if you already have a SIEM.)
★★★★★★★★★★★★★★★
Jessica Payne (MSFT)November 23, 201550 
35
6
Last week at Ignite Australia I presented a session (available here ) on something I don't think gets talked about enough - Windows Event Forwarding, or WEF.  (Edit: I've also since done an depth Microsoft Virtual Academy session on Event Forwarding too!).

Often when we engage for an Incident Response, we find the customer :

Has no centralized logging
Are not monitoring endpoints/member servers (often just DCs)
Spam logs with extra data
Are not logging key events
Logs roll too quickly
Those with centralized logging still missing data, takes too long for IT admins to get reports