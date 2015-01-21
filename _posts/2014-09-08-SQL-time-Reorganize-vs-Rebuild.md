---
layout: post
title:  "SQL time  - Reorganize vs Rebuild"
date:   2014-09-08 19:45:00
categories: blog
tags: ["sqlserver", "reorganize", "rebuild"]
---

 avg_fragmentation_in_percent value

> 5% and < = 30%  ALTER INDEX REORGANIZE

> 30% ALTER INDEX REBUILD WITH (ONLINE = ON)

reorganize quick defrag, rebuild major defrag :)