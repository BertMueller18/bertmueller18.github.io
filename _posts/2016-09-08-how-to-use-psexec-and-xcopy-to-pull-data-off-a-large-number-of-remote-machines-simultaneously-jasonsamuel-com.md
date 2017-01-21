---
layout: post
published: true
title: "How to use PsExec and Xcopy to pull data off a large number of remote machines simultaneously – JasonSamuel.com"
date: 2016-09-08T08:27:48.960Z
categories: automation powershell
link: http://www.jasonsamuel.com/2014/07/30/how-to-use-psexec-and-xcopy-to-pull-data-off-a-large-number-of-remote-machines-simultaneously/
tags:
  - links
ogtype: article
bodyclass: post
---

## How to use PsExec and Xcopy to pull data off a large number of remote machines simultaneouslyBy Jason Samuel
onJuly 30, 2014
SHARE TWEET SHARE SHARE 0 COMMENTS
My co-worker and I were in a bit of a pinch recently and had to quickly pull data off a large number of VMs as fast as possible. We had a real time crunch to get it done.



Well, Ctrl+C Ctrl+V is one way to do it but you’re better than that. The easier way is to use PsExec and Xcopy/Robocopy to do it. Getting PsExec and Xcopy to play nicely is sometimes a bit tricky. Here’s a really quick and dirty script to get it done. Not the most efficient but it will work in a pinch

1. Copy psexec into a folder on the server you plan to copy your data to. Let’s call this drive D:\DataBackup. Now share it out to Everyone with Read/Write access.

2. Create a .bat file with the following. Let’s call it remotescript.bat and let’s say you are after user profile data. So:
