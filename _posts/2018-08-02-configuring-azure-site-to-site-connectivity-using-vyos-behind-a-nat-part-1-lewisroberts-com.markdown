---
layout: post 
title:  "Configuring Azure Site-to-Site Connectivity using VyOS behind a NAT – Part 1 - lewisroberts.com" 
date:   2018-08-02T20:04:46.661Z 
categories: vyos azure vpn ipsec
link: https://www.lewisroberts.com/2015/07/15/configuring-azure-site-to-site-connectivity-using-vyos-behind-a-nat-part-1/ 
tags:
  - links
ogtype: article 
---

## Configuring Azure Site-to-Site Connectivity using VyOS behind a NAT – Part 1
BY LEWIS · WED 15TH JULY, 2015

Introduction
This series of posts will cover the process of creating a Site-to-Site VPN from your on-premises network infrastructure in to Azure IaaS services using VyOS, hosted in a virtual machine. Typically, this results in the “hybrid” model that Microsoft are keen for you to take advantage of when you’re investing in your infrastructure. If you’re asking yourself “Why would I do this?” The answer is: to permit your business to take advantage of the benefits offered by cloud IaaS services such as giving you the ability to spin up virtual machines (VMs) quickly and easily, without the normal associated costs (in terms of both financial and time) typically involved in procuring the hardware, configuring, installing, licencing and finally, commissioning it. In short, if you want to add infrastructure to your existing network and you need it quickly, the cloud is the way to go. Think of the benefits of deploying development environments which can be spun down at the end of the day – no more power, cooling etc. to pay for and better still, you haven’t forked out for new (or had to recycle old) kit.