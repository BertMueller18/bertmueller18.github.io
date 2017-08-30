---
layout: post 
title:  "GitHub - jwilder/nginx-proxy: Automated nginx proxy for Docker containers using docker-gen" 
date:   2017-08-24T19:08:00.760Z 
categories: docker nextcloud linux nginx-proxy
link: https://github.com/jwilder/nginx-proxy#per-virtual_host 
tags:
  - links
ogtype: article 
---

current have a problem when uploading files which gives an error: "Request Entity Too Large"

The solution was to add a config file named exactly like the VIRTUAL_HOST in the vhost.d folder.
I used the default proxy config (see jwilder/nginx-proxy) and added client_max_body_size 10G;
More information can be found here: https://github.com/jwilder/nginx-proxy#per-virtual_host


## nginx-proxy sets up a container running nginx and docker-gen. docker-gen generates reverse proxy configs for nginx and reloads nginx when containers are started and stopped.

See Automated Nginx Reverse Proxy for Docker for why you might want to use this.

