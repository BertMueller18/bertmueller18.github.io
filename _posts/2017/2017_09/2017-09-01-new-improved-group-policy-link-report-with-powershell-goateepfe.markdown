---
layout: post 
title:  "New, Improved Group Policy Link Report with PowerShell – GoateePFE" 
date:   2017-09-01T05:18:48.132Z 
categories: gpo activedirectory powershell reporting 
link: https://blogs.technet.microsoft.com/ashleymcglone/2017/08/31/new-improved-group-policy-link-report-with-powershell/ 
tags:
  - links
ogtype: article 
---

## New, Improved Group Policy Link Report with PowerShell

 A peer asked me to update one of my classic Group Policy reporting scripts this week, so I thought I would share the update with y'all.

### Continuous Improvement
Over the years I have released a number of Group Policy scripts. This one shows you all kinds of goodness:

* GPOs linked to OUs
* OUs where block-inheritance may be turned on
* Situations where no-override is used
* Forensic data about the last time a GPO was linked or updated on an OU

By popular demand the improvements in this release are:

* Unlinked GPOs are included
* Columns are added for easy filtering where User or Computer version do not match
* Output no longer defaults to CSV, so that you can pipe the output wherever you like