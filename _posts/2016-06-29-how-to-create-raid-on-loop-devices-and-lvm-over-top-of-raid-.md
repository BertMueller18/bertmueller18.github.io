---
layout: post 
published: true 
title: "How to create RAID on Loop Devices and LVM over top of RAID." 
date: 2016-06-29T10:52:33.452Z 
link: http://www.slashroot.in/how-create-raid-loop-devices-and-lvm-over-top-raid 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> How to create RAID on Loop Devices and LVM over top of RAID.
Submitted by Satish Tiwary on Mon, 10/29/2012 - 18:29

Before you go through this article, let me inform you that this is completely experimental.So read it, enjoy it,but use it in real environment at your own risk.I use to do so many experimental things in my Lab and this is just one of them.We have studied and know so much about Partitions,RAID and LVM.This time i am going to write something on the fact which comes out after relating all these things together. As you all know that once we have created LVM on top of RAID, it become so easy to add any other volume to RAID. Now instead of using a real device or real partition here we are going to use loop devices.Then after creating loop devices we will create RAID on loop devices.And after that we will create LVM over top of RAID.

