---
layout: post 
title:  "Setting up certificate based communication between SQL server endpoints for SQL mirroring | Sam's Corner" 
date:   2017-10-23T19:45:50.037Z 
categories: sqlserver mirroring cluster highavailability
tags:
  - links
ogtype: article 
---

> Setting up certificate based communication between SQL server endpoints for SQL mirroring

      3 Votes

SQL mirroring is a popular DR option for SQL databases. It provides a warm standby server where a database can be recovered quickly. Although SQL mirroring is being deprecated by Microsoft in SQL 2016 in lieu of Availability Groups, they share several elements of the underlying technologies.

SQL mirroring popularity is often attributed to

It does not require shared storage like clustering
It does not require a common file share like log-shipping
It can be configured for automatic failover (synchronous mode only) with the configuration of a SQL Witness (3rd server). This option requires that the application/client be mirror-aware (include ‘failover partner=xxxx’ in connection string)
It can be configured in safety/synchronous mode (default), where a transaction is written to both servers before a commit is returned to the client. This requires low latency between the 2 servers.
It can be configured in performance/asynchronous mode, where the primary server sends commit back to client as soon as the transaction is written to the send queue. This may lose data if the primary fails before the transaction makes it to the secondary server redo queue.
It can be configured across distant geographical locations (recommend asynchronous mode and certificate based authentication in this scenario)
It can be configured between 2 servers that belong to different AD domains using certificate authentication.