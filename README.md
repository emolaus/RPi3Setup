# RPi3Setup
Basic setup to kickstart a Raspberry Pi 3 node server

I'm currently running Raspbian Jessie Lite. 
To get around the problem with currupt SD cards I boot from USB stick. Instructions:
https://www.stewright.me/2013/05/install-and-run-raspbian-from-a-usb-flash-drive/
and
http://www.instructables.com/id/Boot-the-Raspberry-Pi-from-USB/step5/Set-to-Boot-from-the-Flash-Drive/
NOTE! This fails after a few times and then I have to reflash the USB stick.
I skipped setting the sd card flag and erase the memory. Actually I burned the same image onto it and just edited the file where rootfs is set.

Enable ssh, change password, enable autologin...

start with running 
sudo apt-get update
sudo apt-get upgrade

Setup automatic WiFi and static IP address according to:

http://weworkweplay.com/play/automatically-connect-a-raspberry-pi-to-a-wifi-network/

The files are available in this repo, but with changed access rights so that git can add them. Original access rights documented in folder.

Wrote a script ~bin/resetwlan available in this repo. Checks if connected, if not resets wlan0. Added to cron with line

*/1 * * * * root  /home/username/RPi3Setup/bin/resetwlan

Install git with 

sudo apt-get install git

Install sqlite3, npm, tmux
Installed node 5 with this instruction:
https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

Good tmux cheat sheet:
http://www.dayid.org/comp/tm.html

Some useful commands: 
Press Alt+ Left/Right arrow key to access more tty's

Power off with sudo shutdown -h now
Scan network with mac: sudo nmap -sn 192.168.0/24

nano /etc/crontab och sedan sudo service cron restart
