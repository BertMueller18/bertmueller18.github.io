---
layout: post
title:  "Going serverless with PowerShell – Medium"
date:   2017-01-01T10:57:52.912Z
categories: powershell github programming
link: https://medium.com/@devlead/going-serverless-with-powershell-705677a9ae86#.lrs5wyrz8
tags:
  - links
ogtype: article
---

## Going serverless with PowerShell
Why should JavaScript developers have all the fun?


PowerShell + Azure Functions = ❤
One of the current hype buzzwords going around is “serverless”, very (very) simplified there’s still a server you just don’t see or manage a server and you can be billed by individual usage of “functions” instead of per web app basis. Making scale and cost much more granular and also less ceremony to get a piece of code up and running.
Microsoft serverless offering is called Azure Functions and in this post I will go thru how to setup a continuously deployed HTTP API powered by PowerShell. I’ll assume you already have an Azure Subscription in place and some basic Azure Portal knowledge. One word of warning, while Azure Functions is released and stable, using PowerShell to write functions is still in preview and might be subject to change.
