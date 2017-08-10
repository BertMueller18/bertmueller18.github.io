---
layout: post 
published: true 
title: "How to Setup a Multi-Protocol VPN Server Using SoftEther | DigitalOcean" 
date: 2016-09-28T09:33:06.687Z 
categories: von linux ipsec opnvpn 
link: https://www.digitalocean.com/community/tutorials/how-to-setup-a-multi-protocol-vpn-server-using-softether 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> How to Setup a Multi-Protocol VPN Server Using SoftEther
Posted Nov 19, 2013 213.1k views Security Networking Ubuntu
Introduction

This article explains how to install and configure a multi-protocol VPN server using the SoftEther package. We enable and configure OpenVPN and L2TP over IPSec and SSTP VPN Servers on Linux.

What is SoftEther
SoftEther VPN is one of the world's most powerful and easy-to-use multi-protocol VPN software, made by the good folks at the University of Tsukuba, Japan. It runs on Windows, Linux, Mac, FreeBSD and Solaris and is freeware and open-source. You can use SoftEther for any personal or commercial use free of charge.

Step 1: Create a Virtual Server
First, you need to create a DigitalOcean Droplet. As mentioned in SoftEther's website, SoftEther will work on almost every Linux distro with kernel v2.4 or above,; however it's recommended to choose one of these distributions: CentOS, Fedora, or Red Hat Enterprise Linux.

Personally I have tried it on Ubuntu, CentOS and Fedora, both 32 and 64 bit editions, and it has worked perfectly.