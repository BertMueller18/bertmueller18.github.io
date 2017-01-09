---
layout: post 
title:  "Windows 7 refreshed media creation – The Windows Deployment Guy" 
date:   2017-01-09T15:53:04.559Z 
categories: windows7 deployment
link: https://blogs.technet.microsoft.com/astoica/2017/01/03/windows-7-refreshed-media-creation/ 
tags:
  - links
ogtype: article 
---

> Windows 7 refreshed media creation
★★★★★★★★★★★★★★★
Andrei StoicaJanuary 3, 201732 
66
0
The fastest way to patch a Windows 7/Server 2008 R2 machine is to take advantage of the Convenience Update Rollup from April 2016 (KB3125574). The Conv. UR updates a lot of components and to ensure that that happens without any servicing problems, it has as a prerequisite the Servicing Stack Update from April 2015 (KB3020369). To install most of the other patches in between April 2016 and October 2016 we will include the following updates:

KB3020369 (April 2015 Servicing Stack Update)
KB3125574 (April 2016 Convenience Update Rollup)
KB3177467 (September 2016 SSU)
KB3172605 (July 2016 Functional Update Rollup, 7C* package)
KB3179573 (August 2016 FUR, 8C* package)
KB2841134 (Internet Explorer 11, Optional)
KB3185330 (October 2016 Monthly Quality Rollup, 10B’ package [contains September 2016 FUR, 9C* package])