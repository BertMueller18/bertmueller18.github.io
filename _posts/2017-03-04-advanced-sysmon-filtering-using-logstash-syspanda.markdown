---
layout: post 
title:  "Advanced Sysmon filtering using Logstash – Syspanda" 
date:   2017-03-04T20:39:26.788Z 
categories: sysmon eventlog gpo logstash elasticsearch kibana
link: http://syspanda.com/index.php/2017/03/03/sysmon-filtering-using-logstash/ 
tags:
  - links
ogtype: article 
---

> Advanced Sysmon filtering using Logstash
by Pablo Delgado on March 3, 2017 in Elasticsearch, Sysmon
When I initially deployed Sysmon earlier last year I was amazed by the  amount of details it gathered as well as the huge amount of logs that my ELK stack was consuming. I decided to run it for a few weeks to get an idea of what was “normal” in my environment and later filter out those reoccurring events. If you really want to know what’s going on in your environment you should take this approach and filter as needed, it will take some time but you will feel confident that nothing is slipping through the cracks.

