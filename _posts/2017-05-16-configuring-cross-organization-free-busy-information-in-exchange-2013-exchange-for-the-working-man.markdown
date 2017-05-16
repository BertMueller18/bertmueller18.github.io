---
layout: post 
title:  "Configuring Cross Organization Free Busy Information in Exchange 2013 | Exchange for the Working Man" 
date:   2017-05-16T19:52:34.109Z 
categories: exchange exchange2013 crossforest availability
link: http://port25guy.com/2014/11/05/configuring-cross-organization-free-busy-information-in-exchange-2013/ 
tags:
  - links
ogtype: article 
---

> Configuring Cross Organization Free Busy Information in Exchange 2013
Written by Port25Guy on Wednesday, November 5th, 2014
Uncategorized
4 Comments
There are many times when you will have an outside organization that you wish to share free busy information with.  Starting with Exchange 2010, Microsoft introduced the ability to utilize their Microsoft Federation Gateway to facilitate the sharing of free/busy information across multiple organizations.  While that solution works really well, there are times when that might not be the best solution.  For instance, you may have a customer in the middle of a large scale migration, or a partner company that you have connectivity to.  In these situations, you can utilize the direct method of establishing and configuring sharing free busy information.  This method, does require the two exchange organizations to have some level of connectivity to each other.  There are two direct methods that you can use. 

You can leverage the forest trust model, which indicates that you have a forest between between the two Exchange Organizations.  This would mean that you have a high level of network connectivity and integration between the two organizations.  The benefit to this method is that you can assign per user based permissions.  Meaning Paul from Forest A can have expanded rights to Jon from Forest B’s mailbox for free and busy. 

The second option is to use the non trusted forest based model.  This means that there is no forest trust between the networks.  Instead a general service account is leveraged to secure the permissions.  This means that the free and busy info is assigned organization wide, meaning you lack the granularity to assign different permissions per user.

I’ll walk through and explain both methods.  For our lab, we have the E15.corp forest, running Exchange 2013, and SOA.corp running Exchange 2013.