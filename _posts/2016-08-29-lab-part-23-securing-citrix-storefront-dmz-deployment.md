---
layout: post 
published: true 
title: "Lab: Part 23 - Securing Citrix StoreFront DMZ deployment" 
date: 2016-08-29T03:49:18.023Z
categories: citrix storefront
link: http://www.citrixguru.com/2016/06/15/lab-securing-citrix-storefront-dmz-deployment/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Lab: Part 23 - Securing Citrix StoreFront DMZ deployment

 It’s been a while since CitrixGuru posted a lab article, but we are excited to go in depth with StoreFront once again, this time exploring DMZ implementation.

Most large organizations protect their internal network using a DMZ. The purpose of having a DMZ is to secure access (usually from the Internet) to the internal network. Any potentially vulnerable service that is being provided to users on the external network can be placed in the DMZ and will have limited connectivity with the internal network. Citrix services, such as our beloved Web Interface and his little brother StoreFront, are often used alongside NetScaler Gateway to provide remote access for corporate users.

Citrix recently released StoreFront 3.6, bringing back non-domain deployment which removes the need to have a specific Active Directory Domain in the DMZ. Previously, StoreFront DMZ implementation was a pain-in-the-you-know-what because SFT servers had to be members of an AD domain, but now StoreFront servers can be standalone in a WORKGROUP configuration. They will not sync their configurations, but will act the same way as Web Interface 5.x servers, delegating the authentication to the controllers located in the LAN. In that case, it is important to secure XML/STA communication between the two zones with HTTPS.

I’ve seen many articles online dealing with DMZ implementation and most of them leave the Web servers in the LAN, which does not fit the needs of large organizations.

In this article, we will review the most common DMZ architecture with two firewalls (between Internet/DMZ and between DMZ/LAN). Citrix StoreFront servers and NetScaler VPX appliances will be located in the DMZ, XenDesktop controllers and application servers in the LAN. Let’s get to it.

