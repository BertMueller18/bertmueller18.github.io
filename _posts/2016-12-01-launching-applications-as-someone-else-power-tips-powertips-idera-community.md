---
layout: post
title:  "Launching Applications as Someone Else - Power Tips - PowerTips - IDERA Community"
date:   2016-11-30T23:29:40.866Z
categories: powershell programming
link: http://community.idera.com/powershell/powertips/b/tips/posts/launching-applications-as-someone-else
tags:
  - links
ogtype: article
---

## Launching Applications as Someone Else

Let’s assume you would like to open multiple PowerShell consoles running under different identities – or launch whatever application you require, just as someone else.

To do that, you would have to log on as someone else, and obviously that’s a strain. So here is a way to save credentials to file in a safe way: the password is encrypted using your identity and your machine as a secret. You can get it back only if you are the person that saved them, and if you do it on the machine where you saved the file:
