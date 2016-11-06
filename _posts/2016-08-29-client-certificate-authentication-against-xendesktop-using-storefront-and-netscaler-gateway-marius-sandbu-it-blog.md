---
layout: post 
published: true 
title: "Client Certificate authentication against XenDesktop using Storefront and NetScaler Gateway | Marius Sandbu - IT blog" 
date: 2016-08-29T03:50:26.694Z 
link: https://msandbu.wordpress.com/2016/04/22/client-certificate-authentication-against-xendesktop-using-storefront-and-netscaler-gateway/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Client Certificate authentication against XenDesktop using Storefront and NetScaler Gateway
so this is a question that I was asked the other day, and to be honest I wasn’t quite sure that this would work. I know that Smart Cards and so on works against a XenDesktop enviroment but just plain Client Certificates? not the same..

The purpose was that some admins want to have a simple way to start Citrix without the need for authentication. Now I started by setting up a Certificate policy and define the Client Cert authentication feature in the SSL profile. This gave me full authentication against NetScaler and to Storefront. The issue was when I tried to start an application, then I would get SSL errors which I have never seen before and again not so much information on Google on it. Therefore I needed to try another approach to it. Since the client certificate authentication worked internally, maybe there was an issue with NetScaler doing the authentication validation which seems to break the authentication against the VDA agent