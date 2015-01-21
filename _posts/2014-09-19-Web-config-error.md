---
layout: post
title:  "IIS rewrite module - web.config error"
date:   2014-09-19 21:16:44
categories: blog
tags: ["Web.config", "iis", "debug"]
---

Recently an error in web.config cause IIS to show this error *HTTP Error 500.19 - Internal Server Error*. The error orcurred after having the web.config updated from a co-worker. After some digging it turned out to be related to some invalid configuration sections. My co-worker had IIS rewrite module installed and also added some configuration to the web.config regarding this module.

[id]: /assets/images/blog/2014-09-19-server-error.png  "Optional title attribute"
![Alt text][id]

In my case the solution was to install IIS rewrite module for the configuration elements to be recognized. When I did it i didn't backup my old web.config cause it was working on my co-workers machine. Note to self always do backup :) 
