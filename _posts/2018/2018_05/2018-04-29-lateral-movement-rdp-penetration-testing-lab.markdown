---
layout: post 
title:  "Lateral Movement – RDP | Penetration Testing Lab" 
date:   2018-04-29T07:31:14.427Z 
categories: windows rdp rdsh pentest security
link: https://pentestlab.blog/2018/04/24/lateral-movement-rdp/ 
tags:
  - links
ogtype: article 
---

## Lateral Movement – RDP
April 24, 2018
netbiosX	Red Team	Mimikatz, MiTM, RDP, RDP Inception, RDP Session Hijacking, Red Team	Leave a comment

The Remote Desktop Protocol (RDP) is widely used across internal networks by Administrators. This allows systems owners and admins to manage Windows environments remotely. However RDP can give various opportunities to an attacker to conduct attacks that can be used for lateral movement in red team scenarios. The attacks below can allow the red team to obtain credentials, to hijack RDP sessions of other users and to execute arbitrary code to remote systems that will use RDP as authentication mechanism to infected workstations.