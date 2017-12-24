---
layout: post 
title:  "Image Factory Automation | Keith's Consulting Blog" 
date:   2017-12-24T10:13:42.763Z 
categories: mdt wsus automation imagefactory
link: https://keithga.wordpress.com/2014/05/27/image-factory-automation/ 
tags:
  - links
ogtype: article 
---

> Image Factory Automation
One area where MDT Litetouch excels is with Image Creation. I know of several groups within Microsoft (including Microsoft Consulting) who recommend using MDT LiteTouch to create images, even if those images are eventually used within SCCM OSD (Operating System Deployment).

Background
Back in the Windows XP days, the OS came with it’s own proprietary installation system. Say you spent some time getting XP updated to the latest Service Pack, along with all the necessary security updates, and the latest version of Office. You might want to take a snapshot (or checkpoint) of this reference disk (Image) to reload on other machines. That’s where Sysprep and 3rd party products like Ghost came to the picture.

Starting with Windows Vista, Microsoft started distributing the OS using a new file archival format: Windows Imaging Format (*.wim files). *.wim files are compressed archives with space to store extra metadata. It’s also intelligent to hold multiple archive sets within a single *.wim file, and only keep a single instance of the same file, so a single wim file can hold Windows Starter, Home Premium, and Ultimate on the same disk!

The main difference between Ghost (*.gho) files, and WIM (*.wim) files is that Ghost Files store the contents of a hard disk in block format (partitions and all), whereas the WIM files are stored as files. That means that when you apply a *.gho file to a disk of different size, Ghost itself needs to do some resizing of the partitions to make it fit. Whereas the *.wim file can only hold those files and streams it knows about (boot sectors and deleted files are ignored).

One of the coolest features of *.wim files is that Microsoft allows customers the ability to capture the contents of a Drive (volume) into your own *.wim file. In fact for some versions of Windows, you can replace the install.wim file on the Install DVD with your own captured *.wim file, and continue with the installation process like it came from Microsoft.