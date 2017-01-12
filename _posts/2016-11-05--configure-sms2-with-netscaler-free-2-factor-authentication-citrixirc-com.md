---
layout: post
published: true
title: "  Configure SMS2 with Netscaler (Free 2 Factor Authentication) » Citrixirc.com"
date: 2016-11-05T10:27:15.544Z
categories: netscaler 2fa mfa citrix 
link: http://www.citrixirc.com/?p=485
tags:
  - links
ogtype: article
bodyclass: post
---

#Configure SMS2 with Netscaler (Free 2 Factor Authentication)#

EDIT:  People have been requesting a tool to deploy SMS2 secret keys en mass, and the developer hasn’t implemented it yet.  Until he does I wrote a powershell script that will remotely connect to the sql database and inject the information needed for each user you select (http://pastebin.com/NBJHJPsX).  I have it setup for TOTP keys… which I think is what most people will use.
EDIT2:  I created a new script that does basically the same thing as the script posted above, but you can direct it against a specific AD group (http://pastebin.com/L9D8Jwaf).  Also, if you haven’t yet – upgrade your netscalers to version 11 – much easier to control the portal themes.
