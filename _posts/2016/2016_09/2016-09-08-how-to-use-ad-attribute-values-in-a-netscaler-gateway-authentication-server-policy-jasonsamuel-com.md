---
layout: post
published: true
title: "How to use AD attribute values in a NetScaler Gateway authentication server policy – JasonSamuel.com"
date: 2016-09-08T08:26:52.514Z
categories: citrix netscaler activedirectory security 
link: http://www.jasonsamuel.com/2015/03/02/how-to-use-ad-attribute-values-in-a-netscaler-gateway-authentication-server-policy/
tags:
  - links
ogtype: article
bodyclass: post
---

> How to use AD attribute values in a NetScaler Gateway authentication server policyBy Jason Samuel
onMarch 2, 2015
SHARE TWEET SHARE SHARE 1 COMMENT


Did you know you can authenticate a user on a NetScaler Gateway using an Active Directory object attribute value? I’ve covered NetScaler Gateway authentication using security group extraction or by the OU the user ID is in before here in my “How to setup Citrix Netscaler (Access Gateway) with multiple domains for web browsers and mobile devices” article:

http://www.jasonsamuel.com/2013/05/09/how-to-setup-citrix-netscaler-access-gateway-with-multiple-domains-for-web-browsers-and-mobile-devices/

Those are really common methods at most companies to allow authentication on your NetScaler Gateway. But what happens if your users are in multiple root level OUs and they are not in any kind of common security group that allows NetScaler Gateway access? Many large companies have users in many different security groups and doing this can cause token size bloat which is a huge headache for your AD admins to deal with:
