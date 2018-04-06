---
layout: post 
title:  " Analysing Exchange (2013) Message Tracking Logs using NXLog &amp; ELK (ElasticSearch, Logstash, Kibana) | Elijah Paul" 
date:   2018-03-26T13:45:54.962Z 
categories: exchange exchange2013 elkstack kibana
link: https://elijahpaul.co.uk/analysing-exchange-2013-message-tracking-logs-using-elk-elasticsearch-logstash-kibana/ 
tags:
  - links
ogtype: article 
---

## Analysing Exchange (2013) Message Tracking Logs using NXLog & ELK (ElasticSearch, Logstash, Kibana)
Written by Elijah Paul the 30 Oct 2014 - Tagged: Logstash | Elasticsearch | Kibana | Logging | Exchange Server | Forensics | nxlog | Log Analysis

Share this post
  



Introduction
Exchange 2013 maintains a detailed record of messages sent between the transport services within an Exchange organization via message tracking logs.

The default location for these logs is;  C:\Program Files\Microsoft\Exchange Server\V15\TransportRoles\Logs\MessageTracking.

Exchange generates 3 main log files (there is a 4th, but its use is negligible):

MSGTRKMSyyyymmddhh-nnnn.log; traffic events (sent messages)
MSGTRKMDyyyymmddhh-nnnn.log; traffic events (received messgaes)
MSGTRKyyyymmddhh-nnnn.log; Transport service events (message flow)
These files are in CSV (comma-separated value) format, making for easy parsing by Logstash. Your ELK server can be used to analyse message activity trends, such as which users are sending the most emails, to whom they're sending them and with what frequency. You can also determine the total volume of messages received and sent over a period, average size of message, total message volume over a period by user, and much more.
More detailed information regarding Exchange Server 2013 message tracking logs can be found here