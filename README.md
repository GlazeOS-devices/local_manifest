GlazeOS for Motorola Devices
============================

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/glaze

Next, naviate into that new directory via the terminal:

	cd ~/glaze

To initialize your local repository using the Turbo ROM trees, use this command:

	repo init -u git://github.com/GlazeOS/manifest.git -b ng7.1

Also add the local manifests:

	git clone https://github.com/GlazeOS-devices/local_manifest -b motorola .repo/local_manifests

Then sync up with this command:

	repo sync
	
You can make the 4 higher depending on how fast your internet connection is. 

-------------
 
_Building from source_
---------------

First:

	cd ~/glaze

Second:

	$ echo "export USE_CCACHE=1" >> ~/.bashrc
	$ prebuilts/misc/linux-x86/ccache/ccache -M 80G

Third:

	. build/envsetup.sh
	brunch codename
