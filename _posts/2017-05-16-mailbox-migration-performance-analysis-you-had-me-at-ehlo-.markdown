---
layout: post 
title:  "Mailbox Migration Performance Analysis – You Had Me At EHLO…" 
date:   2017-05-16T20:56:27.546Z 
categories: exchange migration performance
link: https://blogs.technet.microsoft.com/exchange/2014/03/24/mailbox-migration-performance-analysis/ 
tags:
  - links
ogtype: article 
---

## Mailbox Migration Performance Analysis

When you're migrating on-premises mailboxes to Office365, there are a lot of factors that can impact overall mailbox migration speed and performance. This post will help you investigate and correct the possible causes by using the AnalyzeMoveRequestStats.ps1 script to analyze the performance of a batch of move requests to identify reasons for slower performance.

The AnalyzeMoveRequestStatsscript provides important performance statistics from a given set of move request statistics. It also generates two files – one for the failure list, and one for individual move statistics.