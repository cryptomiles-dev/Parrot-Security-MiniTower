
# Update Java To Fix Burp Suite CE  

Burp Suite is already installed on the Parrot Security MiniTower however 
it will not run correctly and will give a Java version error.  To fix this 
we will update the MiniTower to Java 21.  The only way we can get Java 21 on 
arm64 is to use the Java 21 arm64 binaries from BellSoft.

1. First make sure we are up to date: 
`sudo apt update` 
Then:
`sudo parrot-upgrade -y` 
If there are any errors run this twice.

2. Check current Java version - it should be Java 17
`java --version`

3. Install dependancies --- most should already be installed but just in case
`sudo apt install libasound2 libc6 libfreetype6 libfontconfig1 libx11-6 libxau6 libxcb1 libxdmcp6 libxext6 libxi6 libxrender1 libxtst6 zlib1g`

4. Download the Java 21 arm64 binaries:
`wget https://download.bell-sw.com/java/21.0.5+11/bellsoft-jdk21.0.5+11-linux-aarch64.deb`

5. Install the `.deb` package with `dpkg` 
`sudo dpkg -i bellsoft-jdk21.0.5+11-linux-aarch64.deb`

6. Verify Java version
`java --version`

7. Reboot
`sudo reboot`

8. Verify Java version again and then open Burp Suite
`java --version` 
If Java version is 21 then open Burp Suite on the desktop.

9. Prevent future updates from reverting back to Java 17 [optional]
`sudo update-alternatives --set java /usr/lib/jvm/bellsoft-java21-aarch64/bin/java`
This ensures that your manually installed Java 21 won’t switch to other 
versions unexpectedly, even if something triggers an apt package update.






