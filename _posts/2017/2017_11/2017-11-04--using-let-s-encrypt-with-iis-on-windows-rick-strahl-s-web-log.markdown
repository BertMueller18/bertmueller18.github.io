---
layout: post 
title:  "	Using Let's Encrypt with IIS on Windows - Rick Strahl's Web Log" 
date:   2017-11-04T22:19:03.807Z 
categories: certificates pki windows iis letsencrypt
link: https://weblog.west-wind.com/posts/2016/Feb/22/Using-Lets-Encrypt-with-IIS-on-Windows 
tags:
  - links
ogtype: article 
---

## Using Let's Encrypt with IIS on Windows
 February 22, 2016 - from Maui, HI
 58 comments     
Let's Encrypt is a new open source certificate authority that promises to provide free SSL certificates in a standardized, API accessible and non-commercial way. If you've installed SSL certificates in the past, you're probably familiar with the process of signing up for a certificate with some paid for provider and then going through the manual process of swapping certificate requests and completed requests.

Let's Encrypt is based on set of open service APIs that can be implemented on any platform and create certificates for Web servers including IIS. This seems like a fabulous idea, given that securing your site if you have any sort of authenticated access is an absolute requirement. It's not so much the money that's a problem since basic SSL certificates these days even from paid providers are relatively cheap (I use DnSimple both for domain management and SSL certificates), but the fact that you can completely automate the process of SSL creation and management is a huge win. This has both upsides and downsides actually and I'll talk about that at the end of the article. To be clear – I'm not a network admin and I don't have extensive experience managing certificates on a large number of sites so in this post I cover a few basic scenarios that I deal with in my own sites hosted on my own hosted servers.