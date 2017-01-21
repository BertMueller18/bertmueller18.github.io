---
layout: post 
published: true 
title: "Checking effective audit policy forest wide (Get-Auditpol) | Stuff n Things" 
date: 2016-06-27T21:40:58.061Z 
categories: security activedirectory gpo
link: https://blogs.technet.microsoft.com/kfalde/2016/06/05/checking-effective-audit-policy-forest-wide-get-auditpol/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Checking effective audit policy forest wide (Get-Auditpol)

Kurt Falde June 5, 2016

Too many times dealing with customers I find that audit settings are either poorly configured or not configured at all.  The funny thing is this is not industry dependent etc. some of the customers who you would think have the best audit configurations due to various regulations and specific guidelines for auditing in many cases have some of the worst auditing setups.  

You tend to find workstations that either don’t have any audit configured or have something like both legacy auditing and advanced audit policies half applied which puts them in a broken place when they have a setting they wanted in the old settings but the equivalent thing not set in the advanced audit policies.  

I also tend to see a lot of .. well we delegate out GPO management to sub-OU managers either based on org hierarchy or geographical location management etc which typically results in new GPO’s for all these various sub-OU’s where each sub-OU manager does their own thing for audit which widely varies based on knowledge experience etc.  

In my perfect world there would be 3 GPO’s linked at the root of each domain that controlled all audit for all systems.. one for Servers, one for DC’s (Ok yeah link it at the DC OU level  ), and one for Workstations. Since this perfect world rarely happens I put together a script that will query all systems throughout a forest and dump current effective audit settings via auditpol along with a number of other audit settings that I would consider key but aren’t part of the normal ‘Advanced Audit Policies’.
