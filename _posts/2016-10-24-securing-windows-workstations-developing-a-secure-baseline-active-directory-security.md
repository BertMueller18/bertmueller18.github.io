---
layout: post 
published: true 
title: "Securing Windows Workstations: Developing a Secure Baseline » Active Directory Security" 
date: 2016-10-24T16:55:57.925Z 
link: https://adsecurity.org/?p=3299 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Securing Windows Workstations: Developing a Secure Baseline
Microsoft Security, Security Recommendation, Technical Reference by Sean Metcalf
Securing workstations against modern threats is challenging. It seems like every week there’s some new method attackers are using to compromise a system and user credentials.
The best way to create a secure Windows workstation is to download the Microsoft Security Compliance Manager (currently at version 4.0) and select “Security Compliance” option under the operating system version for which you want to create the security baseline GPO. Review the options, change as needed, and export as a GPO Backup (folder). Then apply this GPO to your workstations. This will improve your workstation security baseline if you have minimal security settings already configured, especially if you have no existing workstation GPO.