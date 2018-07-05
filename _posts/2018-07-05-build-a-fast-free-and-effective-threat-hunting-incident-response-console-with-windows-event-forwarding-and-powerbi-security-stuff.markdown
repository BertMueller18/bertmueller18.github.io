---
layout: post 
title:  "Build a fast, free, and effective Threat Hunting/Incident Response Console with Windows Event Forwarding and PowerBI – Security Stuff" 
date:   2018-07-05T13:20:23.969Z 
categories: windowseventforwarding powerbi activedirectory pentest security
link: https://blogs.technet.microsoft.com/jepayne/2017/12/08/weffles/?platform=hootsuite 
tags:
  - links
ogtype: article 
---

## Build a fast, free, and effective Threat Hunting/Incident Response Console with Windows Event Forwarding and PowerBI
★★★★★★★★★★★★★★★
Jessica Payne (MSFT)December 8, 201713

Monitoring your network and gathering massive amounts of data has become easier and easier. Many guides exist on how to gather data, and lots of companies have "enterprise grade" Security Information and Event Management products that can ingest terabytes of data. But what seems to be missing from most environments is the ability to apply context to the data they get, or a knowledge of why certain artifacts that get gathered are important.

Doing Incident Response as a consultant gives you a unique perspective on monitoring, as you get to experience a wide variety of networks in varying stages of overall "health" during what is the worst possible time for owners. Things that normally can slide under the radar like slightly unhealthy patch management systems, or systems that have operational issues with monitoring agents suddenly become insurmountable problems to diagnosing and solving the security issue on the network. Another common finding is that while the company may be collecting data from servers and Domain Controllers, due to licensing costs they are not getting data from desktop endpoints, which are often times both the entry point in an intrusion and where a lot of the data access/exfiltration and lateral movement story happens. These issues are universal in companies big and small, with massive investments or minimal investments in their IT departments, and often aren't revealed until an incident occurs. This leaves the IT and Incident Response team in a position where they have to correct visibility issues when their infrastructure may not be working optimally, and rapidly be able to triage the data from potentially hundreds of thousands of endpoints while learning how to apply context to the events they are seeing.

Learning from these incidents, and the requirements inherent to them (ability to deploy tools and get data rapidly, use only built in tools, has to be usable and deployable by people who probably haven't slept in a week) I developed an Incident Response dashboard that I liked so much I personally used it to "hunt" on all the engagements in the later part of my Incident Response Consultant tenure. Many of the customers liked it so much that they have kept it in their environments to use for proactive threat hunting and log analysis. Using the built in Windows Event Forwarding components of Windows, some PowerShell scripts, and PowerBI desktop, you can create a fast, free, and effective console for diagnosing problems and finding Indicators of Attack in your network. My hope is to make security investigation much more accessible to everyone by showing how to do this quickly and without a massive monetary investment.

We'll go in to detail of how to deploy it and what to look for below, but here's a preview of what you get at the end to hopefully convince you to finish reading and deploy.