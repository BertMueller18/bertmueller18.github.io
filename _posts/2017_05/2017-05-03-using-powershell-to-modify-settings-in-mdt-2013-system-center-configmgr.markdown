---
layout: post 
title:  "Using PowerShell to modify settings in MDT 2013 – System Center ConfigMgr" 
date:   2017-05-02T22:15:16.678Z 
categories: mdt deployment powershell mdt2013
link: http://www.scconfigmgr.com/2014/08/23/using-powershell-to-modify-settings-in-mdt-2013/ 
tags:
  - links
ogtype: article 
---

> Using PowerShell to modify settings in MDT 2013

Nickolaj AndersenAugust 23, 2014

3
During the development phase of my new tool that I will be releasing very soon, I had to find ways to amend and modify various settings in MDT. For instance if you’d like to add a line to the CustomSettings.ini by using PowerShell, combining Get-Content with Select-String is a great idea. In this post I will go through the various settings modifications that I used during the development of my new tool. As you may know from previous experience with MDT, everything can be changed and configured from the Deployment WorkBench. But in order to script these changes, we need to deep into various methods. I’ve divided this post into three main sections:

Retrieve data from a XML file
Modify a XML file
Modify CustomSettings.ini