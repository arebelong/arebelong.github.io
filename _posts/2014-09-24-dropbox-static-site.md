---
layout: post
title:  "Using Dropbox as website provider"
date:   2014-09-24 21:16:44
categories: blog
tags: ["Dropbox", "pancake.io", "brace.io", "harpjs", "staticsite"]
--- 	

I recently decided to skip using wordpress. Instead I found that I could use my dropbox account for free to host a simple blog. You can use these providers which will give you an public url which people can use to access you web site in your dropbox account.

- [http://calepin.co/](http://calepin.co/)
- [http://pancake.io](http://pancake.io)
- [http://brace.io](http://brace.io)

#calepin.io
pro

 - free
 - Easy setup - No need to work with static site generators.
 - markdown support out of the box

cons

 - Limited css control
 - I didn't discover how to modify the layout of the site

#pancake.io
 pro

 - free, note the website states it might become a paid service later

cons

 - possible paid service in the future. 
 - slow loading. I experied slow loading eg. 4-16 seconds
 - need to setup static  site generator

#brace.io
pro

 - free
 - speed, very fast loading times.
 - draft support - view site online before publishing

cons

- need to setup static  site generator

And the winner is...brace.io. It was important for me to have a speedy blog and be able to control the layout.

I use [http://harpjs.com/](http://harpjs.com/) to generate a static siteusing a mixture of ejs templates, jade templates and blog post written in [http://daringfireball.net/projects/markdown/](markdown). Harpjs provides a template for setting up a blog if you want to get started quickly. [https://github.com/harp-boilerplates/hb-blog](https://github.com/harp-boilerplates/hb-blog)




 



