---
layout: post
published: true
title: "Terence Luk: Firewall Port Requirements for Citrix NetScaler 10 and Citrix XenApp 7.6"
date: 2016-09-12T06:57:15.443Z
categories: citrix netscaler
link: https://terenceluk.blogspot.de/2015/01/firewall-port-requirements-for-citrix.html
  - links
ogtype: article
bodyclass: post
---

## Firewall Port Requirements for Citrix NetScaler 10 and Citrix XenApp 7.6
I’ve noticed over the past year that one of the questions I get asked often is where to find specific Citrix documentation outlining the firewall port requirements and rules required to publish a XenApp environment through a NetScaler appliance and I find that every time I forward the following Citrix KB:

Required Ports for Citrix NetScaler Gateway in DMZ Setup
http://support.citrix.com/article/CTX113250

… I always get follow up questions about what is required for their environment so I thought I’d write a quick blog post supplying a diagram that provides a sample configuration.  The following example is a NetScaler deployed with two interfaces where one leg sits in an outside DMZ and the other on an inside DMZ.  Firewall rules are set up as shown in the following diagram between the DMZ networks and the internal server VLAN where the Citrix Delivery Controller, StoreFront, Application server and Active Directory Domain Controllers reside. The rules allow users to access the portal via http or https (http gets redirected to https) and the NetScaler is able to either use LDAP on port 389 or LDAPS on port 636 to authenticate against the domain controllers as well as communicate to the StoreFront server either http or https:
