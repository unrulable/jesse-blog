---
layout: page
title:  "Switching to Linux"
date:   2022-04-29 08:30:00 -0500
show_title: false
show_edit_on_github: false
cover: '/img/antiwindows.jpg'
image: '/img/antiwindows.jpg'
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /img/antiwindows.jpg
---

# Intro
Due to the increased monitoring and collection of data, which you can read through Microsoft's [privacy statement](https://privacy.microsoft.com/en-us/privacystatement) to see exactly what they are collecting and doing with our data, I'm switching all of my computers from Windows OS to Linux. This blog will document the adventure I went through when converting one of my computers...

<br/>
# Why Linux?
### Security
Windows is a blackbox. You have to put your trust and faith in Microsoft that their group of developers will be able to find near all of the security issues before releasing the OS to the public.

Linux is far superior in regards to security, it has a massive community of developers that are constantly reviewing the source code due to it being completely open-source. The developers can see every single line of code, greatly increasing the chances of finding and fixing a security issue before it becomes a [zero day](https://en.wikipedia.org/wiki/Zero-day_(computing)) attack.

<br/>
### Cost
This one is obvious, if you use Windows OS then you have to buy for the privilege to use it. I guess you could go sniffing around the black market for a free version ha but do so at your own risk.

Linux is free for the people, free speech for the people. If you have time, it's worth reading through the history of Linux and why it's free. Here's one [article](https://www.informit.com/articles/article.aspx?p=2118681&seqNum=2) on the topic.

<br/>
### Privacy
Once again, take Microsoft at their word and just look at their [Windows data collection summary](https://privacy.microsoft.com/en-us/data-collection-windows). Remember, this is just what they're willing to admit to, but big tech, including Microsoft, cannot be trusted; we're being watched.

Take Linux at their word and check out their [privacy](https://linuxmint.com/privacy.php) page. If you read through this page, you'll understand that they value privacy and security first and foremost, and knowing this, well... it just makes me feel all warm and cozy inside.

![Warm and Cozy](https://media.giphy.com/media/YnNKrPub6aYbc8u53S/giphy.gif)

<br/>
# My Adventure

### Goal
My goal was to STOP using the Windows OS. To accomplish this, I'm going to take my old gaming computer, currently running Windows 7 Professional, and install Linux OS on it. I built this computer back in 2012 so the hardware WAS considered good but it's day has since past and I'm now just trying to squeeze as much energy and time as I can out of this old thang.

I have two Western Digital [HDD](https://en.wikipedia.org/wiki/Hard_disk_drive)'s currently installed in my computer, so I'm going to re-purpose the 300 GB [VelociRaptor](https://en.wikipedia.org/wiki/Western_Digital_Raptor) HDD to now be the main hard drive for my Linux OS. This setup will be considered a [multi-boot](https://en.wikipedia.org/wiki/Multi-booting) setup, simply meaning, I'll have both Windows and Linux available to boot.

<br/>
### System Requirements
Linux Mint [FAQ](https://www.linuxmint.com/faq.php).

![System Requirements](/img/LinuxMintSystemRequirements.jpg)

<br/>
### My Computer Specs

|:--------------------------|----------------------------------------------:|
| **Operating System:**    | Windows 7 Professional                        |
| **Processor:**           | Intel© Core™ i7-2600K CPU @ 3.40GHz × 4       |
| **Memory (RAM):**        | 8.00 GB                                       |
| **Graphics Card:**       | NVIDIA Corporation GF116 [GeForce GTX 550 Ti] |
| **Hard Drive 1:**        | WD Caviar Black WD1002FAEX 1TB 7200 RPM       |
| **Hard Drive 2:**        | WD VelociRaptor WD3000HLFS 300GB 10000 RPM    |

<br/>
### Step 1: Backup Hard Drive
Knowing that I'm going to completely wipe and reformat my hard drive for Linux, I wanted to make sure I had all files backed up that were on that drive so I did a quick manual scan of my files, backup up what I cared about, and left the trash files.

*Just a note: I'm currently using a [Start9](https://start9.com) [Embassy One](https://store.start9.com/collections/embassy/products/embassy) private server, along with [File Browser](https://filebrowser.org/) and [Syncthing](https://syncthing.net/) to store all of my files across my computers. I plan to create a blog to cover these topics in the future.*

<br/>
### Step 2: Wipe Hard Drive
Now that I confidently have everything backed up, I'm going to wipe the hard drive. Wiping is different than deleting, when you wipe a hard, you erase EVERYTHING that is currently stored on it, whereas deleting can just mark files for deletion at a later point. To perform the wipe, I'm going to use [Partition Wizard](https://www.partitionwizard.com/), tbh, no specific reason for choosing this software; it's a good tool that is also free to use.

Once [Partition Wizard](https://www.partitionwizard.com/) is installed, I clicked on the drive I wanted to wipe and then selected "Wipe Disk".

![Wipe Disk](/img/WipeDisk.jpg)

<br/>
Next, I selected the ["Fill Sectors with Zero"](https://www.techopedia.com/definition/10143/zero-filling) wipe method. Since I'm re-purposing my HDD, not selling or giving it away, I chose the quickest wipe method but if you are giving it to another person then I would select a more complete disk wipe.

![Fill With Zero Wipe Method](/img/FillWithZeroWipeMethod.jpg)

<br/>
### Step 3: Choosing Linux Distro
Luckily, I was exposed to Linux during a work project, that was long ago but I recall setting up many virtual machines, using [Oracle VirtualBox](https://www.virtualbox.org/), and these VM's used an Ubuntu image. Ubuntu was nice to use when I got the chance, but would I call it my favorite? No, but I understood the benefits of it in general.

Figuring my knowledge and opinions were outdated on Linux in general, I decided to do some additional research and I came across [Linux Mint](https://linuxmint.com/). Short overview, I found that it's based off of Ubuntu, it persists the open-source philosophy and privacy features loved by many, while introducing a simpler installation process that births a beautiful desktop baby. I won't bore you with all of my sales pitch in this blog, you can do your own research on that topic if you want, but long story short, I chose [Linux Mint](https://linuxmint.com/) to install on my machine.
![Linux Mint Logo](/img/LinuxMintLogo.jpg)

<br/>
### Step 4: Download Linux
To download [Linux Mint](https://linuxmint.com/), I first navigated to the main [downloads](https://linuxmint.com/download.php) page. I clicked on the Linux Mint Cinnamon edition.

![Linux Mint Download Page](/img/linuxmintdownloadspage.jpg)

Scroll down the next page a bit and select a mirror to download it from. I selected the "advancedhosters.com" mirror.

![Linux Mint Mirrors Page](/img/linuxmintmirrors.jpg)

I saved the download to a location on my existing Windows machine so I could access the downloaded files in the next steps.

<br/>
### Step 5: Verify

Don't trust, verify!

Since anyone can generate their own [ISO image](https://en.wikipedia.org/wiki/Optical_disc_image), I verified that the image I just downloaded was what I expected to download.

There are steps for this posted on the [mirrors](https://linuxmint.com/edition.php?id=292) page.

![Linux Mint Verify ISO Message](/img/verifyfilesmessage.jpg)

Or even more detail instructions are provided [here](https://linuxmint-installation-guide.readthedocs.io/en/latest/verify.html).

<br/>
### Step 6: Create Bootable USB Drive
Next, I needed to create the [bootable drive](https://en.wikipedia.org/wiki/Boot_disk), which all of the steps for this are also well documented [here](https://linuxmint-installation-guide.readthedocs.io/en/latest/burn.html). I used a SanDisk 128 GB USB drive that I had already purchased a while back, I had no issue with the steps and my Sandisk USB drive was now bootable.

![SanDisk USB](/img/Sandiskusb.jpg)

<br/>
### Step 7: Installation
I next restarted my computer with the USB drive installed and entered bios. I can never remember which one it is ha so I was pressing F2, F10, and F12 simultaneously. Turns out it was DEL lol...
![Confused-Keyboard](https://media.giphy.com/media/52HjuHsfVO69q/giphy-downsized-large.gif)

<br/>
Now in the bios, I clicked the "Boot Menu(F8)" button, and then selected the USB flash drive to start the boot.

![Install Linux](/img/asus-uefi-bios-utility-ez-mode.jpg)

<br/>
Once Linux Mint was booted up from the USB drive, I clicked on the disc icon to start the Lint Mint installation.

![Install Linux](/img/InstallLinuxMintIcon.jpg)

There's also amazing installation documentation for this step [here](https://linuxmint-installation-guide.readthedocs.io/en/latest/install.html).

<br/>
After successfully completing the installation setup and configuration, Linux Mint is installed!
![Linux Mint](/img/linuxmintdesktop.jpg)

<br/>
### Step 8: Party
And just like that, the deed was done. Time to mark one more task off of my privacy 4 life list.

![Party](https://media.giphy.com/media/S4AnOkBwfcb4GyDzK7/giphy.gif)

<br/>
When booting my computer, I'll now have the option to boot either Windows or Linux Mint.
![Multi Boot Select](/img/MultiBootSelect.jpg)

<br/>
<br/>
I'll probably create another post for the first software and applications to install but for now that's a wrap, thanks for reading!
