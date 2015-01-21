---
layout: post
title:  "IE 9 console error findings"
date:   2014-09-08 22:22:29
categories: blog
tags: ["IE9", "console"]
---

I recently learned that one has to be careful when using console.log and supporting IE 9 browsers. The error caused javascript code to stop working but only in IE 9. When I tried to debug the webpage using IE developer tools everything worked as expected. I then closed developer tools and instead enabled script debugging in IE. I was now presented with this error.

[id]: /assets/images/blog/201409-09-IE-console-log-error.PNG  "IE displaying the script error related to using console"
![IE displaying the script error related to using console][id]

I was somewhat surprised as I thought that it was possible to check for existing of a variable in that way but as you can see it will display an error in IE 9. Therefore I would recommend to generally avoid using console javascript in production code. 

Code that appears to be fine, but still craches the javascript in IE 9. IE will throw an exception when excecuting if(console) code as you saw in the screenshot. This javascript will throw an error in IE 9.

{% highlight javascript %}
if(console) { 
  console.log('msg');
}
{% endhighlight %}

These to alternatives will work if you need to check for existence of console before using it. 

{% highlight javascript %}
if(typeof console == "undefined") {
  // this code would work.
}

if(window.console){
  // this code would work in IE 9 haven't tested other browsers.
}
{% endhighlight %}
Be careful when using the typeof operator to identify if an javascript variable exists. 
{% highlight javascript %}
var demo = false;
if(typeof demo == "undefined") // does not exist{
	// CODE HERE WOULD EXECUTE ANYWAY
}
{% endhighlight %}
Comment from stackoverflow.

This(meaning the above code) will report "false" if myvar is a false value or if myvar is not in scope (in which case most browsers will also emit a warning)

Fool profway to verify if an variable exist or not. 
{% highlight javascript %}
var exists = true;
try {
    if (someVar)
        exists = true;
} catch(e) { exists = false; }
if (exists)
{% endhighlight %}
[http://stackoverflow.com/questions/5879319/how-to-check-if-a-variable-exist-in-javascript](http://stackoverflow.com/questions/5879319/how-to-check-if-a-variable-exist-in-javascript)

