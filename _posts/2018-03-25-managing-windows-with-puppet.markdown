---
layout: post 
title:  "Managing Windows With Puppet" 
date:   2018-03-25T15:02:48.160Z 
categories: puppet clientmanagement windows chocolatey
link: https://blog.ipswitch.com/managing-windows-with-puppet 
tags:
  - links
ogtype: article 
---

> Managing Windows With Puppet
 DAN FRANCISCUS|  December 28 2017  |  IT insights 
Puppet is one solution that is trying its best to make sure Windows engineers and admins have the tools necessary to manage effectively. Here's how to use it.

Many of the most popular infrastructure configuration solutions are built on *nix platforms, like Ansible, Chef, Salt and Puppet. This means that Linux is a first-class citizen for these tools and, consequently, everything else is second. In the Windows world, this can be somewhat depressing, but fortunately that does not mean you can’t manage Windows with these tools. Puppet is one solution that is trying its best to make sure Windows engineers and admins have the tools necessary to manage effectively. Whether it be supporting DSC resources, IIS or Chocolatey, Puppet allows you to automate Windows effectively.

In this article, I will go over some examples of some of the things you can manage on Windows with Puppet, as well as show how to setup Puppet agent. Keep in mind, I am assuming you have a functioning Puppet master server already set up.