---
layout: post 
title:  "Adding Updates to a Wim File - PowerShell.Getchell.Org" 
date:   2017-06-15T08:59:28.875Z 
categories: deployment win10 mdt2013 powershell
link: https://powershell.getchell.org/2017/06/08/adding-updates-to-a-wim-file/ 
tags:
  - links
ogtype: article 
---

> ADDING UPDATES TO A WIM FILE
 June 8, 2017  Nicholas M. Getchell Comments  0 Comment
Even with Microsoft releasing new Windows 10 builds on a twice-yearly basis, there is still a case to be made to slipstream updates into your install media. First, you never have to worry about whether your computer gets needed patches. If you build in protection against the Wanna Cry malware by patching MS17-010 you can. Second, it saves a decent amount of time during computer provisioning. No need to push down the original copy of a file as well as the updated one included in the latest Windows update.