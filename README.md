# Scripts for Software Write Blocker in Raspberry PI with Kali Linux

Script 1: iforense2019
set ro, use dd for get image and copy image, after mount copy image in /mnt how ro

Script 2: iforense2019-2
when a device is unmounted, delete directories and umount of /mnt

Script 3: iforense2019-3
set read-only devices, nothing more, it is used in conjunction with python server

# Set script in Raspberry PI
* directory of rules
cd /etc/udev/rules.d/
* create rule
nano 01-myrule.rules
* modify this name script
... RUN+= .... script to execute
* Reload rules
udevadm control --reload
# Installation
1. Copy scripts iforense2019,iforense2019-2, iforense2019-3 in /usr/sbin
2. chmod 777 iforense2019*
3. Copy rules in /etc/udev/rules.d/
4. reload: udevadm control --reload

# Run server
1. in folder of server
2. source venv/bin/activate
3. export FLASK_APP=server
4. flask run --host=0.0.0.0
