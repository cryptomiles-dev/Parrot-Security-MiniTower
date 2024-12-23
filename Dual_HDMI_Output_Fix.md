

This fix consists of two commands and a reboot.   Both of these commands are used to change a configuration file.    

- Open a terminal window
- Copy and paste the following two commands into your terminal window then press enter

`sudo sed -i '/^#\?dtoverlay=vc4-kms-v3d/d' /boot/config.txt`

`sudo sed -i '/^# Enable DRM VC4 V3D driver/a dtoverlay=vc4-fkms-v3d' /boot/config.txt`  

- Then reboot your device
`sudo reboot`

Now you should be able to seamelessly switch between the 3.5" LCD touchscreen display, single HDMI output, and dual HDMI output.  








