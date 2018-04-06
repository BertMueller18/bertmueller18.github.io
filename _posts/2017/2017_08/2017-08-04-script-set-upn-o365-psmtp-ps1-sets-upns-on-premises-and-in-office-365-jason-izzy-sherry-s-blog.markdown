---
layout: post 
title:  "Script: Set-UPN-O365-PSMTP.ps1 – Sets UPNs on-premises and in Office 365 | Jason (Izzy) Sherry's Blog" 
date:   2017-08-04T07:58:26.194Z 
categories: o365 office 356 upn sync
link: https://blog.jasonsherry.net/2014/08/15/script-set-upn-o365-ps1-sets-upns-on-premises-and-in-office-365/ 
tags:
  - links
ogtype: article 
---

## Script: Set-UPN-O365-PSMTP.ps1 – Sets UPNs on-premises and in Office 365

11/4/15: Posted script to TechNet Script Gallery: https://gallery.technet.microsoft.com/This-script-will-set-the-590a0907. Also updated code below and renamed the script to “Set-UPN-O365-PSMTP.ps1”

I’m working with a client who is migrating to Office 365 and we ran into the issue where users’ UPNs do not match their primary SMTP address, nor was it included as an SMTP address on their mailboxes.  In older, and maybe some current versions, of Android & iPhone devices if the user’s UPN didn’t match their primary SMTP address Autodiscover would fail. The user would then be prompted to put in the server name and login info.