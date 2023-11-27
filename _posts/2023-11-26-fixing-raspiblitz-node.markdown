---
layout: post
title:  "Fixing My RaspiBlitz Node"
date:   2023-11-26 10:16:00 -0500
show_title: false
show_edit_on_github: false
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    image: /img/Whirlpool/whirlpool.jpg
---

A quick post on how I resolved my issues with my RaspiBlitz device, which acts as one of my dedicated bitcoin nodes.

# The Problem
**The White Screen of DEATH!!** This initially occurred when I was attempting to update the version to a new major version that included a GUI update. I was unsuccessful at the first attempt, I then was moving so this node was packed up in a box and I'm finally getting back to it months later.

![White Screen](/img/RaspiBlitz/WhiteScreen.png)


# The Solution
1. Download a fresh RaspiBlitz image

    a. I followed the instructions listed on the Readme: [SD Card Flash Instructions](https://github.com/raspiblitz/raspiblitz#write-the-sd-card-image-to-your-sd-card)

2. Insert the new SD card into the RaspiBlitz device.

3. Go through RaspiBlitz Setup

    a. My First screen looked like this below to kick off the setup.

    ![Continue Setup](/img/RaspiBlitz/ContinueSetup.png)

    b. update the software if required during setup.

    ![Start Update](/img/RaspiBlitz/StartUpdate.png)

4. Complete installation and setup my Bitcoin node.

    ![Bitcoin Blockchain Sync](/img/RaspiBlitz/BitcoinSync.png)

<br/>

And that was it for me, it ended up being just a bad / corrupted install so a fresh SD card flashed image resolved my issues. I went through a fresh [RaspiBlitz setup process](https://github.com/raspiblitz/raspiblitz#setup-process-detailed-documentation) and am currently waiting for the Bitcoin blockchain to complete the sync process. Check ya later.
