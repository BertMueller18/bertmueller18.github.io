---
layout: post 
title:  "How to Deploy your ‘Cloud-Only’ RDS environment – Part 5 - The Microsoft Workplace Blog" 
date:   2016-12-08T13:34:56.635Z 
categories: rds azure cloud
link: http://www.vroege.biz/?p=2844 
tags:
  - links
ogtype: article 
---

> HOW TO DEPLOY YOUR ‘CLOUD-ONLY’ RDS ENVIRONMENT – PART 5
Standard
After my visit of MVP Summit and speaking on ExpertsLive I’ve finally some time to produce some blogposts which were staying @ the backlog of my blog. Starting with the last part in the series ‘how to deploy your cloud-only RDS environment’. In part 1 till 4 the environment is described and also the instructions how to create the same environment in your own subscription. In this last blogpost I’m describing how to deploy the RDS environment with a Azure ARM template. In part 3 and 4 I already explained the scripts used by the template to deploy a Storage Spaces Direct cluster and the Remote Desktop Services environment. With a Azure ARM template we can deploy all the needed resources on Azure and also execute the scripts on these servers.