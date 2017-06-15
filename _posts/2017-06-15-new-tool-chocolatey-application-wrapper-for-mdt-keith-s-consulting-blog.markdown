---
layout: post 
title:  "New Tool: Chocolatey Application Wrapper for MDT | Keith's Consulting Blog" 
date:   2017-06-15T08:58:47.519Z 
categories: deployment win10 mdt2013 chocolatey
link: https://keithga.wordpress.com/2014/11/25/new-tool-chocolatey-wrapper-for-mdt/ 
tags:
  - links
ogtype: article 
---

## New Tool: Chocolatey Application Wrapper for MDT

I’ve been spending some time recently working on my own private Deployment Share, one of the downsides is the overhead of keeping my application packages up to date. The worst offenders are of course Google Chrome, and the Adobe Flash and PDF readers, seems like these packages are constantly changing, and I need to find and update frequently. If only there was a better way, something to make adding packages easier like my Dell Driver Pack Update tool, or the ZTIWindowsUpdate.wsf script found in MDT to run Windows Update/WSUS. Any way to keep my environment up to date without the manual hassle. :^)

There are several tools out there on the internet that help and assist you with application package management. At first I started looking at Ninite.com, however their tools are designed for End Users, and if you want to have an automated solution (like I need), then you must pay a per-machine licensing fee. (yuck)

Then I started looking at Chocolatey, which provides a command line interface for installing programs similar to Ninite.com without the UI fluff. I come across a couple of packages that were found in Ninite but not found in Chocolatey, but that list is small: (Google Talk, AIM, Yahoo!, KMPlayer, Winamp, K-Lite Codecs, Mozy, RealVNC) and the list of packages found in Chocolatey is very large. Cool!

Anther advantage of Chocolatey is that it’s in alignment with future Microsoft plans around packaging (see OneGet). However Oneget still requires some installation overhead that I didn’t want to deal with for this release, so something for the future.

So I spent some time experimenting, reverse engineering Chocolatey and scripting a workable solution, and I think I have something ready for use.