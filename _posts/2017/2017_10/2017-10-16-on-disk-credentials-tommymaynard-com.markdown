---
layout: post 
title:  "On Disk Credentials | tommymaynard.com" 
date:   2017-10-16T21:02:20.033Z 
categories: powershell programming security
link: http://tommymaynard.com/on-disk-credentials-2017/ 
tags:
  - links
ogtype: article 
---

> On Disk Credentials
2 Replies
This article has been written by plenty of people, plenty of times. But even so, I’m writing it again. This is partly because I want to have a place to find this information written by myself. That said, if it helps anyone else too, then it’s doing the other part, and that’s helping those around me.

What I want to do today, is create an on disk credential file. I’ve done it a few times now, for a few projects, but there’s something about this topic, I can’t forever nail down in my own brain. Well, as best as I see it, those days are numbered.

Once my on disk credential file is created, I want to run an automated task(s) as a user other than that which is running my outlying automation. It’s kind of like this: User1 runs an automated task and it needs to complete some work it can’t do on it’s own. Therefore, it does a part of what it needs as User2. That’s the user that can do what User1 can’t.

The first step is creating the credential file. Now, when you think of credentials, you should think of the combination of a username and a corresponding password, together. That said, this credential file is actually only going to hold the password. While I’m going to continue to call it a credential file, keep in mind that we’re only storing the password inside this file.

