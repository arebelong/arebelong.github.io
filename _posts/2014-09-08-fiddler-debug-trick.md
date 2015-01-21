---
layout: post
title:  "How to debug minified javascript when you have access to unminified version"
date:   2014-09-08 22:22:29
categories: blog
tags: ["IE", "Fiddler", "debug"]
---

I recently had an eror which only affected IE 9. Since I didn't have IE 9 locally I was forced to use an Virtual Machine to run the browser. You can read more information [here(/post/somewhre)].
I could only reproduce the error on production and due to time restraint unable to setup dev identical to production. What to do, Fiddler to the rescue.

##Fiddler Autoresponder
Fiddler has a feature called Autoresponder which enabled you to predifine a response to a given request. All I had to do to debug on with production data, was to replace the minified javascript with the unminified version. In order to do that I added an rule which matched the minified javascript url and asked fiddler to instead load the unminified javascript when the browser requested the minified version. Voila now I could debug the javascript in the browser.

Note firefox and chrome also allow one to unminified javascript but that was not an option du to IE 9 the error was only present in this browser.