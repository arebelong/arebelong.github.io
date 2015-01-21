http://www.webupd8.org/2012/10/ubuntu-multi-monitor-tweaks-full-screen.html

To install GHex in Ubuntu, use the following command:

sudo apt-get install ghex


Now, find out where your Flash plugin is installed using the following commands:

sudo updatedb
locate libflashplayer.so


The "locate" command above should return the full path to libflashplayer.so. Copy it because you'll need it for the next command:

gksu ghex /path/to/libflashplayer.so


Where "/path/to/" is the path to libflashplayer.so you've copied above (usually it should be /usr/lib/flashplugin-installer/libflashplayer.so or /usr/lib/adobe-flashplugin/libflashplayer.so)


Now, editing a binary with GHex is tricky, so read everything carefully. 

Once GHex opens the libflashplayer.so file using the command above, select Edit > Find, and in the right square, type (don't paste!) "_NET_ACTIVE_WINDOW" without the quotes, then click find:

ghex

On the right GHex pane, click one letter from "_NET_ACTIVE_WINDOW", let's say the first "N" and enter some other letter, let's say "A". Do not press the backspace key or anything, to replace a letter, simply click it, then press the letter you want to replace it with! Do not modify anything else! 

ghex

Once you've made this change, from the GHex menu select File > Save and restart your browser. You will have to follow these steps again if you update Adobe Flash Player!


If later on you want to revert this change, reinstall Flash Player plugin:

sudo apt-get install --reinstall flashplugin-installer



Note: Google Chrome (does not apply to Chromium) uses its own Adobe Flash Player plugin which doesn't have "_NET_ACTIVE_WINDOW", so if you want this fix to work with Google Chrome, enter "chrome://plugins/" in the url bar, then click "Details" on the right, scroll to the Adobe Flash Player plugin and 2 versions should be listed:

google chrome disable pepper flash

Here, disable the one that has "/opt/google/chrome/PepperFlash/libpepflashplayer.so" as its path. Doing this, Google Chrome will use the system Adobe Flash Player and not the built-in Google Chrome Adobe Flash Player.
