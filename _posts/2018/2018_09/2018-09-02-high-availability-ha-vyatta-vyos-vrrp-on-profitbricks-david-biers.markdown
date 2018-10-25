---
layout: post 
title:  "High Availability HA Vyatta VyOS VRRP on ProfitBricks - David Biers" 
date:   2018-09-02T16:11:33.190Z 
categories: vyos vrrp networking
link: https://dbiers.me/high-availability-ha-vyatta-vyos-vrrp-on-profitbricks/ 
tags:
  - links
ogtype: article 
---

## High Availability HA Vyatta VyOS VRRP on ProfitBricks

BY DAVID · MAY 9, 2016

Introduction
Configuring a high-availability configuration is key to keeping the business running. Of course, instead of just duplicating every single thing, you should perform some risk assessments to see where the critical services are and duplicate from there. One of the guaranteed points in infrastructure is your core routers or firewalls. All traffic is flowing through them and if it goes down, you're out since everything is connected to it.

This will be a pretty straight forward walk-through as VRRP is easy to setup and configure on VyOS.