---
layout: post 
title:  "Creating Hyper-V images with Packer — Hurry Up and Wait!" 
date:   2018-07-15T10:17:14.527Z 
categories: terraform hyperv deployment
link: http://www.hurryupandwait.io/blog/creating-hyper-v-images-with-packer 
tags:
  - links
ogtype: article 
---

> Creating Hyper-V images with Packer /August 2, 2016

Over the last week I've been playing with some new significant changes to my packer build process. This includes replacing the Boxstarter based install with a Chef cookbook,  and also using a native Hyper-V builder. I'll be blogging about the Chef stuff later. This post will discuss how to use Taliesin Sisson's PR #2576 to build Hyper-V images with Hyper-V.

The state of Hyper-V builders
Packer currently comes bundled with builders for the major cloud providers, some local hypervisors like VirtualBox, VMware, Parallels, and QEMU as wells as OpenStack and Docker. There is no built in Hyper-V builder - the native hypervisor on Windows.