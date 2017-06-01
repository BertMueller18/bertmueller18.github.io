---
layout: post 
title:  "Send As, Send on Behalf of and permutations | Blog" 
date:   2017-06-01T22:34:03.974Z 
categories: exchange exchange2013 sharedmailbox
link: http://www.michev.info/Blog/Post/1430/send-as-send-on-behalf-of-and-permutations 
tags:
  - links
ogtype: article 
---

> Send As, Send on Behalf of and permutations
Posted on February 21, 2014 by Vasil Michev
Send As/Send on Behalf of permissions can be a bit confusing from time to time. What’s making them even more confusing for people is the way clients handle permissions. The ‘source of authority’ for permissions is the Global Address List, so it makes a lot of difference whether the client is using the GAL or a offline copy of it. I will try to illustrate this with several examples.

Lets start with how OWA handles things, which is the simplest case. As it is directly connected to the server, it works with the GAL and is always up to date with the latest changes (this is one of the reasons why we always ask the user to reproduce any permissions related issue in OWA). If you try to send a message as a different recipient, and you have no permissions to do so, you will be greeted by the following message:

