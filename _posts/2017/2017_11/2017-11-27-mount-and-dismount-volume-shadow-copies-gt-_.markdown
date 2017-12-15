---
layout: post 
title:  "Mount and dismount volume shadow copies | &gt;_" 
date:   2017-11-27T21:53:15.457Z 
categories: powershell vss backup
link: https://p0w3rsh3ll.wordpress.com/2014/06/21/mount-and-dismount-volume-shadow-copies/ 
tags:
  - links
ogtype: article 
---

## Mount and dismount volume shadow copies

Posted on June 21, 2014
Volume shadow copies can help you to:

recover a file, a directory or a volume, or Windows
find additional artifacts when conducting a live incident response.
It may be worth reading VISTA and Windows 7 Shadow Volume Forensics

etc.
All the demos, I’ve seen so far were using the built-in DOS mklink command to mount a volume shadow copy and vssadmin to list shadow copies. While playing with vssadmin, I’ve found a use of case of the context parameter of the Select-String cmdlet.