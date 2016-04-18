# RPi3Setup
Basic setup to kickstart a Raspberry Pi 3 node server

I'm currently running Raspbian Jessie Lite. 
To get around the problem with currupt SD cards I boot from USB stick. Instructions:
https://www.stewright.me/2013/05/install-and-run-raspbian-from-a-usb-flash-drive/
NOTE! This fails after a few times and then I have to reflash the USB stick.
Don't forget to format the USB stick to FAT32.

start with running 
sudo apt-get update
sudo apt-get upgrade

Setup automatic WiFi according to:
http://weworkweplay.com/play/automatically-connect-a-raspberry-pi-to-a-wifi-network/
The files are available in this repo, with changed access rights so that git can add them. Original access rights documented in folder.


Install git with 
sudo apt-get install git

Install sqlite3 same way


Some useful trick: 
Press Alt+ Left/Right arrow key to access more tty's
Power off with sudo shutdown -h now


