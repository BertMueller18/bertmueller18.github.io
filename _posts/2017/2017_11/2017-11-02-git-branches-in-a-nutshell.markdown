---
layout: post 
title:  "Git - Branches in a Nutshell" 
date:   2017-11-02T06:00:31.682Z 
categories: git programming 
link: https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell 
tags:
  - links
ogtype: article 
---

## Git Branching - Branches in a Nutshell

Nearly every VCS has some form of branching support. Branching means you diverge from the main line of development and continue to do work without messing with that main line. In many VCS tools, this is a somewhat expensive process, often requiring you to create a new copy of your source code directory, which can take a long time for large projects.

Some people refer to Git’s branching model as its “killer feature,” and it certainly sets Git apart in the VCS community. Why is it so special? The way Git branches is incredibly lightweight, making branching operations nearly instantaneous, and switching back and forth between branches generally just as fast. Unlike many other VCSs, Git encourages workflows that branch and merge often, even multiple times in a day. Understanding and mastering this feature gives you a powerful and unique tool and can entirely change the way that you develop.