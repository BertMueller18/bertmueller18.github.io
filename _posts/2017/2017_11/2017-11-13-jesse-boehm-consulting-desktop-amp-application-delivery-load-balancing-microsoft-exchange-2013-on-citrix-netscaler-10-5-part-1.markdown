---
layout: post 
title:  "Jesse Boehm Consulting - Desktop &amp; Application Delivery |   load-balancing-microsoft-exchange-2013-on-citrix-netscaler-10-5-part-1" 
date:   2017-11-13T21:48:19.220Z 
categories: citrix netscaler exchange loadbalancer
link: http://www.jesseboehmconsulting.com/load-balancing-microsoft-exchange-2013-on-citrix-netscaler-10-5-part-1/ 
tags:
  - links
ogtype: article 
---

> INTRODUCTION
Load Balancing Microsoft Exchange 2013 on Citrix NetScaler 10.5
I have read a lot of information on the internet about Load Balancing Exchange 2013 on Citrix NetScaler including the document from Citrix on how to Load Balance Exchange on NetScaler, which doesn’t work at all. Now there is a world of information out there and if you search you may compile many web pages that will help you each step of the way till you configure Exchange 2013 on NetScaler. I think I used 30+ sources some totally unrelated NetScaler or Exchange 2013 to compile my information and put this Article together.

So my idea with this article is to create a single source point of reference on how to do this setup from start to finish.

I caveat that there is many ways to do things. I am not an Exchange 2013 Expert. But I learned a lot through this process.

I found this method with NetScaler was the best approach. I did not find the Content Switching Method used in Exchange 2010 with NetScaler Valid. This was also the way the Citrix eDocs suggested this to be done. I could find absolutely no value in this method so I did not use it. Almost everything in Exchange runs on port 443 so to separate the Services like the Citrix eDocs seemed not required. That being said, this document is an absolute work in progress and I welcome any feedback to improve this document. So if the GURUs in the world have suggestions for Addendums to this Article I welcome the feedback.

There are many articles out there for Exchange 2010 with NetScaler. Replacing TMG 2010 with NetScaler. All of which I find do not really apply with Exchange 2013.

My goal in this document is to do the following

Configure the Exchange Components so they are ready for the NetScaler Load Balancing
Add Exchange Servers to the NetScaler for Load Balancing
Create and SSL_BRIDGE Service Group
Load Balance all SSL Traffic, including OWA through an SSL Load Balanced VIP
Redirect HTTP to HTTPS
Create a Managed Availability Monitor for Exchange SSL Traffic
Create an HTTP to HTTPS Redirect for Autodiscover
Pass the Microsoft Exchange ActiveSync Connectivity Tests
Test our setup with Auto Config of Outlook with and Exchange Account
This will take us through Outlook Anywhere for Exchange 2013 and Part 1 of my Exchange 2013 Deployment Guide for NetScaler