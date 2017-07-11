---
layout: post 
title:  "David Gardiner - Dave's Daydreams: PowerShell Wix Extension" 
date:   2017-01-12T13:38:09.559Z 
categories: powershell deployment
link: https://david.gardiner.net.au/2014/05/powershell-wix-extension.html 
tags:
  - links
ogtype: article 
---
## PowerShell Wix Extension 

I've looked, but I couldn't find anyone who'd implemented a Wix Extension that would allow running PowerShell scripts. So I've spent a few hours this weekend writing one (and learned a bit more about Wix and MSIs along the way).
This extension allows you to run script from a file that is included in the MSI, or inline script (inside a CDATA section).
By hosting PowerShell in the custom actions, scripts also get access to the $session variable (which is of type Microsoft.Deployment.WindowsInstaller.Session), so you can call $session.Log("Running this") and it will add "Running This" to the MSI log!

