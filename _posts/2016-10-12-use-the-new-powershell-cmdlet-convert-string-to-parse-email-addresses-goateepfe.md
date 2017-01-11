---
layout: post
published: true
title: "Use the new PowerShell cmdlet Convert-String to parse email addresses – GoateePFE"
date: 2016-10-12T20:36:07.105Z
categories: powershell  programming
link: https://blogs.technet.microsoft.com/ashleymcglone/2016/09/13/use-the-new-powershell-cmdlet-convert-string-to-parse-email-addresses/?utm_content=buffer0b371&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer
tags:
  - links
ogtype: article
bodyclass: post
---

## Use the new PowerShell cmdlet Convert-String to parse email addresses
Tired of hacking away at RegEx and string functions to parse text? This post is for you!

New toys
PowerShell 5.x includes a number of new features. One of the lesser-known and incredibly powerful is the string conversion set of cmdlets. The names are very similar. Check out how Get-Help describes them:

PS C:\> Get-Help Convert*-String | Format-Table Name,Synopsis -AutoSize

Name               Synopsis
----               --------
Convert-String     Formats a string to match examples.
ConvertFrom-String Extracts and parses structured objects from string content.
Convert-String
I will admit that doesn’t sound very interesting on first glance. But check out what they can do! Let’s start with a simple example of Convert-String:
