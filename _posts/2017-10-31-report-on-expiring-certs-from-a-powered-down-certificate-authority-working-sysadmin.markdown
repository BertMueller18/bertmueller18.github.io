---
layout: post 
title:  "Report On Expiring Certs From A Powered Down Certificate Authority – Working Sysadmin" 
date:   2017-10-31T09:57:00.676Z 
categories: activedirectory pki certificate 
link: http://www.workingsysadmin.com/report-on-expiring-certs/ 
tags:
  - links
ogtype: article 
---

> Report On Expiring Certs From A Powered Down Certificate Authority
November 12, 2014Automation, PKI, PowerShell, SMA, Windows CAautomation, certificate authority, pki, powershell, sma, windows ca
Let’s hypothetically say I have an old Windows Server 2003 Intermediate Certificate Authority. Let’s also hypothetically say that I already replaced my antiquated Windows Server 2003 PKI infrastructure with a Windows Server 2012 PKI infrastructure and I am only keeping the 2003 stuff around so it can publish a CRL and to run a monthly script that tells me which certs are going to expire within 60 days. It’s good to know which certs will expire within 60 days so you can remember to renew them or confirm that they don’t need renewal.

