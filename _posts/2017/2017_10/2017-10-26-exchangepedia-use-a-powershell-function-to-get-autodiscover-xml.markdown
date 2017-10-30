---
layout: post 
title:  "Exchangepedia | Use a PowerShell function to get AutoDiscover XML" 
date:   2017-10-26T14:31:11.085Z 
categories: exchange outlook powershell
link: http://exchangepedia.com/2015/10/use-a-powershell-function-to-get-autodiscover-xml.html 
tags:
  - links
ogtype: article 
---

> Use a PowerShell function to get AutoDiscover XML
by BHARAT SUNEJA
If you manage Exchange or support Exchange Online users, you may need to retrieve the AutoDiscover XML response. You can use the Test E-mail AutoConfiguration option in Outlook or the AutoDiscover tests in Microsoft Remote Connectivity Analyzer to retrieve the AutoDiscover response. The good news is you can also use a PowerShell one-liner or function to retrieve it.

Here’s a one-liner that uses the Outlook.Application COM object. It requires Outlook.