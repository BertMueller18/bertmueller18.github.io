---
layout: post 
title:  "Convert, Resize, and Optimize VHD and VHDX files with PowerShell – Mike F Robbins" 
date:   2017-03-24T15:47:21.666Z 
categories: hyper-v powershell
link: http://mikefrobbins.com/2017/03/23/convert-resize-and-optimize-vhd-and-vhdx-files-with-powershell/ 
tags:
  - links
ogtype: article 
---

> Convert, Resize, and Optimize VHD and VHDX files with PowerShell

MIKE F ROBBINS MARCH 23, 2017 0
I recently received an email from someone who attended one of my presentations asking if I had a blog article on using PowerShell to compact and optimize VHD files. Since I didn’t have a blog article on that subject, I decided to create one.

The process itself is fairly simple. The examples shown in this blog article are being run on a Windows 10 computer which has Hyper-V enabled on it. Only specific SKU’s of Windows 10 are capable of running Hyper-V. The same process can be used on servers running Windows Server 2012 R2 or Windows Server 2016 (and possibly on other versions, but I can’t confirm that).