---
layout: post 
title:  "Securing your infrastructure with Just Enough Administration – miriamxyra" 
date:   2018-05-11T08:32:40.280Z 
categories: activedirectory security powershell pentest
link: https://blogs.technet.microsoft.com/miriamxyra/2018/05/10/securing-your-infrastructure-with-just-enough-administration/ 
tags:
  - links
ogtype: article 
---

## Securing your infrastructure with Just Enough Administration

Miriam WiesnerMay 10, 20181 
I was giving a talk about Just Enough Administration (JEA) at PSConfEU 2018 in Hannover and I also wanted to share my thoughts with you writing this blog post.

My PSConfEU presentation and demo code can be found on GitHub. The recording on the session will be released soon on the official PSConfEU YouTube channel (I will update this link, once the recording of my session is released).

Current Threat Landscape
When speaking to decision makers in IT, often I hear the statement "But we are having a hardware firewall and an antivirus software! Of course we are having a good security!!!".

Actually that was true fifteen years ago, but isn't anymore. Of course, firewall and antivirus vendors have secured their systems according to known threats. To breach a hardware firewall is really hard for an attacker (well, except if they have an implemented backdoor, but let's not talk about this).

So attackers moved on. Most attackers choose the easy way: They don't want to spend too much resources or time, if there are easier ways to exploit. And the easiest link in the chain is the human being, so they target the identities of an organization.

Once they find a way in, it takes only few hours to complete the attack, but several hundred days until they get detected. If they get detected.