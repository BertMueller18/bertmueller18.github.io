---
layout: post 
title:  "Introducing Reverse DSC – Crawl, Walk, Run, Automate" 
date:   2017-12-07T07:52:49.636Z 
categories: powershell psdsc automation
link: https://nikcharlebois.com/introducing-reverse-dsc/ 
tags:
  - links
ogtype: article 
---

## Introducing Reverse DSC

 > 2016-12-13  Nik Charlebois	 Announcements, Tutorial  2,049 5 Comments

Ever since becoming a Microsoft PowerShell MVP back in the summer of 2014, I have been heavily involved with various PowerShell Desired State Configuration (DSC) projects. The main initiative I have been involved with is the SharePointDSC module which is currently led by Brian Farnhill down in Australia. While my contributions to the core of the project have been limited, I have been spending numerous hours working on a new concept I came up with and which is very close to my heart. Reverse DSC is something I introduced back in late 2015 after spending some late night hours testing out my SharePointDSC scripts. It is the concept of extracting a DSC Configuration Script out of an existing environment in order to be able to better analyze it, replicate it or onboard it onto PowerShell DSC. Let me be very clear, this concept does not only apply to the SharePoint world; it applies to all software components that can be automated via DSC. I am of the opinion that this concept will be a game changer in the world of automation, and I strongly encourage you to read through this article to better understand the core concepts behind it.