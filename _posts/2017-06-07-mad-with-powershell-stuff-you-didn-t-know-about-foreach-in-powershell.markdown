---
layout: post 
title:  "Mad With PowerShell: Stuff you didn’t know about ForEach in PowerShell" 
date:   2017-06-07T21:25:12.982Z 
categories: powershell programming
link: http://www.madwithpowershell.com/2014/03/stuff-you-didnt-know-about-foreach-in.html 
tags:
  - links
ogtype: article 
---

> Mad With PowerShell
Tim Curwick's PowerShell blog | Tips and tricks and tools and techniques | Explanations and explorations

Saturday, March 29, 2014
Stuff you didn’t know about ForEach in PowerShell
ForEach is a very useful tool.  I don’t have many scripts that don’t use it.  I’ve used it for years in hundreds of scripts.  But there is always more to learn.  I recently discovered some new things about it, and found that a lot of the information is not very discoverable and not well known.  So I thought I should share what I know about it.

This article is a mix of basic information, advanced techniques, and esoteric weirdness you’ll never need to know.  So take what’s useful to you and ignore the rest.

The first fun fact about ForEach is that it is actually two different things with the same name.  This was by design, as they intended for the two things to provide related behavior in different circumstances, and this was easier than trying to make one thing do everything.
