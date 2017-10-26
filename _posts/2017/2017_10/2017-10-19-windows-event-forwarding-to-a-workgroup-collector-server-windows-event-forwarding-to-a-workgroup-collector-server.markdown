---
layout: post 
title:  "Windows Event Forwarding to a workgroup Collector Server – Windows Event Forwarding to a Workgroup Collector Server" 
date:   2017-10-19T21:15:54.808Z 
categories: security eventlog windows
link: https://blogs.technet.microsoft.com/thedutchguy/2017/01/24/windows-event-forwarding-to-a-workgroup-collector-server/ 
tags:
  - links
ogtype: article 
---

## Windows Event Forwarding to a workgroup Collector Server
★★★★★★★★★★★★★★★
R. KluitJanuary 24, 20170 
0
0
Using Windows Event Forwarding (aka Windows Event Collection) events can be forwarded from various nodes to a central collector server. Having logs centrally makes it simpler to analyze the logs, additionally any uninteresting entries can be filtered out by configuring the appropriate event filters. To prevent tampering on the collected logs the events can be forwarded to a dedicated, non-domain joined machine. This guide is about how to setup such a configuration.

This guide documents a step by step approach to achieve the above configuration and is intended as an initial lab or learning exercise.  The document may be used as a template to configure Event Forwarding inside your organization, in which case changes to the template to reflect those differences are required.  I recommend you test these steps prior to implementing in a production environment.

To enable Windows Event Forwarding to forward events to a centralized non-domain joined collector server the following steps must be completed.

Configure an Enterprise PKI configuration.
Create specific certificate templates.
Issue a certificate for the collector server.
Configure the collector server.
Finally, configure the policy to enable event forwarding.