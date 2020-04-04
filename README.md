# bo-be
Video communicator for the elderly

What do we need
Computer
Internet connection
Micro SD Card reader
Rasp
Power Supply

Download Raspbian
Use Torrent
https://www.raspberrypi.org/downloads/raspbian/
(Raspbian Buster with desktop and recommended software)

Download the Imager
https://www.raspberrypi.org/downloads/raspbian/
Burn image to card

The first time is longer than the rest, wait for 5 minutes for installation
Green LED should be blinking or steady

Headless installation

Find the IP
https://learn.pimoroni.com/tutorial/raspberry-pi/finding-your-raspberry-pi
https://angryip.org/download/#mac
** connect via Wifi **
https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md

We need to SSH to device
Create an empty file
https://www.raspberrypi.org/forums/viewtopic.php?t=210137

Might need to delete previous key
https://www.digitalocean.com/community/questions/warning-remote-host-identification-has-changed
ssh-keygen -R 192.168…..

Good practice
sudo apt update
sudo apt-get upgrade
sudo shutdown -r now

sudo raspi-config
Update
Change password - enter new one - write it down
Network options - N2 - wi-fi connect to wifi
Boot options - B4 - Desktop auto login
Interfacing Options - P1 - camera enable
Interfacing Options - P2 - SSH enable
Interfacing Options - P3 - VNC enable
Advanced options - A9 - Compositor - disable
Advanced options - AA - Pi 4 Video options - V3 - Disable both 
Advanced options - A5 - Screen resolution - DMT Mode 9 - 800x600 
Advanced options - A3 - Memory split - 512
 
Connect via VNC
https://www.realvnc.com/en/connect/trial/

Connect Screen
Show connector right direction
Warn about bending the cable
https://learn.pimoroni.com/tutorial/pi-lcd/getting-started-with-raspberry-pi-7-touchscreen-lcd

Connect camera
https://www.youtube.com/watch?v=lAbpDRy-gc0
Test camera output
raspistill -o Desktop/image.jpg
https://www.dummies.com/computers/raspberry-pi/test-raspberry-pi-camera-module/


Chromium autostart
https://www.raspberrypi.org/forums/viewtopic.php?t=10165
https://www.raspberrypi.org/forums/viewtopic.php?t=267943
sudo nano ~/.config/lxsession/LXDE-pi/autostart
@chromium-browser --kiosk --disable-session-crashed-bubble --disable-infobars --disable-restore-session-state https://meet.jit.si/FooBar

Remove mouse
sudo apt-get install unclutter
sudo nano ~/.config/lxsession/LXDE-pi/autostart
@unclutter -idle 1 -root

Linphone
https://www.linphone.org/news/linphone-python-raspberry-pi-38
https://wiki.linphone.org/xwiki/wiki/public/view/Linphone/Linphone%20and%20Raspberry%20Pi/
https://stackoverflow.com/questions/28385540/gstreamer-error-on-mac


OSX Brew
https://brew.sh/

GSTREAMER
https://github.com/joicemjoseph/videocall
https://tutos-sphinx-test.readthedocs.io/en/latest/source/rpi/video/video-streaming-gstreamer.html

Why and what
https://en.wikipedia.org/wiki/Comparison_of_VoIP_software

Jitsi Community Help
https://github.com/jitsi/docker-jitsi-meet/issues/195

Config file on Pi
https://www.raspberrypi.org/documentation/configuration/config-txt/

Overclocking
https://www.raspberrypi.org/documentation/configuration/config-txt/overclocking.md
https://magpi.raspberrypi.org/articles/how-to-overclock-raspberry-pi-4


Inspiration
https://www.reddit.com/r/raspberry_pi/comments/fsdhld/i_built_some_hardware_into_a_box_of_capn_crunch/

Install Chromium browser
sudo apt-get install chromium-browser --yes
https://tutorials-raspberrypi.com/google-chrome-for-raspberry-pi/

Build our Jitsi server and test
https://stackoverflow.com/questions/44381648/try-jitsi-meet-with-raspberry-pi
