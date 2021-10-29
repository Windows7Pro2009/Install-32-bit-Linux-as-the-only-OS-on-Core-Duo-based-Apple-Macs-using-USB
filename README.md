# Install-32-bit-Linux-as-the-only-OS-on-Core-Duo-based-Apple-Macs-using-USB
This guide focuses on how you can install Linux of 32 bit architecture on your aging Intel Mac as the only OS, which has the Core Duo 32 bit processor using USB instead of a DVD. With this, you can rejuvenate your old Mac. Do note that in this guide, you are wiping your entire hard drive with OS X, so if you are thinking that if you came to "dual boot" your old Mac with Linux, this guide isn't for you. Proceed with caution!

Things you'll need:
    • A USB drive of at least 8GB (to make a bootable Linux USB
    • A computer running Windows (this is for creating the bootable USB using Rufus)
    • A boot manager called rEFInd 
    • Obviously a 32 bit Intel Mac with a password protected account (you need a password so that Terminal will not complain about it)

Now let's go!
1. Go to your Windows machine and download your Linux distro of your choice (Note: it MUST be a 32 bit distro and should have a DE that is known to run smooth on your Mac. In this case, I'm using Linux Mint 19.3 Tricia MATE 32 bit)

2. While your distro is downloading, download the latest version of  Rufus (Link: https://rufus.ie/en/ )

3. If both of the files have downloaded, connect your USB drive.

4. Open Rufus and click the Device drop-down and then select the name of the USB you have just connected.


5. Click the Partition Scheme and Target System Type drop-down, and then select "MBR partition scheme for BIOS or UEFI."

6. Choose the File System drop-down, and then click "FAT32 (Default)."

7. Select the Cluster Size drop-down, and then click "4096 bytes (Default)."

8. Enter a new name for the USB storage drive in the New Volume Label field if you want to change the name from what it is currently.

9. Ensure that Quick Format, Create a Bootable Disk Using, and Create Extended Label and Icon Files have the boxes to the left of them checked under Format Options.

10. Select "FreeDOS" in the drop-down to the right of Create a Bootable Disk Using.

11. Click the disc icon to the right of FreeDOS. The Open dialog box appears. 
12. Navigate to the location where you downloaded the Linux installer, click the ISO associated with the Linux installer, and then click "Open." Where you previously selected FreeDOS in the Format Options section now says "ISO Image. A Download Required message may appear, prompting you to download additional Syslinux files to complete creating this file.

13. Click "Yes" to download any additional Syslinux files. Another message appears warning you that the image you selected is an ISOHybrid image.

14.Choose "Write in ISO Image Mode (Recommended)," and then click "OK." Another warning appears that all current information on your USB storage drive will be erased. 

15. Click "OK."

16. Click "Start" the Rufus USB Installer begins creating the bootable USB drive. The creation of the bootable USB Linux installer will be complete when the green progress bar at the bottom of the Rufus application is entirely green, and when the message below the progress bar says Ready. 

17. Click "Close" when Rufus is completed creating the bootable USB Ubuntu installer, and then remove the thumb drive from that computer.

18. Download the latest version of rEFInd from SourceForge (Link: https://sourceforge.net/projects/refind

19. Copy the rEFInd binary zip file to another USB drive with FAT32 format.

If you have completed all the steps above, go ahead and plug the USB drive to your Mac (the one where we copied the rEFInd binary zip file).

20. Uncompress the rEFInd binary zip file that you downloaded from SourceForge.

21. Open Terminal and navigate into the uncompressed rEFInd folder.

22. Drag the “refind-install” file to the Terminal and it will ask for the account password (this is where the password you created for your account comes into play). An automatic installer will install rEFInd into your EFI partition.

23. Disconnect the data USB drive and connect the bootable Linux USB drive you created at the beginning.
Restart your Mac and you’ll be presented with this screen
![image](https://user-images.githubusercontent.com/76607426/139415627-3c363215-d491-4911-8faf-8d9649e24e59.png)

24. Go to (Linux (Legacy) from <your-flash-drive>) and press the Return key. It will boot your Linux USB drive in BIOS emulation mode.

25. Select the "Linux Mint" (or the name of your particular distro) option.
  ![image](https://user-images.githubusercontent.com/76607426/139415998-046039bd-123c-4a09-ad1b-76fe1ee9d5be.png)
Note: The wording will vary slightly depending on the version of your distro’s version)
  
26. Wait for the Linux desktop to load. It shouldn't take more than a few minutes. Once it finishes, you can proceed with installing Linux on your hard drive.

27. If your Mac has booted to the live desktop, check if your Wifi, Bluetooth and all other devices work.

28. After checking, double-click "Install Linux Mint" (or your distro's install file). This disc-shaped icon is on the desktop. A window will open.

29. Select a setup language. Click the language that you want to use, then click Continue in the bottom-right corner of the window.
  ![image](https://user-images.githubusercontent.com/76607426/139416091-8c0921c3-298c-4fd5-93a3-7091222bfcea.png)

30. Set up Wi-Fi. Click a Wi-Fi network, enter the password in the "Password" text field, click Connect, and click Continue. (skip this step if you have already connected to WiFi before opening the ‘Install Linux Mint’ file for checking your hardware.

31. Check the "Install third-party software" box (necessary for all the hardware of your Mac to work with Linux) at the top of the page and click Continue.
 ![image](https://user-images.githubusercontent.com/76607426/139416172-3a740529-7284-4eb2-81b4-0c2bae9e742f.png)

32. Indicate that you want to replace your operating system with Linux. Check the "Erase disk and install Linux Mint" box, click Continue, click Install Now, and click Continue when prompted.
(Note: Doing this will erase your entire drive which has  macOS installed. But our main goal here is to wipe macOS and have Linux as the only OS on your Mac. This is not a dual boot guide. Remember what I've said in the description of this repository)

33. Select a time zone. Click a vertical time zone bar that correlates with your geographic location, then click Continue in the bottom-right corner.
  ![image](https://user-images.githubusercontent.com/76607426/139416405-7ca5ce3c-cc89-4c33-a7b9-5335ca98e2e5.png)

34. Select an operating system language. Click a language on the left side of the window, select a keyboard layout on the right side of the window, and click Continue.
![image](https://user-images.githubusercontent.com/76607426/139416458-780fc3bc-4e60-41d5-b8b1-946ff3e09681.png)

35. Enter your personal details. This includes typing in your name, your computer's name, your preferred username, and a password, and then clicking Continue. Linux will begin installing onto your computer.
  ![image](https://user-images.githubusercontent.com/76607426/139416537-4069f095-d743-474c-b8e9-64402f113f56.png)

36. Remove the USB flash drive from your computer. While your Mac probably won't try to reinstall Linux when rebooting, it's best to limit the number of boot options during the initial installation phase.
  ![image](https://user-images.githubusercontent.com/76607426/139416646-5b4becde-f7bb-4c3e-b335-95e9e3d73cc3.png)

37. Click Restart Now when prompted. Doing so will cause your computer to restart, thereby saving the installation on your hard drive.
  ![image](https://user-images.githubusercontent.com/76607426/139416792-e8928332-5c05-4948-8900-20f880aa2cbc.png)

38. When your Mac reboots, it will take you to the rEFInd boot menu. From there select “Linux (Legacy) from <your-volume-name>” (In my case, it shows as Linux (Legacy) from 23 GiB ext4 volume)
  ![image](https://user-images.githubusercontent.com/76607426/139417095-929595e0-073e-440c-a247-cfa7f04e8e9e.png)

39. After selecting it, your Mac will now boot into your newly installed partition of your Linux distro. The first boot will take quite a while so be patient. When it finally finishes booting, you’ll reach your desktop. You will now be able to use Linux on your computer like any other operating system.
![image](https://user-images.githubusercontent.com/76607426/139417205-9e938d1d-b445-4443-8c65-92915f280b90.png)

Congratulations! You installed Linux on your old Mac!
