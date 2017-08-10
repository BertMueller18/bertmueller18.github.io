---
layout: post
title:  "Careful with Add-Member! - Power Tips - PowerTips - IDERA Community"
date:   2016-11-30T23:34:45.969Z
categories: powershell programming
link: http://community.idera.com/powershell/powertips/b/tips/posts/careful-with-add-member
tags:
  - links
ogtype: article
---

## Careful with Add-Member!

Frequently, Add-Member is used to create custom objects, for example like this:

$o = New-Object -TypeName PSObject
$o | Add-Member -MemberType NoteProperty -Name Notes -Value 'Something'
$o | Add-Member -MemberType NoteProperty -Name Date -Value (Get-Date)

$o
