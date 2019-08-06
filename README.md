# Scripts for Software Write Blocker in Raspberry PI with Kali Linux

# Script 1: iforense2019
# set ro, use dd for get image and copy image, after mount copy image in /mnt how ro

# Script 2: iforense2019-2
# when a device is unmounted, delete directories and umount of /mnt

# Script 3: iforense2019-3
# set read-only devices, nothing more, it is used in conjunction with python server

# Set script in Raspberry PI
# directory of rules
cd /etc/udev/rules.d/
# create rule
nano 01-myrule.rules
# modify this name script
... RUNÂ+= .... script to execute
# Reload rules
udevadm control --reload
