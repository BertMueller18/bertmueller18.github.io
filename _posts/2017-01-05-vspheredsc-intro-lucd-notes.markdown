---
layout: post 
title:  "vSphereDSC - Intro - LucD notes" 
date:   2017-01-05T11:06:29.200Z 
categories: psdsc vsphere vmware
link: http://www.lucd.info/2016/06/04/vspheredsc-intro/ 
tags:
  - links
ogtype: article 
---

> VSphereDSC – Intro


My attempts to marry DSC and vSphere have been going on for nearly a year* now. I showed some of my attempts and intermediate results at VMworld 2015, in two sessions at the PowerShell + DevOps Global Summit and recently during a session at the 24th VMUGBE+. But now I’m finally going public with the vSphereDSC module.

Since WMF 5 has been made available in preview, and still is in RTM at the moment I’m writing this, there have been constant changes to the way I was writing the DSC resources for vSphere. Since the February 2016 WMF 5 release, I now have a (somewhat) stable, working class-based solution. At least, that is what my initial tests seem to indicate.

