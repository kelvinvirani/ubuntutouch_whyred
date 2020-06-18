## ubuntutouch_whyred
methods and guides for ubuntu touch
Halium 9.0


# Device Info


Branch : Xiaomi

Model : Redmi Note

Phone : Xiaomi Redmi Note 5 Pro / AI

CodeName : Whyred


# How to Flash
1 Backup Boot With Recovery
2 Flash Halium-Boot.img
3 Flash UbPorts-*.zip
4 reboot
( Please Don't Wipe )

# How To Dualboot
boot to android :
Restore Backup Boot

# boot to UbPorts :
Flash Halium-Boot.img Into Boot

# Anbox Install
Open Terminal and Type :

sudo apt install anbox-ubuntu-touch
 cd /home/phablet/
 sudo wget --show-progress http://cdimage.ubports.com/anbox-images/android-armhf-64binder.img
sudo -s
mkdir -p /home/phablet/anbox-data
mv /home/phablet/android-armhf-64binder.img /home/phablet/anbox-data/android.img
touch /home/phablet/anbox-data/.enable
chmod -R o+wrx /home/phablet/anbox-data/data
 sudo start -q anbox-container
 start -q anbox-session
reboot
( Wait Reboot, Don't Force Reboot )
