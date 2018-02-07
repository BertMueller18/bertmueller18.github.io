---
layout: post 
title:  "A PowerShell Tool Scorecard" 
date:   2018-01-27T11:59:21.852Z 
categories: powershell programming
link: http://wragg.io/the-powershell-tool-scorecard/ 
tags:
  - links
ogtype: article 
---
## A PowerShell Tool Scorecard

17 Jan 2018  

This post contains a PowerShell tool-making scorecard: a series of short questions to assess whether your custom cmdlet/function/tool is following some (generally considered) best practice design choices.


By "tool-making" I am referring the concept of creating one or more PowerShell functions that are intended to be used by end users in the same way as any other built-in (or 3rd party) cmdlet that you might use. Some of the questions below don't necessarily apply for private/helper type functions that can (and often should) be much more simplistic.

The idea for this scorecard was inspired by several others i've seen, notably the Joel Test which is a scorecard for Developers to evaluate the maturity of a workplace, as well as the Operations Report Card which similarly can be used to assess the operational sophistication of an Ops team.
