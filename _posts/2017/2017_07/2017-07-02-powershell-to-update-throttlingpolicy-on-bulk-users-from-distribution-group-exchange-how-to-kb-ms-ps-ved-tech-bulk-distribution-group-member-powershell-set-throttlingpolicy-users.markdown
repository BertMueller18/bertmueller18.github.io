---
layout: post 
title:  "Powershell to update ThrottlingPolicy on bulk users from distribution group EXCHANGE, How To, KB, MS, PS - Ved Tech bulk, distribution, group, member, powershell, set, throttlingpolicy, users" 
date:   2017-07-02T10:38:07.553Z 
categories: exchange throtteling
link: http://vedtechno.com/powershell-to-set-throttlingpolicy-on-bulk-users-member-of-one-distribution-group/ 
tags:
  - links
ogtype: article 
---

## POWERSHELL TO UPDATE THROTTLINGPOLICY ON BULK USERS FROM DISTRIBUTION GROUP
indiakb | October 29, 2015 | EXCHANGE, How To, KB, MS, PS | No Comments
Home » EXCHANGE » Powershell to update ThrottlingPolicy on bulk users from distribution group

Powershell to set ThrottlingPolicy on bulk users member of one distribution group

You can set ThrottlingPolicy “exchcheck” on bulk users who are part of one Distribution group by using below command:

`Get-DistributionGroupMember group1 |foreach {write-host $_.PrimarySmtpAddress ; Set-Mailbox -ThrottlingPolicy exchcheck -Identity $_.Alias}`
