---
layout: post 
title:  "GitHub - diginc/docker-pi-hole: pi-hole in a docker container" 
date:   2017-11-01T19:19:19.137Z 
categories: docker webapp
link: https://github.com/diginc/docker-pi-hole 
tags:
  - links
ogtype: article 
---

> Running Pi-Hole Docker

DockerCloud automatically builds the latest docker-pi-hole changes into images which can easily be pulled and ran with a simple docker run command. Changes and updates under development or testing can be found on the dev tags

One crucial thing to know before starting is this container needs port 53 and port 80, 2 very popular ports that may conflict with existing applications. If you have no other services or dockers using port 53/80 (if you do, keep reading below for a reverse proxy example), the minimum arguments required to run this container are in the script docker_run.sh or summarized here:

