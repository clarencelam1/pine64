# pine64
This repo holds instructions for flashing an OS onto and SD card for the pine64

Steps:

1. Download pine64-image-ubuntubase-31065bsp-longsleep.img from https://www.pine64.pro/getting-started-linux/ (https://www.pine64.pro/download.php?option=download&optionid=33)

2. Put SD into android mobile device (Samsung S4) and format the SD card
3. Insert SD card into a USB card reader.
4. Insert USB card reader into MacBook Pro.
5. Open a terminal
6. Run the following commands the burn the ubuntu image onto the SD card:

  ```
  diskutil unmountDisk /dev/disk2
  sudo dd if=pine64-image-ubuntubase-31065bsp-longsleep.img of=/dev/disk2 bs=1m
  ```

7. After the image is done burning onto the SD card, remove it and insert it into the SD card slot of the pine64.
8. Plug in all peripherals (mouse, keyboard, HDMI) and ethernet for the pine64.
9. Power up the pine64.
10. Once the `localhost login:` prompt shows up, type in:

  `ubuntu`

11. Once the `Password:` prompt shows up, type in:

  `ubuntu`


12. Type in the following into the console get sudo access:

  `sudo -i`

13. Once the `[sudo] password for ubuntu:` prompt shows up, type in:

  `ubuntu`

14. You should now see the `root@localhost:~` prompt once you have root access.

15. Type in the following into the console to update uboot, update kernel and resize the rootfs. Reboot the board with the last command listed after resizing the rootfs.

  ```
  /usr/local/sbin/pine64_update_uboot.sh
  /usr/local/sbin/pine64_update_kernel.sh
  resize_rootfs.sh
  reboot
  ```

16. After rebooting, login and get root access again by repeating steps 10 - 14.
17. Following the directions on https://www.pine64.pro/desktop-environment-on-ubuntu/ or, they will be listed here again for convince.
18. To update to the latest package lists and upgrade to them, enter the following commands into the console:

  ```
  apt-get update
  apt-get upgrade
  apt-get install dialog tasksel
  tasksel
  ```

19. After the desktop is installed, to enable features like 2d acceleration, video hardware decoding and resolution switching, enter the following commands:

  ```
  apt-get install libump libvdpau-sunxi1 libcedrus1 sunxi-disp-tool xserver-xorg-video-fbturbo
  echo 'Section "Device"' > /etc/X11/xorg.conf
  echo 'Identifier "Allwinner A10/A13 FBDEV"' >> /etc/X11/xorg.conf
  echo 'Driver "fbturbo"' >> /etc/X11/xorg.conf
  echo 'Option "fbdev" "/dev/fb0"' >> /etc/X11/xorg.conf
  echo 'Option "SwapbuffersWait" "true"' >> /etc/X11/xorg.conf
  echo 'EndSection' >> /etc/X11/xorg.conf
  reboot
  ```

20. Install en_US locale first:

  ```
  sudo locale-gen en_US en_US.UTF-8
  sudo dpkg-reconfigure locales 
  ```
  

  
22. Optional but useful addons to install as well:

  ```
  apt-get install midori
  apt-get install clamtk
  apt-get install gparted
  apt-get install synaptic
  ```

23. Insall gitih te following command:

  `apt-get install git`
  
24. Install pip3 and upgrade to the latest version of pip3:

  ```
  sudo apt-get update && sudo apt-get -y upgrade
  sudo apt-get install python3-pip
  pip3 -V
  pip3 install --upgrade pip
  ```
  
