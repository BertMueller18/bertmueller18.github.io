---
layout: post 
title:  "Forensics: Automating Active Directory Account Lockout Search with PowerShell (an example of deep XML filtering of event logs across multiple servers in parallel) – GoateePFE" 
date:   2017-03-14T21:51:18.694Z 
categories: activedirectory security forensics powershell
link: https://blogs.technet.microsoft.com/ashleymcglone/2015/08/31/forensics-automating-active-directory-account-lockout-search-with-powershell-an-example-of-deep-xml-filtering-of-event-logs-across-multiple-servers-in-parallel/ 
tags:
  - links
ogtype: article 
---

## Forensics: Automating Active Directory Account Lockout Search with PowerShell (an example of deep XML filtering of event logs across multiple servers in parallel)

Today we learn how to efficiently filter event log queries, going beyond simple event ID filtering into the specific values of the XML message data. Then we will run this filter against multiple servers in parallel for faster data collection.

This posts meets the following objectives:

Add some efficiencies to my previous popular post for parsing XML event message data.
Apply the concept to Active Directory account lockout troubleshooting, formerly posted in the sample code of this post.
Provide a working example for your future event log forensic scripts, regardless of which logs or events or data you are mining. Our example today is Active Directory lockouts and bad password attempts.
Someone else may have done this already, but I have not searched for other examples.  This is my own approach to the solution.