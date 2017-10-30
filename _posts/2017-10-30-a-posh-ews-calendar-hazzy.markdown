---
layout: post 
title:  "A POSH EWS Calendar - HAZZY" 
date:   2017-10-30T17:08:37.249Z 
categories: exchange ews powershell programming
link: http://hazzy.techanarchy.net/winadmin/windows/a-posh-ews-calendar/ 
tags:
  - links
ogtype: article 
---

> A POSH EWS Calendar
by Hazzy on February 26, 2016 in Exchange, Powershell, Tips, Windows, Windows Admin • 0 Comments
Grumpy Admin here – as we know Grumpy admin isn’t one to not accept a challenge – Where it is legal and sensible.  The challenge of introducing my ex-wife to an industrial sized wood chipper was sadly rejected after a long hard consultation! I can’t create or enter a pssession from jail!

Grumpy Admin has been doing some work for a friend, and part of this work meant, using the Exchange Web Services Managed API to access mailboxes from PowerShell!

In the normal office banter way, Grumpy Admin was expressing how neat it was and useful – The others didn’t and lacked the imagination to see how useful it could actually be! So they challenged me to come with a useful usage case for this. I think they just wanted a use case, not a proof in concept but then I am Grumpy Admin and it is what I like to do!

Took me about 5 mins to think of something, that was actually useful and here was my offering to them!

We have a script that runs once a month or so – currently the script emails us when it complete with the results, which we then make an entry on to the shared calendar to show everyone that the script ran on that date.  Easy to keep track and people can see when the script ran.  There might be smarter ways of doing it, but it was in place and being done like this before my time! It is just one of the many processes I dislike! They seem to think automation is a bad thing…. Like I would replace them with a script if I could!