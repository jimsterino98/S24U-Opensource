# S24-Ultra-KSU-next-with-susfs
Basically with the lack of samsung repos on the internet because they can be a pain, i've decided that with this repo I want to provide samsung specific kernel builds for KSU-next with susfs patches. For now it's limited to the s24 ultra, SM-S928B as that's the phone I have and can validate that they work. If anyone would like to be a tester for another phone that you have just shoot me a message on telegram!

# DISCLAIMER:
I am NOT responsible for any damage, lost data or bricks to any devices! You are doing this AT YOUR OWN RISK! Warranty is now void and knox is tripped!

# Instructions
Must have unlocked bootloader. If unaware how to do that, there are many tutorials on the internet, I will not be going through it.

Flashing this on for the first time WILL make you factory reset. Back up all data!

## 1. Downloading Firmware
Download your Samsung firmware, you can either use Frija or SamFirm. I like to use Frija. You can get that from [here](https://github.com/SlackingVeteran/frija/releases)

## 2. Odin
You also need the latest Stable version of Odin which is 3.14.1 from [here](https://odindownload.com/Odin-Download.html)

## 3. Extracting
Go to the folder where you downloaded your firmware, and extract it. After extracting, you should have different files, BLxx...tar.md5, APxx...tar.md5, CPxx...tar.md5, CSCxx...tar.md5, HOME_CSCxx...tar.md5.

## 4. Download Mode
Boot your S24 ultra to download mode. To do that, first make sure you have a USB cable plugged into your computer. Turn the phone off. Then, press and hold VOL_UP button and VOL_DOWN button at the same time. After a couple seconds, plug the phone into the cable that's in the computer, then whichever key combo gets you into download mode. It should be VOL_UP.

## 5. Using ODIN
After your phone is in download mode, make sure ODIN detects it. Near the top left it should show a COM port. If it doesn't, use the internet to figure out why. Then in BL, CP, CSC slot you are going to pick the respective tar files from the downloaded firmware. In the AP Slot you are going to put the tar file downloaded from the releases page of this REPO.

### NOTE: If this is your FIRST TIME installing KSU-next on your phone, use the regular CSC file to trigger a factory reset. If you already have KSU installed and you are just updating firmware, use HOME_CSC. MAKE SURE AP FILE MATCHES DOWNLOAD FIRMWARE! Example: Downloaded firmware build number ends in BYEB, make sure to download the BYEB AP file from releases!

After odin has completed flashing, phone will reboot and you will need to go through the set up process. IF YOU END UP IN BOOTLOOP, INSTALL STOCK FIRMWARE.

If you are having issues with ODIN, see telegram group at the bottom and send a message.

# 6. Confirming installation

Download and install latest release of KernelSU-Next from [here](https://github.com/KernelSU-Next/KernelSU-Next/releases) <br/>
If it shows "Working" at the top of the homepage of the KSU-next App, that means install was successful. If you look further down it will tell you kernel version, and susfs version.

Congratulations! You now have KSU-next with susfs!

# Giving apps root in KSU-next
Open the app and go to the "superuser" tab at the bottom, select the app you would like to give root to, then touch the switch. That's all!

# KSU Modules
First module to download should be the susfs4ksu module, found [here](https://github.com/sidex15/susfs4ksu-module/releases/). <br/>
To install modules, go to the "Modules" tab at the bottom and touch "+ Install", then find the module and install it. <br/>
Other main modules I would recommend to download to bypass all the integrity stuff to use banking apps are as follows: <br/>
[Play Integrity Fix by KOW](https://github.com/KOWX712/PlayIntegrityFix/releases/) <br/>
[TrickyStore](https://github.com/5ec1cff/TrickyStore/releases/) <br/>
[Tricky-Addon](https://github.com/KOWX712/Tricky-Addon-Update-Target-List/releases/)

# Issues
If you have any issues you can submit an issue, or message on this [telegram group](https://t.me/Wild_Kernels). If you would like to be a tester for Samsung specific kernels, send a message in the group and I can definitely add your Samsung kernel if available.

# Updating KSU Patch
If theres a new version of the KSU app, there will also be new kernel patches to go along with it to apply the update. For example, right now it's on version 1.0.8, which means the app is 1.0.8 and the patches in the kernel are 1.0.8. Lets say there's a 1.0.9 update. You can update the app, but then to have the latest features in the kernel, you need to update the kernel patch to 1.0.9 as well. <br/>
To do that, download FatalCoder254 [Kernel Flasher](https://github.com/fatalcoder524/KernelFlasher/releases/) and give it root access in KSU App. <br/>
Download the Anykernel3.zip from releases. <br/>
Open the app, select boot slot, select flash, then flash AK3 zip, then select the zip file, then reboot.

# Special Thanks
[TheWildJames](https://github.com/TheWildJames) for his Wild Kernels and all his help. <br/>
[sidex15](https://github.com/sidex15) for susfs4ksu module. <br/>
[simonpunk](https://gitlab.com/simonpunk/susfs4ksu) for making the actual susfs4ksu. <br/>
[FatalCoder254](https://github.com/fatalcoder524) for kernel flasher. <br/>
[Rifsxd](https://github.com/rifsxd) for making KernelSU-Next

If I'm forgetting a name that needs to be here just let me know!

# Donation
If anyone would like to donate, you can do so [here](paypal.me/NgadhnjimHoxha)
