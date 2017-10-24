---
layout: post 
title:  "PowerView 2.0 – harmj0y" 
date:   2017-10-24T06:35:46.503Z 
categories: activedirectory pentest powershell
link: http://www.harmj0y.net/blog/redteaming/powerview-2-0/ 
tags:
  - links
ogtype: article 
---

> PowerView 2.0
Published October 13, 2015 by harmj0y
PowerView is a tool that I’ve spoken frequently about on this blog. It debuted as part of the Veil-Framework in March of 2014, and has gone through a huge number of changes over the last year and a half. It is now a part of the PowerTools repository under the PowerShellEmpire GitHub account, and may be integrated soon into the central PowerSploit repository.

Today marks probably the biggest change to PowerView and how people use it since its inception. PowerView v2.0 is a major refactor that eliminates some code components, renames others, absorbs some functions into existing ones, and adds a chunk of new functionality. As this is a pretty substantial change that breaks backwards compatibility, we wanted to put together a guide on converting your usage of PowerView from 1.X to 2.0.

There is a tagged release of PowerView 1.9 here, and we will also keep the previous code under the “version_1.9” branch for a few months. I will also be going through past posts on this blog and making edits where appropriate at the top of each post with new function syntax, however any relevant presentation slide decks will remain in their original states. And finally, to facilitate the transition, there are a series of aliases for *most* old cmdlets at the bottom of the powerview.ps1 file (though this is far from perfect). This will remain in place for a few months, and will eventually be removed at some point down the line.

Removed Cmdlets