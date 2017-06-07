---
layout: post 
title:  "Mad With PowerShell: [Math] in PowerShell" 
date:   2017-06-07T21:26:29.099Z 
categories: powershell programming
link: http://www.madwithpowershell.com/2013/10/math-in-powershell.html 
tags:
  - links
ogtype: article 
---

> Math] in PowerShell
Basic arithmetic is, of course, built-in to PowerShell.

3 + 2  yields  5
3 - 2  yields  1
3 * 2  yields  6
3 * ( 3 + 2 )   yields  15
3 / 2   yields  1.5

That last one is nice.  In some programming languages, if you divide two integers, it will give you an integer result; if you don't want to lose your precision, you need to convert your variable types before the calculation, which is messy.  But in PowerShell, the result is of a logical type, and in those rare circumstances when you need to change it, it's always very easy.

And that's about all of the math PowerShell can do.
