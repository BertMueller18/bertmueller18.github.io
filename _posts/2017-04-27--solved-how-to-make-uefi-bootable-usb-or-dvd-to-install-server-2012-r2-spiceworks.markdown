---
layout: post 
title:  "[SOLVED] How to make UEFI bootable USB or DVD to install Server 2012 R2 - Spiceworks" 
date:   2017-04-27T06:42:21.213Z 
categories: deployment usb windows uefi diskpart dism
link: https://community.spiceworks.com/topic/762943-how-to-make-uefi-bootable-usb-or-dvd-to-install-server-2012-r2 
tags:
  - links
ogtype: article 
---

## UEFI Bootable Stick with Diskpart
I believe to make a usb bootable for UEFI it has to be FAT32

So you could open CMD and run this:

diskpart

list disk

select disk # (# is the value that represents your USB)

clean

create partition primary

select partition 1

format fs=fat32 quick

active

exit

## Alternatively create with powershell
get-disk
clear-disk #Nr -removeData
new-partition -disknumber 1 -isActive:$true -AssignDriverLetter -UseMaximumSize
format-volume -driveletter f -filesystem fat32



## Splitting large WIM-File

See Also: [http://www.zdnet.de/88280665/windows-server-2016-mit-usb-stick-installieren/]
Copy ISO Content in Folder

start command
Dism /Split-Image /ImageFile:f:\sources\install.wim /SWMFile:c:\temp\install.swm /FileSize:4000

make new iso booable with tool from ADK
First DVD:
oscdimg -n -m –b“C:\Program Files (x86)\Windows Kits\10\Assessment and Deployment Kit\Deployment Tools\x86\Oscdimg\etfsboot.com“ C:\temp\cd1\source C:\temp\cd1\cd1.iso
Second DVD
oscdimg -n C:\temp\cd2\source C:\temp\cd2\cd2.iso



