---
layout: post
title:  "How to set Citrix XenApp 7.6 Policies with PowerShell – Sinisa Sokolic"
date:   2016-11-29T20:09:32.753Z
categories: citrix xenapp gpo activedirectory
link: https://www.sinisasokolic.com/how-to-set-citrix-xenapp-7-6-policies-with-powershell/
tags:
  - links
ogtype: article
---

## How to set Citrix XenApp 7.6 Policies with PowerShell

I was recently asked how to create Citrix policies with PowerShell and I must admit that it took me some time to figure it out. If you search for solutions you get only a few hints on how to do it. The best hint came from Ingmar Verheij (http://www.ingmarverheij.com/set-citrix-policies-via-powershell/) but things changed a little but with the latest XenApp and XenDesktop versions.

Why should we use PowerShell to create Citrix Policies?
Lets start with some words why you should use PowerShell and why you should use Citrix Policies without setting them by Group Policy. PowerShell gives us the possibility to create baseline policies for a whole bunch of customers and you can parameterize your installations or you can recreate your homelab automatically.
And… processing local policies should be much faster (I will recheck that argument shortly by comparing the logon duration between locally set Citrix Policies and GPOs).
