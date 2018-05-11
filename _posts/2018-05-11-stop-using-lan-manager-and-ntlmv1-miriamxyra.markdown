---
layout: post 
title:  "Stop using Lan Manager and NTLMv1! | miriamxyra" 
date:   2018-05-11T08:34:20.442Z 
categories: activedirectory smb security
link: https://miriamxyra.com/2017/11/08/stop-using-lan-manager-and-ntlmv1/ 
tags:
  - links
ogtype: article 
---

## STOP USING LAN MANAGER AND NTLMV1!

When performing Security checks in customer environments I often find out that LAN Manager or NTLMv1 is still allowed. Most customers don’t know that this setting leaves the environment highly vulnerable to attacks targeting their authentication methods.

Why you should not use LAN Manager and NTLMv1 anymore you will read in this article.

What’s the problem with LAN Manager?
LAN Manager is the ‘grandpa of authentication‘ in Windows Systems. It was implemented in 1987 and nowadays it is old and deprecated. And yes of course, it can be broken easily.

This protocol is still used by Windows-NT based operating systems to store Password Hashes. And due to backward compatibility issues it is still in use: If a password is stored, which is shorter than fifteen Characters, a LM-Hash is generated and used.

A LM-Hash is NOT case-sensitive: Before creating the hash, all characters are being casted to uppercase characters. So it does not matter if upper or lower characters were used when creating the password.