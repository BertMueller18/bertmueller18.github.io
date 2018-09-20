---
layout: post 
title:  "Tips for Running the TICK Stack Using Docker | Blog | InfluxData" 
date:   2018-09-20T06:23:29.967Z 
categories: grafana elastisearch docker 
link: https://www.influxdata.com/blog/tips-for-running-the-tick-stack-using-docker/ 
tags:
  - links
ogtype: article 
---

## Tips for Running the TICK Stack Using Docker
BY NOAH CROWLEY | JUN 29, 2018 | COMMUNITY, DEVELOPER, INFLUXDB | 0 COMMENTS

Docker? Docker docker docker.
While the Docker buzz has faded a bit, replaced by new words like “Kubernetes” and “Serverless”, there is no arguing that Docker is the default toolchain for developers looking to get started with Linux containers, as it is fairly ubiquitous and tightly integrated with a variety of platforms.

Linux containers are an abstraction built from several pieces of underlying Linux functionality like namespaces and cgroups, which together provide a type of OS-level virtualization; to your applications, it seems like each one of them is running alone on their own copy of the OS. As a result, Docker provides a variety of benefits over running software directly on a host machine; it isolates your applications from the rest of your system, and each other, and makes it easier to deploy applications across a variety of operating systems. In general, it just keeps things clean and tidy and well-partitioned.