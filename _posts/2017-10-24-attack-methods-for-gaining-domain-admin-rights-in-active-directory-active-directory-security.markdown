---
layout: post 
title:  "Attack Methods for Gaining Domain Admin Rights in Active Directory – Active Directory Security" 
date:   2017-10-24T06:34:13.757Z 
categories: activedirectory pentest
link: https://adsecurity.org/?p=2362#more-2362 
tags:
  - links
ogtype: article 
---

> Attack Methods for Gaining Domain Admin Rights in Active Directory
ActiveDirectorySecurity, Microsoft Security, Technical Reference by Sean Metcalf
There are many ways an attacker can gain Domain Admin rights in Active Directory. This post is meant to describe some of the more popular ones in current use. The techniques described here “assume breach” where an attacker already has a foothold on an internal system and has gained domain user credentials (aka post-exploitation).
The unfortunate reality for most enterprises, is that it often does not take long from an attacker to go from domain user to domain admin. The question on defenders’ minds is “how does this happen?”.
The attack frequently starts with a spear-phishing email to one or more users enabling the attacker to get their code running on a computer inside the target network. Once the attacker has their code running inside the enterprise, the first step is performing reconnaissance to discover useful resources to escalate permissions, persist, and of course, plunder information (often the “crown jewels” of an organization).