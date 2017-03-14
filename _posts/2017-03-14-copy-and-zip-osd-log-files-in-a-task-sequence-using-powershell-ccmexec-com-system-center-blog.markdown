---
layout: post 
title:  "Copy and Zip OSD log files in a Task Sequence using Powershell - CCMEXEC.COM – System Center blog" 
date:   2017-03-14T21:53:40.793Z 
categories: mdt 
link: http://ccmexec.com/2017/03/copy-and-zip-osd-log-files-in-a-task-sequence-using-powershell/ 
tags:
  - links
ogtype: article 
---

> Copy and Zip OSD log files in a Task Sequence using Powershell
March 3, 2017Jörgen Nilsson
No comments
My college Johan Schrewelius wrote a script to copy log files from OSD to a network share like the functionality we have in MDT so I thought I would post it here as it is brilliant. It can be downloaded here: https://gallery.technet.microsoft.com/Script-to-Zip-and-copy-c37c4c8e

The script “CopyOSDLogs.ps1” can be run anywhere in an OSD TS but is most often used in the Error Section, thus only run in case of a failed deployment. I wrote a post here a while ago as well on how to add some basic error handling in a standalone TS.

http://ccmexec.com/2016/12/error-handling-in-ts-without-mdt-using-osdbackground/

There are a couple of pre-requisites to make it work:

·         We need to make sure that Powershell support is added to our Boot image.

·         We need a location (file share) to save the logs.

·         A TS Variable holding the UNC path to the share.

·         The “First” Network Access Account must be granted “Modify” permissions on the share.

Make sure that Powershell is added to the boot image by adding it if it isn’t added already.