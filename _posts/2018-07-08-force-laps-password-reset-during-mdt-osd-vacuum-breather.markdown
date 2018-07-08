---
layout: post 
title:  "Force LAPS Password Reset during MDT OSD - Vacuum Breather" 
date:   2018-07-08T16:27:58.534Z 
categories: mdt mdt2013 deployment laps
link: https://www.vacuumbreather.com/index.php/blog/item/75-force-laps-password-reset-during-mdt-osd 
tags:
  - links
ogtype: article 
---

## Force LAPS Password Reset during MDT OSD
 Written by	Anton Romanyuk
Font Size      Print  Email  1 comment
Rate this item1 2 3 4 5 (2 votes)


My customers often send me exciting cases. This particular one is especially interesting because it is common in infrastructures that use "Local Administrator Password Solution" (LAPS) for password management. LAPS, which I can't recommend highly enough, provides management of common local administrator account by setting a different, random password on every managed domain-joined computer. The case opened when a customer contacted me a few weeks ago reporting that they experienced issues when re-installing computers using Microsoft Deployment Toolkit: after OS deployment, LAPS didn't update the local administrator password which in turn significantly increased the risk of lateral escalation (Pass-the-Hash (PtH)) that results when the same administrative local account and password combination is used. Given the importance of the customer, I immediately sat down to investigate.

In this case, the fact that stood out was that all the systems on which the problem had occurred kept their computer name and re-used computer’s corresponding Active Directory object. LAPS stores the password for each computer’s local administrator account in a confidential ms-Mcs-AdmPwd attribute in the AD, while the expiration date is written into the ms-Mcs-AdmPwdExpirationTime attribute. Re-using the computer's AD account is not a supported scenario: when MDT installs LAPS client-side extension (CSE), after the next startup or background group policy refresh (whichever comes first), the LAPS agent determines that the expiration date of the local administrator password set by the previous computer that used the AD object is within the defined threshold and does not reset password. Only when the expiration time is reached, will LAPS CSE replace local admin password.

