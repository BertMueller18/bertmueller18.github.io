---
layout: post 
title:  "[SOLVED] Install TCP/IP printers on many computer - Spiceworks" 
date:   2017-09-18T13:13:35.665Z 
categories: deployment vbscript driver printer
link: https://community.spiceworks.com/topic/719226-install-tcp-ip-printers-on-many-computer 
tags:
  - links
ogtype: article 
---

 It should work as long as the driver does not throw any UI.

If you run into an issue installing the driver, stage it to the store using pnputil.exe.

Steps

Add port

cscript C:\windows\system32\printing_admin_scripts\en-us\prnport.vbs -a -r "IP_192.168.15.1" -h 192.168.15.1 -o raw -n 9100

Stage driver

pnputil -a C:\Lexmark\LMUD1o40.inf

Add printer  (printui will add the driver to spooler process when it exists in the driverstore)

printui /q  /if /b "Printer Name" /r "IP_192.168.15.1" /m "Lexmark Universal v2"﻿

View this "Best Answer" in the replies below »