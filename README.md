Squeak-All-In-One
=================

bash scripts to create a Cog based Squeak All In One

##How To Use
To create a Squeak 4.4 all-in-one run ./create4.4AllInOne.  In that file the 4.4 specfies the Squeak version and the 2697 specifies the VM version.

##Process
1. download the vms from Eliot Miranda's site http://www.mirandabanda.org/files/Cog/VM/
2. extract the vms in the current directory
3. create the linux startup script 'squeak.sh'
4. create the windows Squeak.ini file
5. copy the windows and linux vms into the appropriate place in the Mac app bundle
6. copy in the squeak.sh, Squeak.ini, splash.bmp, and Info.plist file
7. make the Zip file
8. print a guide note about how you still have to get the image, changes, and sources file. 

At this point making the Zip file is premature because it will not contain an image, changes, or sources file.  The image and changes file need to be renamed to Squeak.image and Squeak.changes respectively.  Also the Info.plist file that is copied in is only valid for Squeak 4.4 and will need to be edited to point to the correct files for different versions of Squeak.  

##Caveats
I've only tested it on ubuntu.  It downloads the VM's every time.  It would probably be better as a Makefile.  It doesnt do anything to get the image, changes, or sources file or put them in the proper place (Contents/Resources/ of the .app directory).  IF there is ever a 'currentSable.zip' file on the ftp server the getImage script will be useful for downloading and extracting the appropriate version.
