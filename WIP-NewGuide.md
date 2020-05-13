# Unlocking the bootloader
## Table of content

 1. [Disclaimers](#disclaimers)
 2. [Important information about this project](#important-information-about-this-project)
 3. [Unlocking your phone bootloader](#unlocking-your-phone-bootloader)
	 1. [Prerequisites](#prerequisites)
	 2. [Windows Phone checklist](#windows-phone-checklist)
	 3. [Using WPinternals to unlock your phone bootloader](#using-wpinternals-to-unlock-your-phone-bootloader)
 
 ## Disclaimers
 
 This project is not an official and reliable replacement for your phone operating system. You may lose device functionality, data, or not receive emergency calls or texts. We cannot be taken responsible for any damage or loss caused by this project or this guide. You have been warned.
 
 Some parts of this project are experimental at best, or not working at all. Be sure to read the current status of what works, and what doesn't as well as the Q&A.
 
 This project is not sold, and can't be sold. If you paid for this, you have been scammed. Microsoft Windows and Windows 10 on ARM are trademarks of Microsoft Corporation.
 
 ## Important information about this project
 
 It is important you read the latest information about this project.
 
 You can find the latest up to date status about what works and what doesn't here: https://github.com/WOA-Project/MSM8994-8992-NT-ARM64-Drivers/wiki/Status
 
 You can find information about general usability questions here: https://github.com/WOA-Project/MSM8994-8992-NT-ARM64-Drivers/wiki/Q&A
 
 You can find changelogs here: https://github.com/WOA-Project/MSM8994-8992-NT-ARM64-Drivers/wiki/Changelog
 
 You can find information about switching your USB port roles here: https://github.com/WOA-Project/MSM8994-8992-NT-ARM64-Drivers/wiki/USB-Mode-Switching
 
 You can find information about pre-release vibration motor settings here: https://github.com/WOA-Project/MSM8994-8992-NT-ARM64-Drivers/wiki/Vibration-Preliminary-Settings
 
 You can find information about FM Radio here: https://github.com/WOA-Project/MSM8994-8992-NT-ARM64-Drivers/wiki/FM-Radio
 
 ## Unlocking your phone bootloader
 
 In order to install Windows 10 Desktop onto your phone, its bootloader must be unlocked. No official bootloader unlock was ever available for these phones, so you need to rely on third party software to unlock your phone bootloader: WPinternals by HeathCliff74.
 
 ### Prerequisites
 
 WPinternals latest version: https://www.wpinternals.net/index.php/downloads
 
 Windows Device Recovery Tool (for connectivity drivers only): http://go.microsoft.com/fwlink/p/?LinkId=522381
 
 Win32DiskImager (for backup): https://sourceforge.net/projects/win32diskimager/
 
 Please install Windows Device Recovery tool and allow driver installations from the installer.
 Extract WPInternals zip archive to a folder, for use later on.
 
 ### Windows Phone checklist
 
 Boot up your phone, open the ```Settings app``` from the start screen, go to ```Update and Security```, and go to ```Device encryption```
 
 ![](https://i.imgur.com/0I4WVWh.png)
 
 Please make sure that settings is set to off. An unlocked bootloader is incompatible with device encryption (which is in reality bitlocker), leaving it on may cause issues during the unlocking process. If you just toggled that feature off, reboot the device.
 
 Make sure you have no SD Card inserted into your phone during the unlock procedure as this can cause issues later on. You are free to insert it back into the phone after the unlock process.
 
 It is recommended for you to backup your phone before unlocking its bootloader. It is also recommended to have the phone on the most recent update available for it as you won't be able to update it later on, and some windows phone versions may cause unexpected issues (like any 14393 OS build).
 
 ### Using WPinternals to unlock your phone bootloader
 
 #### Unlock the device bootloader 

![](https://i.imgur.com/wapDl0i.png)

Figure 1 WPInternals Main screen when a phone is connected 

WPInternals is a tool that will allow you to unlock your retail phone bootloader. This is required to use unsecure features and flash custom ROMs, operating systems. This portion is divided into two sections, the Spec A section, and the Spec B section. It is important to note WPInternals will only work with a single phone at a time. 

Phones with Bootloader Spec B: Lumia 1520, Lumia 435, Lumia 530, Lumia 532, Lumia 535, Lumia 630, Lumia 635, Lumia 638, Lumia 730, Lumia 735, Lumia 830, Lumia 930, Lumia 540, Lumia 640, Lumia 640 XL, Lumia 550, Lumia 650, Lumia 950, Lumia 950 XL 

Phones with Bootloader Spec A: Lumia 810 (not unlockable), Lumia 520, Lumia 521, Lumia 525, Lumia 620, Lumia 625, Lumia 820, Lumia 920, Lumia 925, Lumia 928, Lumia 1020, Lumia 1320 (No mass storage) 

#### Prerequisites 

WPInternals needs some files to unlock your device bootloader. To get those files, please go to the tool Download section, with the phone connected in normal mode. The fields for ProductType, ProductCode and OperatorCode should be prefilled, if not, make sure the phone is properly connected in normal mode to your computer. 

![](https://i.imgur.com/mOdKvj0.png)

Figure 2 Download section of the WPInternals tool 

In the download section, press the “Search” button, wait until the list gets populated. Once the list is populated, press the “Download all” button. WPInternals will download minimum 4 files. Even though it may only show 3 or 1 of them, after the big ffu image is downloaded, a new ffu file will show up downloading, but only after, so make sure both your device files, and the supplementary RM1085 ffu is downloaded. 

Note: Only Spec B phones may get a RM1085 ffu. 

If your phone doesn’t get an emergency package downloaded, this is abnormal, and you must download an emergency package for your device product code from a third-party source. You can find most of them at https://protobetatest.com/download/lumia-emergency-files/ 

To start unlocking your device bootloader, make sure your phone has enough battery charge. Go to the Manual mode section of WPInternals and select Switch to flash mode. 

![](https://i.imgur.com/LbX9Nfk.png)

Figure 3 Manual mode section of the WPInternals tool 

![](https://i.imgur.com/xCP3IWj.png)

Figure 4 WPInternals switching the phone to Flash mode 

Once switched to flash mode (Flash app), the tool will display more information about your device, including wherever the phone is considered a Spec A or Spec B phone. You may also want to read the linked warning about Samsung eMMCs if you phone contains a Samsung eMMC and is a Spec A phone. 

![](https://i.imgur.com/SsSbnxP.png)

Figure 5 WPInternals flash mode information screen showing eMMC information, and device product code information 

![](https://i.imgur.com/wzYdZe4.png)

Figure 6 (cont) WPInternals showing security features status 

#### Unlocking a Spec B device 

When attempting to unlock your phone and if the phone is already unlocked, you’ll get the following message in WPInternals: 

![](https://i.imgur.com/TOu2kYV.png)

Figure 7 When attempting to unlock an already unlocked phone, WPInternals will notify you it's already unlocked 

It is recommended you reflash the phone using WPInternals, and try a fresh unlock, for better results. If your phone isn’t already unlocked, you’ll instead get the following dialog: 

![](https://i.imgur.com/MIneEeQ.png)

Figure 8 Bootloader unlock screen for Spec B phones, using a compatible device FFU image 

This is the dialog shown when a compatible FFU image is selected. If your phone doesn’t have a compatible FFU image, you’ll get a third field, asking you to select one. All options must already be prefilled because we downloaded files using WPInternals download section. If the last field (the third one) isn’t prefilled, you did not use download all properly. If you want to manually fix this, you must obtain an FFU image for RM-1085 (even if your phone is not a RM-1085 device!), and you must select this for the support FFU image. Once everything is confirmed selected, you can then proceed to press the unlock button in WPInternals. 

When pressing the unlock button, you’ll see a series of screen like this: 

![](https://i.imgur.com/G9LwJgD.png)

Figure 9 WPInternals initializing the bootloader unlock process 

![](https://i.imgur.com/zQFPL5H.png)

Figure 10 WPInternals scanning for a Flashing profile, this may take a while depending on the device you're unlocking, do not interfere with this process 

![](https://i.imgur.com/8Bxmv9o.png)

Figure 11 WPInternals flashing the unlocked bootloader (Part 1 of the bootloader unlocking process) 

![](https://i.imgur.com/QtCyINE.png)

Figure 12 WPInternals asking you to manually reset the phone using power for 15 seconds, halfway throughout the unlock process 

![](https://i.imgur.com/Pn2hoib.png)

Figure 13 WPInternals flashing an unlocked bootloader (Part 2 of the unlock process) 

Once this whole process is finished, your phone has an unlocked bootloader. 

Note: For Lumia 950, Lumia 950 XL, Lumia 550, Lumia 650, if you unlock your phone on an unsupported OS version, your phone will boot into a blue “sad face” screen. You can however still access mass storage mode via interrupting the bootloader. 
 

#### Unlocking a Spec A device 

When a phone is already unlocked, you'll have this screen shown in WPInternals, without an emergency flash loader section. 

![](https://i.imgur.com/r5OVJMa.png)

Figure 14 Bootloader unlock screen for Spec A phones, using a phone already unlocked 

It is recommended you reflash the phone using WPInternals, for better results. 

To unlock your device, you’ll need to pick the ffu you previously downloaded using WPInternals in the first field, for the second field, pick the folder where WPInternals downloaded the HEX file (should be the same folder as where the FFU is). You’ll also need an Engineering SBL3 partition dump. To obtain such file, you can go to <TODO LINK>. You must make sure to use an engineering SBL3 designed for your phone, and not any other one. Flashing a wrong SBL3 may harm your phone! 

![](https://i.imgur.com/qN6UwSM.png)

Figure 15 Bootloader unlock screen for Spec A phones, using a phone not already unlocked 

Once you verified every field is correct, you can press the unlock button, and WPInternals will start the unlocking process. You may see those screens during the unlocking process, do not interfere with the unlocking process. 

![](https://i.imgur.com/Tc0z5qJ.png)

Figure 16 WPInternals preparing the unlocking process and preparing to switch the phone to Emergency Download mode 

![](https://i.imgur.com/XurdXon.png)

Figure 17 WPInternals forcing the phone to switch to EDL 

![](https://i.imgur.com/6fVB9nu.png)

Figure 18 WPInternals flashing the unlocked bootloader to the device 

![](https://i.imgur.com/Ki5ztiy.png)

Figure 19 WPInternals escaping from RED flash app issue 

Once the phone is unlocked, you’ll have to enable root access (specifically for EFIESP) to patch integrity checks in EFIESP, to do so, go to the enable root access section, and click on unlock phone. 

![](https://i.imgur.com/J0ODopw.png)

Figure 20 Enable root access section (via mass storage mode) 

Once done, your phone will be unlocked. Here’s a picture showing the security configuration of the phone after the unlocking process: 

![](https://i.imgur.com/RWvuIP8.png)

Figure 21 Phone state after unlocking, any flash of the device will get rid of the unlocks 

#### Switch to mass storage mode 

![](https://i.imgur.com/AQ98pq2.png)

Figure 22 Manual mode section of the WPInternals tool 

To switch your phone to mass storage mode, many ways are offered to you after unlocking the phone bootloader. For Spec A phones, you can do the following: 

Press the camera button at boot up 

Interrupt the boot sequence using WPInternals and switch to mass storage mode 

Switch to mass storage mode using WPInternals from a supported device mode (ie normal mode) 

Use thor2 -mode rnd -bootmsc 

For phones with bootloader Spec B, you must use WPInternals to switch to mass storage mode. 

Phones with bootloader Spec A additionally support reboot commands from mass storage mode. To reboot from mass storage mode on phones with bootloader Spec A, run the following:  

thor2 -mode rnd -reboot 

To reboot a Spec B phone from mass storage mode, you must press the power button until the phone vibrates. 
 

#### Backup of the phone 

To avoid issues going forward, and avoid a brick of your device, you must perform a full eMMC backup. You must also make sure to keep this whole eMMC backup intact, and in a safe place. You can compress it using 7zip using ULTRA compression. It will generally compress well. To create such backup file, open Win32DiskImager, and put your phone in mass storage. 

![](https://i.imgur.com/v80ZPLp.png)

Figure 23 Win32DiskImager, along with the device field 

In the device field of the tool, select the drive letter corresponding to your phone, (look for the MainOS partition). You can additionally find out the drive letter of the phone by look at WPInternals mass storage mode screen. Once properly selected, click the blue folder icon. A file open dialog will open. It is important to note, it’s not because it says open you must open an existing file. You want to go to a location where you got enough free space (account for the size of the phone storage entirely) and in the bottom input field of the open dialog, enter the name of the image file you want to create. Once done, press read, the tool will do the rest for you. 

![](https://i.imgur.com/QRRsyiz.png)

Figure 24 The "open" dialog with the bottom field 
 
