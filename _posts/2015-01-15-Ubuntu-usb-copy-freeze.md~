Ubuntu usb copy freeze

Recently I needed to transfer files between two usb drives during wich performance was horrible. When using the TOP command there was no visible CPU usage explaining it. 

After a google to the problem I ended up finding this link describing a possible solution. 

http://unix.stackexchange.com/questions/107703/why-is-my-pc-freezing-while-im-copying-a-file-to-a-pendrive(http://unix.stackexchange.com/questions/107703/why-is-my-pc-freezing-while-im-copying-a-file-to-a-pendrive)

http://lwn.net/Articles/572911/(http://lwn.net/Articles/572911/)

	sudo -i

	echo $((16*1024*1024)) > /proc/sys/vm/dirty_background_bytes 
	echo $((16*1024*1024)) > /proc/sys/vm/dirty_bytes 

That did the trick. 

