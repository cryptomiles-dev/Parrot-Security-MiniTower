
# Remote access with Raspberry Pi Connect

You can access a Raspberry Pi remotely from a browser on another device using Raspberry Pi Connect. Connect handles configuration automatically, so you don’t have to find your Raspberry Pi’s local IP address, your network’s public IP address, or modify your local network firewall to enable external access.

**NOTE:** You will need an account with Raspberry Pi in order to use Raspberry Pi Connect.  You can sign up for free at [connect.raspberrypi.com](https://connect.raspberrypi.com/sign-in)

Raspberry Pi Connect provides secure access to your Raspberry Pi from anywhere in the world.

[![hero](https://github.com/raspberrypi/documentation/raw/develop/documentation/asciidoc/services/connect/images/hero.png)](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/services/connect/images/hero.png)

To use Connect, [install the Connect software](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/services/connect/connect.adoc#install-connect) and [link your device with an account](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/services/connect/connect.adoc#link-connect) on your Raspberry Pi. Then visit [connect.raspberrypi.com](https://connect.raspberrypi.com/) to access the desktop or a shell running on your Raspberry Pi in a browser window.

## Install - Enable Raspberry Pi Connect     

Raspberry Pi Connect is already installed on your system.  Raspberry Pi Connect must be enabled before you can use it.  This is done through the `raspi-config` tool.   
`sudo raspi-config`  
 
 Navigate to `interfaces` > `RPI Connect` > then enable it.  

If for some reason Raspberry Pi Connect is not installed you can easily install it.    
`sudo apt install rpi-connect`  
After installation, use the `rpi-connect` command line interface to start Connect for your current user:
`rpi-connect on`  


## How To Use Raspberry Pi Connect   

Once you have Raspberry Pi Connect up and running go the nicely made guide by Raspberry Pi for further instructions.  
[Use Raspberry Pi Connect](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/services/connect/use.adoc)

If you run into any issues see the [Troubleshooting page](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/services/connect/troubleshooting.adoc)  

