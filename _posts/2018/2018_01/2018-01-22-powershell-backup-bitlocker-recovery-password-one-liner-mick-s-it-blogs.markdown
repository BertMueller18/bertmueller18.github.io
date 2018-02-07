---
layout: post 
title:  "PowerShell Backup Bitlocker Recovery Password One-Liner ~ Mick's IT Blogs" 
date:   2018-01-22T22:52:23.466Z 
categories: bitlocker mbam powershell
link: https://mickitblog.blogspot.de/2018/01/powershell-backup-bitlocker-recovery.html?spref=tw 
tags:
  - links
ogtype: article 
---

## PowerShell Backup Bitlocker Recovery Password One-Liner
Mick Pletcher  9:09 PM    No comments
While writing the solution for a secure and safe deployment of BIOS updates, I had to come up with a one-liner to backup the Bitlocker recovery password to a file named <computer name>.txt in a secured UNC path. Yes, we already have MBAM, but I wanted an extra layer of safety in the event something went wrong when applying the BIOS updates to the Bitlockered machines, thereby requiring the recovery password. Also, there are a lot of admins who work at companies which do not have products such as SCCM and MBAM. The reason the PowerShell Bitlocker CMDLETS were not used is that this is designed to run on Windows 7, 8, 8.1, and 10 operating systems.
