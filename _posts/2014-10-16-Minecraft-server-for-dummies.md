---
layout: post
date:   2014-10-16 07:26:44
categories: blog
tags: ["Minecraft"]
---

Quick guide in getting a minecraft server up and running using a custom map. 

You can download the server from here
[https://minecraft.net/download](https://minecraft.net/download)

Direct download link here. 
[https://s3.amazonaws.com/Minecraft.Download/versions/1.8/minecraft_server.1.8.exe](https://s3.amazonaws.com/Minecraft.Download/versions/1.8/minecraft_server.1.8.exe)

But the downloaded exe in a seperate folder as it will create some files in the current folder the first time you run the exe.

Run the exe and close it again. It will create a logs folder, eula.txt and server.properties files. 
![Screenshot minecraftserver folder after first run](/images/2014/2014-10-16-minecraft-server.png)

Open the qula.txt file and change the following settings.

	eula=TRUE

No you can start the exe again and a bunch of files is created this time. This run takes some time as the server is  "Preparing level". On my machine this took 30 seconds one time only.  

![Screenshot minecraftserver folder after second run](/images/2014/2014-10-16-minecraft-server-second-run.png
)

For debugging you can look in the logs folder or create the batchfile from below and use it to start the server. 

	Set path=%path%;"C:\Program Files (x86)\Java\jre7\bin"
	title Minecraft server
	java -Xms1024M -Xmx1024M -jar minecraft_server.1.8.exe
	pause
	
	
Avoid UI by addid nogui switch

	Set path=%path%;"C:\Program Files (x86)\Java\jre7\bin"
	title Minecraft server
	java -Xms1024M -Xmx1024M -jar minecraft_server.1.8.exe nogui
	pause
	

64 bit java with d64 switch

	Set path=%path%;"C:\Program Files (x86)\Java\jre7\bin"
	title Minecraft server
	java -d64 -Xms1024M -Xmx1024M -jar minecraft_server.1.8.exe nogui
	pause

#Custommap
In order to change the map on you server do the following. I wanted to use a this map. 

[http://www.minecraftdl.com/herobrines-mansion-adventure-map/](http://www.minecraftdl.com/herobrines-mansion-adventure-map/)

Copy all these files from the downloaded zip directly to the worlds folder. 

![Screenshot custom map folder content](/images/2014/2014-10-16-custommapfiles.png
)

Note you need to modify the "server.properties" file with these settings as noted in the "Important Settings.txt" file. 

	allow-flight=true
	spawn-animals=true
	enable-command-block=true
	view-distance=15
	spawn-npcs=true

My "server.properties" ended up looking like this
	
	#Minecraft server properties
	generator-settings=
	op-permission-level=4
	resource-pack-hash=
	allow-nether=true
	level-name=world
	enable-query=false
	allow-flight=true
	announce-player-achievements=true
	server-port=25565
	max-world-size=29999984
	level-type=DEFAULT
	enable-rcon=false
	force-gamemode=false
	level-seed=
	server-ip=
	network-compression-threshold=256
	max-build-height=256
	spawn-npcs=true
	white-list=false
	spawn-animals=true
	snooper-enabled=true
	hardcore=false
	online-mode=true
	resource-pack=
	pvp=true
	difficulty=1
	enable-command-block=true
	player-idle-timeout=0
	gamemode=0
	max-players=20
	max-tick-time=60000
	spawn-monsters=true
	view-distance=15
	generate-structures=true
	motd=A Minecraft Server
	
Now start your server and it should have the custom map :)
