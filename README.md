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
