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

16. After rebooting, login and get root access again by repeating steps 10 - 14

