# List
Hard Ware : RaspberryPi Zero 2 W
CSI Camera : OEM 5647 CAM
display : Waveshare 240*240p 1.3 inch TFT 

OS : Raspberry Pi OS Bullseye (32bit Lite)
username : pi
Pass : nvpi

firststep

ssh pi@raspberrypi.local

# Setup
Q:https://www.waveshare.com/wiki/1.3inch_LCD_Module#Download_Drivers
### 01.Driver download

sudo apt-get install cmake -y
cd ~
wget https://files.waveshare.com/upload/1/18/Waveshare_fbcp.zip
unzip Waveshare_fbcp.zip
cd Waveshare_fbcp/
sudo chmod +x ./shell/*
### 02.run script
sudo ./shell/waveshare-1inch3

# Autoreboot

sudo fdisk -l

save img 
sudo shutdown now


## host 
diskutil list

# backup cmd
sudo dd if=/dev/disk2 of=nvpizero2w.img bs=1m

14804+0 records in
14804+0 records out
15523119104 bytes transferred in 4529.853701 secs (3426848 bytes/sec)

# set Displayreso
sudo nano /boot/config.txt

sudo apt update && sudo apt upgrade