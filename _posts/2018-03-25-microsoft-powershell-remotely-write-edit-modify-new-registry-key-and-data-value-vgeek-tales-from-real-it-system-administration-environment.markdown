---
layout: post 
title:  "Microsoft Powershell: remotely write, edit, modify new registry key and data value | vGeek - Tales from real IT system Administration environment" 
date:   2018-03-25T15:22:41.930Z 
categories: powershell automation
link: http://vcloud-lab.com/entries/powershell/microsoft-powershell-remotely-write-edit-modify-new-registry-key-and-data-value?utm_content=buffer1dcbc&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer#.Wn8X6_7Z-oE.buffer 
tags:
  - links
ogtype: article 
---

> Microsoft Powershell: remotely write, edit, modify new registry key and data value
February 5, 2018 03:34PM
Part 1: Powershell: Get registry value data from remote computer
Part 2: Microsoft Powershell: remotely write, edit, modify new registry key and data value
Part 3: Microsoft Powershell: Delete registry key or values on remote computer

Recently I had a another requirement to write edit, modify new windows registry keys and value data on remote server using Microsoft PowerShell. Here I have used 3 scripting ways, to perform this task. This is second part of my earlier written script Powershell: Get registry value data from remote computer. This script is written using in powershell using .net registry class. This require remote registry service enabled on remote server and there should be permissions registry. For modification or editing of regedit on localhost run powershell as an administrator. here I am showing 3 methods you can achieve this taks.