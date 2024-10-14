
# How To Check And Update Firmware - Raspberry Pi 5 MiniTower  


### Check Current Firmware Version  

`sudo rpi-eeprom-update`

This will display the currently running firmware version and will also show 
you if there are any other firmware updates currently newer than the one you 
are running.

### Updating The Firmware To Newer Version  

To update the firmware to a newer version use `raspi-config` to set the 
firmware option to **latest**.  The new firmware will be flashed.  Make sure 
to reboot afterwards.

`sudo raspi-config`
Scroll down to `Advanced`
Scroll down to `Bootloader version`
Select `Latest`

When finished if not prompted to reboot
`sudo reboot`


