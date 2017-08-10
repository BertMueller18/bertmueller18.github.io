---
layout: post
published: true
title: "mikeboers.com -- One Time Passwords for SSH on Ubuntu and OS X "
date: 2016-11-05T10:57:36.295Z
categories: ssh otp linux ubuntu mac osx
link: http://mikeboers.com/blog/2011/05/28/one-time-passwords-for-ssh-on-ubuntu-and-os-x
tags:
  - links
ogtype: article
bodyclass: post
---

## One Time Passwords for SSH on Ubuntu and OS X
I have been meaning to beef up the security on my various servers for a while. Everything was configured in a way that was relatively closed, but ultimately I decided that convenience outweighed absolute security. To that end, my passwords are not as good as they could be (ie. I can remember them easily and type them quickly (although they were designed to be...)), SSH continues to serve from the default port, and one could SSH to root just with its (enormous) password.

Walking home from the train yesterday I decided to finally fix this. My original idea was to setup a pluggable authentication module (PAM) for Steve Gibson's "Perfect Paper Passwords", but I soon discovered the (slightly more official) Initiative for Open Authentication (OATH). OATH provides specifications for two types of one time passwords (OTPs): event based (HOTP) or time based (TOTP).

Event based OTPs are generated from a counter that increments every time you ask for a password. The servers keep track of the current counter so they will never accept previous passwords again (eg. if someone watches over your shoulder or there is a key logger). Time based OTPs do much the same, except they are based off of the current time and so are only valid for the current 30 second block.

These sorts of two-factor authentication schemes often rely upon proprietary hardware and expensive service plans, but the openness of OATH allows for free apps for iOS, Android, and many more. Another open source project, OATH Toolkit, provides the server side code including a PAM.
