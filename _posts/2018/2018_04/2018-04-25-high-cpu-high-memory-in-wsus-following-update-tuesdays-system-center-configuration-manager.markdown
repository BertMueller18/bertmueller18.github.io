---
layout: post 
title:  "High CPU/High Memory in WSUS following Update Tuesdays | System Center: Configuration Manager" 
date:   2018-04-25T20:51:09.146Z 
categories: wsus maintenance
link: https://blogs.technet.microsoft.com/configurationmgr/2017/08/18/high-cpuhigh-memory-in-wsus-following-update-tuesdays/ 
tags:
  - links
ogtype: article 
---

## High CPU/High Memory in WSUS following Update Tuesdays

August 18, 2017 by Jarrett Renshaw MSFT // 32 Comments

Updated 10/11/2017 – updated hotfix information.

Recently, we’ve seen an increase in the number of high CPU/High Memory usage problems with WSUS, including WSUS in a System Center Configuration Manager environment – these have mostly corresponded with Update Tuesdays.

Microsoft support has determined that the issue is driven primarily by the Windows 10 1607 updates, for example KB4022723, KB4022715, KB4025339, etc. See here for the list of Windows 10 1607 updates.

These updates have large metadata payloads for the dependent (child) packages because they roll up a large number of binaries. Windows 10, versions 1507 (Windows 10 RTM) and 1511 updates can also cause this, though to a lesser extent.  Windows 10, version 1703 is still recent enough that the metadata is not that large yet (but will continue to grow).

Symptom
The symptoms include

High CPU on your WSUS server – 70-100% CPU in w3wp.exe hosting WsusPool
High memory in the w3wp.exe process hosting the WsusPool – customers have reported memory usage approach 24GB
Constant recycling of the W3wp.exe hosting the WsusPool (identifiable by the PID changing)
Clients failing to scan with 8024401c (timeout) errors in the WindowsUpdate.log
Mostly 500 errors for the /ClientWebService/Client.asmx requests in the IIS logs
Cause
Microsoft support has determined that the issue is driven primarily by the Windows 10 1607 updates, for example KB4022723, KB4022715, KB4025339, etc. See here for the list of Windows 10 1607 updates.

These updates have large metadata payloads for the dependent (child) packages because they roll up a large number of binaries. Windows 10, versions 1507 (Windows 10 RTM) and 1511 updates can also cause this, though to a lesser extent. Windows 10, version 1703 is still recent enough that the metadata is not that large yet (but will continue to grow).