locale -a

export LC_TIME=en_DK.utf8

thunderbird

mkdir -p ~/.thunderbird/init.d
cd .thunderbird/
cd init.d/
nano S00Locale.sh
chmod +x S00Locale.sh 


Nothing suggested above worked in my case (Ubuntu Server 12.04LTS). What finally helped was putting to the file /etc/environment:

LC_ALL=en_US.UTF-8
LANG=en_US.UTF-8

