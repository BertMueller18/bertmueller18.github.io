---
layout: post 
title:  "PADT script to install *.msu file : PowerShell" 
date:   2017-09-18T13:20:51.395Z 
categories: deployment mdt powershell psadt 
link: https://www.reddit.com/r/PowerShell/comments/5mxlib/padt_script_to_install_msu_file/ 
tags:
  - links
ogtype: article 
---

## PADT script to install *.msu file (self.PowerShell)
eingereicht vor 8 Monate von jetmanus
So I'm trying to install a *.msu file. I would like to be able to use the PowerShell App Deployment Toolkit since I'm familiar with it. What I need to do is to stop Windows Update service (wuauserv) and install the *.msu file. Can this be done?
2 KommentareWeitersagenmelden
Alle 2 Kommentare
sortiert nach: beste
[–]jheinikel 2 Punkte vor 8 Monate 
You can do it this way if you want to install it silently:
Stop-Service wuauserv -Force
Start-Process WUSA.exe -ArgumentList "Path\File.msu /quiet /norestart" -Wait
Permalinkembed
[–]jetmanus[S] 1 Punkt vor 8 Monate 
Worked like a charm. Thank you very much.
PermalinkembedÜbergeordnet