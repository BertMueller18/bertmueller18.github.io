---
layout: post
published: true
title: "Dave's Technology: Tips and Trick for Citrix PVD"
date: 2016-11-10T21:14:34.028Z
categories: citrix pvdisk xendesktop xenapp 
link: https://davestechnology.blogspot.de/2015/02/tips-and-trick-for-citrix-pvd.html
tags:
  - links
ogtype: article
bodyclass: post
---

> Wednesday, February 18, 2015
Tips and Trick for Citrix PVD
 

Is PvD compatible with XenApp?
No only XenDesktop
 

Is a PvD the same as a differential disk?
No, PvD operates at the object level (files, folders, and registry). This enables all the changes that have been captured to persist across a base image updates whereas a differential disk would become invalidated in the case of a base image update.
 

Can multiple PvDs be associated to a device/user?
There can only be one PvD per Virtual Machine. The PvD is assigned to a Virtual Machine when building the catalogue of desktops. The pool type for a PvD catalogue is a pooled static, which the desktop is assigned to the user on first use.
 

Is the PvD a 1-1 mapping per user?
It is a 1:1 mapping to a Virtual Machine in a catalogue (assigned to the user on first use). The administrator can move a PvD to a new virtual machine in a recovery situation.
 

If you create a catalogue for pooled with PvD, it does not mean that the user is always required to be assigned to that Virtual Machine defeating one of the benefits of a pooled?
The base image is still shared and updated across the pool. However, once the user makes an initial connection to a Virtual Machine, the Virtual Machine is kept assigned to the user.
Note: You must connect early in the starting stage long before you know who the user is in order to maximise the application compatibility for services, devices etc.
 
