---
layout: post 
title:  "	Deployment Research &gt; Research" 
date:   2018-06-07T18:04:48.207Z 
categories: certificate letsencrypt security windows server2016 server2012r2
link: https://deploymentresearch.com/Research/Post/667/Home-Lab-Options-for-free-public-TLS-SSL-Certificates-By-Adam-Gross 
tags:
  - links
ogtype: article 
---

## Home Lab: Options for free public TLS/SSL Certificates - By Adam Gross
Deployment Research
Johan Arwidmark
May
08
2018
This is a guest post graciously provided by Adam Gross (@AdamGrossTX). Thanks Adam!

 

	
Adam has been a Desktop Architecture Analyst in his day job since 2004 where he shares management duties for a ConfigMgr infrastructure which supports ~9000 clients.

While he doesn’t consider himself an expert in any field, he is proficient enough in ConfigMgr, SQL, PowerShell and C# to build creative solutions to streamline processes as part of his continual improvement strategy.

When he’s not chasing his 3 small children, he tries to give back to the systems management community through his blog http://www.asquaredozen.com and on Twitter @AdamGrossTX.

 

Home Lab: Options for free public TLS/SSL Certificates
If you’re like me, your home lab is built with leftover parts and anything you can pull together to make it happen and you likely don’t have the budget to spend on an TLS/SSL certificate, especially if you only need to use it on occasion to test a few things. While using a self-signed certificate works for many things, I recently found that some automated processes don’t work because they can’t validate a self-signed certificate. In my case it was Windows 10 AutoPilot user authentication using AD FS. I know I could have chosen a different authentication option for AutoPilot, but I really wanted to test with AD FS, so I went looking and found some free options.

