---
layout: post 
title:  "Shadow Admins - The Stealthy Accounts That You Should Fear The Most - CyberArk" 
date:   2017-06-22T22:05:29.585Z 
categories: activedirectory security 
link: https://www.cyberark.com/threat-research-blog/shadow-admins-stealthy-accounts-fear/ 
tags:
  - links
ogtype: article 
---

## Shadow Admins – The Stealthy Accounts That You Should Fear The Most


June 8, 2017 | Advanced Attack Techniques, Credential Theft | Asaf Hecht
Shadow Admin accounts are accounts in your network that have sensitive privileges and are typically overlooked because they are not members of a privileged Active Directory (AD) group. Instead, Shadow Admin accounts were granted their privileges through the direct assignment of permissions (using ACLs on AD objects).

From the attacker’s perspective, these accounts are highly desired because they provide the administrative privileges necessary to advance an attack, and they have a lower profile compared to accounts under the well-known admin groups (ex: Domain Admins).

To maintain a strong security posture, CyberArk Labs highly recommends that organizations get to know all of the privileged accounts in the network, including those Shadow Admins. For that reason, we developed a special tool that scans and discovers privileged accounts based on account permissions. The tool, ACLight, is available for free on GitHub and can be used to discover these Shadow Admin accounts on your network today. You can find ACLight here.