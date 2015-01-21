---
layout: post
date:   2014-10-09 16:02:44
categories: blog
tags: ["Sitecore", "Sitecore tips and tricks"]
---

I recently was creating some new templates in Sitecore. I wanted to modify the insert options of the template so only items of a specific type could be children. I modified the template like this


Next I created an item based on this template but it didn't work.

Instead you need to change this by using the Standard values.

Now if you create an item based on this item the insert options will have effect :)