---
title: Linux on a Lenovo IdeaPad U410 (2)
author: Juan M Canovas
date: '2019-04-01'
slug: linux-on-a-lenovo-ideapad-u410-2
categories: []
tags: []
---

This is part 2 of the migration from Windows to Linux. Here I will focus on the steps I followed to get Linux running on this Lenovo IdeaPad U410. Briefly speaking, the steps boil down to:

1) Make (several) back up(s) of the data you wish to keep  
2) Update Windows     
3) Update BIOS version  
4) Disable UEFI    
5) Create a bootable USB stick with your favourite distro   
6) Install Linux        

**NOTE: We will not cover how to set up dual boot (keep Windows and Linux in the same computer and decide which OS you wish to boot into). Here we will format the hard drive and remove Windows completely.**     

--- 

# 1) Back up(s)   

**DO NOT use any backup program nor the built-in Windows backup utility**. Any of these will backup your data into a format that can not be read in Linux, so your *"back up"* won't be so.    

Instead, you should copy and paste the data you wish to save to an external hard drive, a USB stick or burn it to CDs/DVDs. This way, your data will be saved into FAT32 or NTFS formats, that can be read by a Linux system. It is also OK to store backup data in a Zip file.    

This step can be time-consuming, but it's worth the pain: if things go wrong it's better to be safe than sorry.   

# 2) Update Windows   

Nothing new here. Go to "Start" > "Settings" > "Update & Security" > "Check for updates"   

If there is an update available, it will download and install it. If your Internet connection is decent and the update is not too big, then all you can do here is **WAIT** (yes, bolded capital letters). Otherwise, all you can do is **WAIT, WAIT & WAIT**.   

Still lost? More details with screenshots included [here](https://www.wikihow.com/Update-Windows) 

**NOTE: This step might not be strictly necessary, but since we are going to update the BIOS booting into Windows we don't want any interference. And Windows updates can certainly be an interference.**  


# 3) Update the BIOS version   

The BIOS, short for Basic Input/Output System, is where we can choose where we wish to boot from. I am not going to delve into details, but if you want to know more about what it is and what it does check out the [Wikipedia page](https://en.wikipedia.org/wiki/BIOS). 

This Lenovo IdeaPad U410, and also the IdeaPad U310, came with a BIOS version which is **65CN89WW**. According to my Internet research when Windows *upgraded(?)* from 8 to 8.1 something made impossible to access the BIOS. In order to recover the access to the BIOS and select where we wish to boot from, we need to update it to the **65CN99WW** version. This new version is available on Lenovo's website and it should be the only place where you download the file.   

Also, you **must** watch this 2 min video by Lenovo: [check it out here](https://www.youtube.com/watch?v=9jMz7KV76VA&list=PLq4roe1E45w8b5L18aQqnSo6Z7wFARVG4&index=1). They explain all you need to know about the process.  

**NOTE: This is a delicate process. It can go wrong and screw things up to a no recovery point. DO NOT continue if you are not completely sure about what you are doing. Needless to say, I am not responsible if things go wrong.**   

I downloaded the file from Lenovo's webpage (see the 2 min video I linked above: they explain how to search and download the correct file from their website). It is a .exe file that I saved on the Windows desktop and then double-clicked.  

As soon as I double clicked, it started to install the new BIOS version and restarted the computer several times. Here you will see black screens with white console letters. The whole process took approximately 7 minutes for me, but it may be longer for you. **Be patient** and don't forget to do this with your battery charged AND your computer plugged in. Any power fluctuation can turn the process into a failure.   

# 4) Disable UEFI    

AFTER updating the BIOS, you will be able to access it and disable UEFI. What UEFI is? That is out of the scope of this post but we will need to turn it off in order to boot from a USB stick and install Linux. The way to go is:   

### 4.1) Press the "novo" button   

This is a tiny button located on the left side of your laptop (Lenovo calls it "novo button"). Press it once and wait.  

<img src=/img/linux_lenovo/01.jpg width="500"  />

### 4.2) Select BIOS setup     

<img src=/img/linux_lenovo/02.png width="500"  />

### 4.3) Navigate tabs and select the "Boot" tab    

To navigate between tabs using the arrows of your keyboard.   

<img src=/img/linux_lenovo/03.jpg width="750"  />

Inside the "Boot" tab, select "Boot mode" and hit enter. Once there, choose "Legacy Support" and hit enter again.   

<img src=/img/linux_lenovo/04.jpg width="750"  />

### 4.4) Save changes and exit   

Navigate to the "Exit" tab and select "Exit Saving Changes". Then select "Yes" and your laptop will boot into Windows.  

<img src=/img/linux_lenovo/05.jpg width="750"  />


# 5) Create a bootable USB stick with your favourite distro   

You will need a 4 GB (or larger) USB stick. This tutorial by the Ubuntu team is awesome: [link](https://tutorials.ubuntu.com/tutorial/tutorial-create-a-usb-stick-on-windows#0). Bear in mind that the USB will be formatted and all the data in it lost.    

When you get to tutorial's step #6 you don't need to select the Ubuntu ISO. I installed [Linux Mint](https://linuxmint.com/download.php) with the Cinnamon desktop and it worked flawlessly. WiFi, video, audio, webcam, microphone, keyboard shortcuts: all of them work perfectly!   


# 6) Install Linux        

Boot from the USB you created above. **Before installing anything, try the "live" mode**: this way you can check at no cost if the distro you wish to install supports the hardware you have. Using the "live" mode open YouTube and try watching a video: you'll check WiFi, video, and audio all at the same time.  

At this point, you may find that some hardware doesn't work with Linux. Some folks had to sacrifice the webcam or the keyboard shortcuts in order to install Linux. The final decision is up to you. As I mentioned above, all the Lenovo IdeaPad U410 hardware works perfectly with Linux Mint and the Cinnamon desktop.       

Once you have checked the hardware works, then restart your computer and install Linux. Before doing so, I recommend the videos in [Joe Collins' YouTube channel](https://www.youtube.com/channel/UCTfabOKD7Yty6sDF4POBVqA), particularly [this one](https://www.youtube.com/watch?v=G0AFuhVSvEk&list=PLq4roe1E45w8b5L18aQqnSo6Z7wFARVG4&index=3&t=0s). 


---

# Conclusion  

Getting rid of Windows brought this Lenovo IdeaPad U410 back to live **at no cost**. Now I have a fully capable laptop AND 730 dollars that otherwise would be in someone else's pocket. If you have any computer that turned out to be unusable due to [bloatware](https://en.wikipedia.org/wiki/Software_bloat), I encourage you to try Linux.  

Have you brought an old computer back to life? Do you have any questions? Please leave a comment and let us now!



