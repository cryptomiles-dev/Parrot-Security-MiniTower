

Included on the USB drive is a copy of the original image the device shipped with.   If you want to revert back to how the device was when you first got it then flash the MicroSd card (or other MicroSd card at least 32GB).
To do this you can use Raspberry Pi Imager from a Windows or Mac computer, or use the any Linux distribution.  

**NOTE** In this guide I use `parrot-minitower-restore.img.xz` but the image you recieve may have a slightly different name.    
If the restore image you recived has a different name then in the commands below replace `parrot-minitower-restore.img.xz` with the name of your restore image (make sure to include the `.img.xz` extension)   

## To use Raspberry Pi Imager:  

1. Download and install the appropriate Windows/Mac version from  
[https://www.raspberrypi.com/software](https://www.raspberrypi.com/software/)  

2. Select Raspberry Pi 5 for Raspberry Pi Device  
3. Select Choose OS > scroll to the bottom and select Use custom  
4. Select the included image titled [parrot-minitower-restore.img.xz]  
5. Select Storage and select your MicroSD card drive **Be careful here**  
	[If you select the wrong drive on this step you will do bad things!]
6. Click next to start burning the MicroSD card.

Thats it!  Now just insert the MicroSD card into the MiniTower and boot it up.


## To use the MiniTower (or any other Linux distro)  

1. Uncompress the image  
`xzcat parrot-minitower-restore.img.xz > parrot-minitower-restore.img.xz`  
2. Check where to write it - ie the MicroSd card location  
`lsblk`
3. Write the image  
`sudo dd if=parrot-minitower-restore.img.xz of=/dev/sdX bs=4M status=progress && sync`
	Replace `/dev/sdX` with the correct location discovered in step 2 for example `/dev/sda`





``
