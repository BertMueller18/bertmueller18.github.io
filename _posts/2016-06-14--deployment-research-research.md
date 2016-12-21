---
layout: post 
published: true 
title: "	Deployment Research Research Using PowerShell scripts with MDT 2013" 
date: 2016-06-14T12:23:39.086Z 
categories: deployment mdt mdt2013
link: http://deploymentresearch.com/Research/Post/318/Using-PowerShell-scripts-with-MDT-2013 
tags:
  - links
ogtype: article 
bodyclass: post 
---

## Using PowerShell scripts with MDT 2013

Deployment Research
Johan Arwidmark
Jul-04-2013

For the last ten years or so, VB Script wrappers have been popular due to the fact they have been available by default in the platforms. Now, in a time where most companies deploy either Windows 7 or Windows 8, there are other options, like PowerShell (PowerShell is King!).

MDT 2013, as well was MDT 2012 Update 1, does have the option of calling PowerShell scripts natively from the task sequence, but I normally don’t do that for the following reasons:

I like to have my scripts as applications because they are easier to import/export.
The MDT PowerShell feature is a bit picky about what you do in your scripts, as well as a being overly sensitive to PowerShell Group Policies :)
The solution – Create your own PowerShell wrapper

To have a nice solution, create a PowerShell wrapper for your commands, and then run that as an application in MDT. In the wrapper I also do some additional logging for good measure.