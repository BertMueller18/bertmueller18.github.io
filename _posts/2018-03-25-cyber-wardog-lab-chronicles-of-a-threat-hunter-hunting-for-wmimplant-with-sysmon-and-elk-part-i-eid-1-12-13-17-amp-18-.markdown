---
layout: post 
title:  "Cyber Wardog Lab: Chronicles of a Threat Hunter: Hunting for WMImplant with Sysmon and ELK - Part I (EID 1,12, 13, 17 &amp; 18)" 
date:   2018-03-25T15:52:25.950Z 
categories: sysmon elkstack pentest 
link: https://cyberwardog.blogspot.de/2017/03/chronicles-of-threat-hunter-hunting-for_26.html?m=1 
tags:
  - links
ogtype: article 
---

> Chronicles of a Threat Hunter: Hunting for WMImplant with Sysmon and ELK - Part I (EID 1,12, 13, 17 & 18)

It was a normal day at work when all of the sudden I see the following on Twitter 



 



Apparently this new WMI RAT runs perfectly fine on Device Guard-enabled systems! It was Game ON ! I got very excited to test this tool BUT only to see how I could hunt for it, of course. Even though there might be different ways to detect the behavior of this new tool, I decided to use the tools I have been playing with for the past couple of months, Sysmon & ELK. 



Requirements: