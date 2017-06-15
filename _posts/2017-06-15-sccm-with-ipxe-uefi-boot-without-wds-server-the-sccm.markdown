---
layout: post 
title:  "SCCM with iPXE UEFI boot without WDS server | The SCCM" 
date:   2017-06-15T12:31:38.977Z 
categories: ipxe tinypxe win10 deployment
link: http://www.thesccm.com/ipxe-sccm/ 
tags:
  - links
ogtype: article 
---

## Prepare Tiny PXE Server (example Windows 10)

Download Tiny PXE server. http://reboot.pro/files/file/303-tiny-pxe-server/   (the link is quite slow, maynot work sometimes)
Create C:\TFTPD folder, copy unziped tiny pxe server files to C:\TFTPD
Create C:\TFTPD\iPXE folder
Mount the SCCM boot media iso file or unzip it, copy everything to C:\TFTPD\iPXE
copy modified boot.wim from “Prepare the boot.wim” to C:\TFTPD\iPXE\sources folder, overwrite the original boot.wim
Download http://git.ipxe.org/releases/wimboot/wimboot-latest.zip, unzip it, copy only wimboot file to C:\TFTP\iPXE folder
Create install.ipxe file in C:\TFTPD\iPXE folder

