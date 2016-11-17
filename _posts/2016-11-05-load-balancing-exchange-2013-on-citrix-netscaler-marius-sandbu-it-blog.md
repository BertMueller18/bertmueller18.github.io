---
layout: post 
published: true 
title: "Load-balancing Exchange 2013 on Citrix Netscaler | Marius Sandbu - IT blog" 
categories: citrix netscaler exchange exchange2013 loadbalancer
date: 2016-11-05T22:32:31.042Z 
link: https://msandbu.wordpress.com/2013/05/31/load-balancing-exchange-2013-on-citrix-netscaler/ 
tags:
  - links
ogtype: article 
bodyclass: post 
---

> Load-balancing Exchange 2013 on Citrix Netscaler
So I’ve gotten this questions lot the last couple of days, and I see it on the search terms statistics on the blog. So it is possible to load balance Exchange 2013 on Netscaler? Yes!
Now Microsoft usually has a list of «certified» load balancers that can be used on Exchange, but there still hasn’t been made one for Exchange 2013. 
You can see the one for Exchange 2010 here à
http://technet.microsoft.com/en-us/exchange/gg176682

now the problem with load balancing Exchange 2010 on a HLB (Hardware Load Balancer) was that you need to do it on L7 and using persistency why? because of the way that Exchange 2010 operated was that when a user
connected to OWA or other Exchange protocols, it was bound to that particular CAS server for the time of the connection. (Since the CAS rendered the mailbox, and if the connection moved to another CAS the user would need to reauthenticate)
You can see the old documentation for Exchange 2010 and Netscaler here à
http://www.citrix.com/content/dam/citrix/en_us/documents/products/netscalerexchange2010.pdf

With Exchange 2013 the roles and how it functions have changed. First of we only have two roles. We have the Mailbox and the Client Access Server role. The CAS role now only acts like a proxy, which allows for communication to a mailbox server and does the logic with protocol redirect.
These changes makes it easier to setup load balancing for now we have the option to load balance on L4 and are not dependent on using session persistency (Where we just need to define a VIP, SNIP, and a service. (+ Maybe a certificate for SSL offload purposes.) 
You can read more about it here à
http://technet.microsoft.com/en-us/library/jj898588(v=exchg.150).aspx

