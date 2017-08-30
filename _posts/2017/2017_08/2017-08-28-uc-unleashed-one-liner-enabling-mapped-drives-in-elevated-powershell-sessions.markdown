---
layout: post 
title:  "UC Unleashed » One Liner: Enabling Mapped Drives in Elevated PowerShell Sessions" 
date:   2017-08-28T05:30:11.419Z 
categories: powershell windows security
link: https://www.ucunleashed.com/3116 
tags:
  - links
ogtype: article 
---

## One Liner: Enabling Mapped Drives in Elevated PowerShell Sessions
July 18th, 2016Pat RichardLeave a commentGo to comments
If you’ve worked with mapped drives in PowerShell sessions, you know it’s problematic to access mapped drives from an elevated PowerShell session when UAC is configured to prompt to prompt for credentials. Microsoft released a TechNet KB article on this issue quite some time ago. The article shows different ways to address the problem, from using the Local Security Policy, mapping the drives again in the elevated prompt, and using the registry. We’ll focus on the registry here for several reasons. The first is that using the local security policy seems burdensome; mapping the drives again seems redundant, and potentially confusing if the original mappings change and the ones in your PowerShell session don’t; and thirdly, and most important, we’re talking PowerShell here!