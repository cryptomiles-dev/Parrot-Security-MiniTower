
 

Parrot OS can be easily upgraded using the following commands.  Note we use   
`apt parrot-upgrade` instead of `apt upgrade` as  Parrot OS has its own upgrade wrapper for apt.  
 

`sudo apt update`  
`sudo parrot-upgrade -y` 
Run this ^ command twice.
After this the system is fully updated.  

If you would like to see which packages will be upgraded before upgrading them:  
`apt list --upgradeable`  




