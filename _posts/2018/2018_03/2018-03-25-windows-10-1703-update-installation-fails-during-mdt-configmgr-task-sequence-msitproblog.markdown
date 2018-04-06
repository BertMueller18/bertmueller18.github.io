---
layout: post 
title:  "Windows 10 1703 Update Installation fails during MDT / ConfigMgr Task Sequence - msitproblog" 
date:   2018-03-25T15:04:26.520Z 
categories: mdt deployment windows10
link: https://msitproblog.com/2017/06/08/windows-10-1703-update-installation-fails-mdt-task-sequence/ 
tags:
  - links
ogtype: article 
---

## Windows 10 1703 Update Installation fails during MDT / ConfigMgr Task Sequence Simon Dettling  8. June 2017  ConfigMgr, MDT, Windows  18 Comments
UPDATE: I’ve added some ConfigMgr / SCCM related details at the end of the blog post.

Over the last few weeks, I had an interesting issue regarding Windows 10 1703 and the Installation of Windows Updating during a Capture MDT Task Sequence.

MDT was configured to install Updates from a locally installed WSUS, which worked for Windows 7 up to Windows 10 1511. I recently started working with Windows 10 1703 and used about the same Capture Task Sequence as for Windows 10 1511. Here I had the issue, that the Reference Computer reaches the first Windows Update Step and runs into a Timeout while searching for Updates. You can leave the Computer pretty much for hours in this state without it doing anything.