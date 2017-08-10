---
layout: post 
title:  "Convert a HashTable to an Array – Jay Carper : ExchangeTips.us" 
date:   2017-06-07T21:49:47.372Z 
categories: powershell programming exchange
link: http://exchangetips.us/2016/01/convert-a-hashtable-to-an-array/ 
tags:
  - links
ogtype: article 
---

> Convert a HashTable to an Array

Posted: January 27, 2016/Under: PowerShell/By: jay c
Of course, this only works with a single column in the hashtable…

Say you have a list of mailboxes in a hashtable, like this:

$Mailboxes = Get-Mailboxes -OrganizationalUnit administration
But for some reason (It doesn’t really matter why, does it? You just do.) you want a list of their User Principal Names in an array instead of the hashtable. You can do this like so:

$Array = @()
$Mailboxes | Foreach {$Array += $_.UserPrincipalName}