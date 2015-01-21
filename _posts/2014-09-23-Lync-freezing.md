---
layout: post
title:  "Lync 2013 freezing after 5 sec - Solution found"
date:   2014-09-23 21:16:44
categories: blog
tags: ["Lync"]
---

My Lync 2013 stopped working recently and began to be unresponsive 2-5 secs after application had been started. 
I followed the traditional troubleshooting workflow.

- Reboot computer
- Remove Lync and install it again
- Install all windows updates 

It didn't work instead this was needed. 
 
How to fix
 
- Uninstall the soundcard driver
- Uninstall the IDTxxxx soundcard software
- Reboot machine

That's it :)

