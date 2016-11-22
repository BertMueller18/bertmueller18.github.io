---
layout: post 
title:  "Brendan's blog   » Top 10 DTrace scripts for Mac OS X" 
date:   2016-11-22T21:21:40.281Z 
---

> Top 10 DTrace scripts for Mac OS X

Since version 10.5 “Leopard”, Mac OS X has had DTrace, a tool used for performance analysis and troubleshooting. It provides data for Apple’s Instruments tool, as well as a collection of command line tools that are implemented as DTrace scripts. I’m familiar with the latter as I wrote the originals for the DTraceToolkit, which Apple then customized and enhanced for Mac OS X where they are shipped by default (great!). I use them regularly to answer this question:

why is my MacBook slow?

I work in an office where everyone has MacBook Pros, and “why is my MacBook slow?” is a common question. Applications can become slow or unresponsive while waiting for CPU work, memory requests or disk I/O to complete.

For people who try to ignore the slowdown, the question can become:

why is my MacBook fan so loud?

Standard performance analysis tools like Activity Monitor and top(1) (and any third-party tools based on the same foundation) can’t tell you some key information about activity on your system, such as how much CPU consumption is caused by short-lived processes, or which processes are causing disk I/O. DTrace, however, can see (just about) everything.

In this post, I’ll cover the top ten Mac OS X DTrace scripts that I use for figuring out why laptops are slow or why applications are misbehaving. Most of these scripts are already installed, a few are from the new DTrace book. &#x2014;[Brendan's blog   » Top 10 DTrace scripts for Mac OS X](http://dtrace.org/blogs/brendan/2011/10/10/top-10-dtrace-scripts-for-mac-os-x/)
