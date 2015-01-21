apt-get remove nvidia-*

apt-get autoremove

dconf reset -f /org/compiz/ 
unity --reset-icons &disown

dconf reset -f /org/compiz/ 
unity --reset-icons &disown

 export DISPLAY=:0

sudo apt-get autoremove

sudo apt-get purge nvidia-*


 sudo stop lightdm 


dpkg --get-selections

dpkg --get-selections | grep php

File locations 

dpkg -L php5-gd

Use this PPA
https://launchpad.net/~mamarley/+archive/ubuntu/nvidia



    I don't think the CUDA .deb was necessary. I generally recommend this PPA as it's less invasive than xorg-edgers. https://launchpad.net/~mamarley/+archive/ubuntu/nvidia 



sudo add-apt-repository ppaorg-edgers/ppa

sudo apt-get update

sudo apt-get install nvidia-343 
