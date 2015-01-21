---
layout: post
title:  "Installing Jekyll on Ubuntu 14.04"
date:   2014-10-08 10:43:44
categories: blog
tags: ["Jekyll", "Ubuntu"]
---

How to install Jekyll on Ubuntu
{% highlight bash %}
$ sudo apt-get install ruby
{% endhighlight %}
No problems
{% highlight bash %}
$ sudo gem install jekyll
{% endhighlight %}

Got this error
{% highlight bash %}
Fetching: liquid-2.6.1.gem (100%)
Fetching: kramdown-1.4.2.gem (100%)
Fetching: mercenary-0.3.4.gem (100%)
Fetching: safe_yaml-1.0.4.gem (100%)
Fetching: colorator-0.1.gem (100%)
Fetching: yajl-ruby-1.1.0.gem (100%)
Building native extensions.  This could take a while...
ERROR:  Error installing jekyll:
	ERROR: Failed to build gem native extension.

	/usr/bin/ruby1.9.1 extconf.rb
/usr/lib/ruby/1.9.1/rubygems/custom_require.rb:36:in `require': cannot load such file -- mkmf (LoadError)
	from /usr/lib/ruby/1.9.1/rubygems/custom_require.rb:36:in `require'
	from extconf.rb:1:in `<main>'
{% endhighlight %}

#New approach. 
Found this blogpost describing a way to get Jekyll installed.[http://sharadchhetri.com/2014/06/30/install-jekyll-on-ubuntu-14-04-lts/]

1
{% highlight bash %}
$ curl -sSL https://get.rvm.io | bash -s stable
{% endhighlight %}
2.
{% highlight bash %}
$ source /home/myserusernamehere/.rvm/scripts/rvm
{% endhighlight %}
3.
{% highlight bash %}
$ rvm requirements

Checking requirements for ubuntu.
Installing requirements for ubuntu.
Updating system...............
Installing required packages: gawk, libreadline6-dev, libyaml-dev, libsqlite3-dev, sqlite3, autoconf, libgdbm-dev, libncurses5-dev, automake, libtool, bison, libffi-dev..............
Requirements installation successful.
{% endhighlight %}

4. 
{% highlight bash %}
$ rvm install 2.1.2

Searching for binary rubies, this might take some time.
Found remote file https://rvm.io/binaries/ubuntu/14.04/x86_64/ruby-2.1.2.tar.bz2
Checking requirements for ubuntu.
Requirements installation successful.
ruby-2.1.2 - #configure
ruby-2.1.2 - #download
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
	                         Dload  Upload   Total   Spent    Left  Speed
100 22.8M  100 22.8M    0     0   287k      0  0:01:21  0:01:21 --:--:--  314k
ruby-2.1.2 - #validate archive
ruby-2.1.2 - #extract
ruby-2.1.2 - #validate binary
ruby-2.1.2 - #setup
ruby-2.1.2 - #gemset created /home/henrik/.rvm/gems/ruby-2.1.2@global
ruby-2.1.2 - #importing gemset /home/henrik/.rvm/gemsets/global.gems....................................
ruby-2.1.2 - #generating global wrappers........
ruby-2.1.2 - #gemset created /home/henrik/.rvm/gems/ruby-2.1.2
ruby-2.1.2 - #importing gemsetfile /home/henrik/.rvm/gemsets/default.gems evaluated to empty gem list
ruby-2.1.2 - #generating default wrappers........
{% endhighlight %}
5.
{% highlight bash %}
$ rvm use 2.1.2 --default

Using /home/henrik/.rvm/gems/ruby-2.1.2
{% endhighlight %}
6.
{% highlight bash %}
$ gem install jekyll

Fetching: liquid-2.6.1.gem (100%)
Successfully installed liquid-2.6.1
Fetching: kramdown-1.4.2.gem (100%)
Successfully installed kramdown-1.4.2
Fetching: mercenary-0.3.4.gem (100%)
Successfully installed mercenary-0.3.4
Fetching: safe_yaml-1.0.4.gem (100%)
Successfully installed safe_yaml-1.0.4
Fetching: colorator-0.1.gem (100%)
Successfully installed colorator-0.1
Fetching: yajl-ruby-1.1.0.gem (100%)
Building native extensions.  This could take a while...
Successfully installed yajl-ruby-1.1.0
Fetching: posix-spawn-0.3.9.gem (100%)
Building native extensions.  This could take a while...
Successfully installed posix-spawn-0.3.9
Fetching: pygments.rb-0.6.0.gem (100%)
Successfully installed pygments.rb-0.6.0
Fetching: redcarpet-3.1.2.gem (100%)
Building native extensions.  This could take a while...
Successfully installed redcarpet-3.1.2
Fetching: blankslate-2.1.2.4.gem (100%)
Successfully installed blankslate-2.1.2.4
Fetching: parslet-1.5.0.gem (100%)
Successfully installed parslet-1.5.0
Fetching: toml-0.1.1.gem (100%)
Successfully installed toml-0.1.1
Fetching: jekyll-paginate-1.0.0.gem (100%)
Successfully installed jekyll-paginate-1.0.0
Fetching: jekyll-gist-1.1.0.gem (100%)
Successfully installed jekyll-gist-1.1.0
Fetching: coffee-script-source-1.8.0.gem (100%)
Successfully installed coffee-script-source-1.8.0
Fetching: execjs-2.2.1.gem (100%)
Successfully installed execjs-2.2.1
Fetching: coffee-script-2.3.0.gem (100%)
Successfully installed coffee-script-2.3.0
Fetching: jekyll-coffeescript-1.0.1.gem (100%)
Successfully installed jekyll-coffeescript-1.0.1
Fetching: sass-3.4.5.gem (100%)
Successfully installed sass-3.4.5
Fetching: jekyll-sass-converter-1.2.1.gem (100%)
Successfully installed jekyll-sass-converter-1.2.1
Fetching: ffi-1.9.5.gem (100%)
Building native extensions.  This could take a while...
Successfully installed ffi-1.9.5
Fetching: rb-inotify-0.9.5.gem (100%)
Successfully installed rb-inotify-0.9.5
Fetching: rb-fsevent-0.9.4.gem (100%)
Successfully installed rb-fsevent-0.9.4
Fetching: hitimes-1.2.2.gem (100%)
Building native extensions.  This could take a while...
Successfully installed hitimes-1.2.2
Fetching: timers-4.0.1.gem (100%)
Successfully installed timers-4.0.1
Fetching: celluloid-0.16.0.gem (100%)
Successfully installed celluloid-0.16.0
Fetching: listen-2.7.11.gem (100%)
Successfully installed listen-2.7.11
Fetching: jekyll-watch-1.1.1.gem (100%)
Successfully installed jekyll-watch-1.1.1
Fetching: fast-stemmer-1.0.2.gem (100%)
Building native extensions.  This could take a while...
Successfully installed fast-stemmer-1.0.2
Fetching: classifier-reborn-2.0.1.gem (100%)
Successfully installed classifier-reborn-2.0.1
Fetching: jekyll-2.4.0.gem (100%)
Successfully installed jekyll-2.4.0
Parsing documentation for blankslate-2.1.2.4
Installing ri documentation for blankslate-2.1.2.4
Parsing documentation for celluloid-0.16.0
Installing ri documentation for celluloid-0.16.0
Parsing documentation for classifier-reborn-2.0.1
Installing ri documentation for classifier-reborn-2.0.1
Parsing documentation for coffee-script-2.3.0
Installing ri documentation for coffee-script-2.3.0
Parsing documentation for coffee-script-source-1.8.0
Installing ri documentation for coffee-script-source-1.8.0
Parsing documentation for colorator-0.1
Installing ri documentation for colorator-0.1
Parsing documentation for execjs-2.2.1
Installing ri documentation for execjs-2.2.1
Parsing documentation for fast-stemmer-1.0.2
Installing ri documentation for fast-stemmer-1.0.2
Parsing documentation for ffi-1.9.5
Installing ri documentation for ffi-1.9.5
Parsing documentation for hitimes-1.2.2
Installing ri documentation for hitimes-1.2.2
Parsing documentation for jekyll-2.4.0
Installing ri documentation for jekyll-2.4.0
Parsing documentation for jekyll-coffeescript-1.0.1
Installing ri documentation for jekyll-coffeescript-1.0.1
Parsing documentation for jekyll-gist-1.1.0
Installing ri documentation for jekyll-gist-1.1.0
Parsing documentation for jekyll-paginate-1.0.0
Installing ri documentation for jekyll-paginate-1.0.0
Parsing documentation for jekyll-sass-converter-1.2.1
Installing ri documentation for jekyll-sass-converter-1.2.1
Parsing documentation for jekyll-watch-1.1.1
Installing ri documentation for jekyll-watch-1.1.1
Parsing documentation for kramdown-1.4.2
Installing ri documentation for kramdown-1.4.2
Parsing documentation for liquid-2.6.1
Installing ri documentation for liquid-2.6.1
Parsing documentation for listen-2.7.11
Installing ri documentation for listen-2.7.11
Parsing documentation for mercenary-0.3.4
Installing ri documentation for mercenary-0.3.4
Parsing documentation for parslet-1.5.0
Installing ri documentation for parslet-1.5.0
Parsing documentation for posix-spawn-0.3.9
Installing ri documentation for posix-spawn-0.3.9
Parsing documentation for pygments.rb-0.6.0
Installing ri documentation for pygments.rb-0.6.0
Parsing documentation for rb-fsevent-0.9.4
Installing ri documentation for rb-fsevent-0.9.4
Parsing documentation for rb-inotify-0.9.5
Installing ri documentation for rb-inotify-0.9.5
Parsing documentation for redcarpet-3.1.2
Installing ri documentation for redcarpet-3.1.2
Parsing documentation for safe_yaml-1.0.4
Installing ri documentation for safe_yaml-1.0.4
Parsing documentation for sass-3.4.5
Installing ri documentation for sass-3.4.5
Parsing documentation for timers-4.0.1
Installing ri documentation for timers-4.0.1
Parsing documentation for toml-0.1.1
Installing ri documentation for toml-0.1.1
Parsing documentation for yajl-ruby-1.1.0
Installing ri documentation for yajl-ruby-1.1.0
Done installing documentation for blankslate, celluloid, classifier-reborn, coffee-script, coffee-script-source, colorator, execjs, fast-stemmer, ffi, hitimes, jekyll, jekyll-coffeescript, jekyll-gist, jekyll-paginate, jekyll-sass-converter, jekyll-watch, kramdown, liquid, listen, mercenary, parslet, posix-spawn, pygments.rb, rb-fsevent, rb-inotify, redcarpet, safe_yaml, sass, timers, toml, yajl-ruby after 18 seconds
31 gems installed
{% endhighlight %}
7.
{% highlight bash %}
$ jekyll -v
	
jekyll 2.4.0
{% endhighlight %}