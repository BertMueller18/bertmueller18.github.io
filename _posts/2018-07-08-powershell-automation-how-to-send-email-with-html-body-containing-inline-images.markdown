---
layout: post 
title:  "PowerShell Automation - How To Send Email With HTML Body Containing Inline Images" 
date:   2018-07-08T15:56:07.670Z 
categories: powershell automation
link: https://www.c-sharpcorner.com/article/powershell-automation-how-to-send-email-with-html-body-containing-inline-images/ 
tags:
  - links
ogtype: article 
---

> 	
PowerShell Automation - How To Send Email With HTML Body Containing Inline Images
  Prashant Bansal Jun 29 2018 Article
1 0 1.2k
facebook
twitter
linkedIn
google Plus
Reddit
Expand
Download Free Office API
During a recent assignment I got an automation requirement to send formatted emails daily to a set of users.

The email content involved the HTML formatting with a lot of images as a part of the layout. I have appointed PowerShell as the automation technology to get this done.

I felt it would be worth writing a small article to explain the code (which is interesting) to embed images within the outgoing email content.

Now to start with a demo, say we have to send an email with Health of Weekly Sales Card for an online shopping store every week on Monday.

This email would look like the one in the following screenshot,