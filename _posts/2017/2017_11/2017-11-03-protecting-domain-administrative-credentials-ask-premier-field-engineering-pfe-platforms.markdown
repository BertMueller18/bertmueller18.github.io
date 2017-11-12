---
layout: post 
title:  "Protecting Domain Administrative Credentials | Ask  Premier Field Engineering (PFE)  Platforms" 
date:   2017-11-03T13:27:42.344Z 
categories: activedirectory security 
link: https://blogs.technet.microsoft.com/askpfeplat/2017/10/31/protecting-domain-administrative-credentials/ 
tags:
  - links
ogtype: article 
---

 Protecting Domain Administrative Credentials
October 31, 2017 by BrandonWilson // 1 Comments

Hello, Paul Bergson back again with today’s topic of preventing your Domain Administrators and other privileged identities from logging into Tier 1 and Tier 2 devices.

Credential theft protection is always an important step in protecting the enterprise. While your administrators are your most trusted employees within the IT enterprise, they may not always use good judgment when doing day to day tasks. ALL privileged users should have at least two accounts, one for daily tasks which need internet and e-mail access and one or more privileged accounts that are used to performed tasks which require elevated permissions and should have no access to internet or e-mail. In the case of Tier 0 accounts, they should only be authenticating to Tier 0 assets. Beyond the expectation that these elevated user accounts should not be used to log on to lower Tier assets, protection measures should be put in place to guard against administrators who want to take short cuts to get the job done quickly.

What are Tier’d devices you as