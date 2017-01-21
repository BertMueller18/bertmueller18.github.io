---
layout: post
published: true
title: "Adding websites to IE zones on a XenApp server using local group policy – JasonSamuel.com"
date: 2016-09-08T08:33:15.826Z
categories: xenapp citrix internetexplorer gpo 
link: http://www.jasonsamuel.com/2012/08/15/adding-websites-to-ie-zones-on-a-xenapp-server-using-local-group-policy/
tags:
  - links
ogtype: article
bodyclass: post
---

> CITRIX XENAPPAdding websites to IE zones on a XenApp server using local group policyBy Jason Samuel
onAugust 15, 2012
SHARE TWEET SHARE SHARE 6 COMMENTS
Sometimes when working on a XenApp server and publishing websites through Internet Explorer, you may have a need to temporarily add the website to the Local Intranet or Trusted Sites zone for testing purposes. Usually NTLM passthrough windows authentication won’t work unless the website is part of the Local Intranet zone. Your users will get a popup box asking for their credentials. In multidomain environments, things can get especially hairy sometimes with the way IE detects a Local Intranet website. You can add the site manually in IE after the website has launched but it’s per profile. If you want to add it for all users on the server, group policy is the way to go. Associating a site with a zone can be accomplished through group policy at the domain level easily but sometimes you just want to test things first and it’s quicker to edit the local group policy on the server.
