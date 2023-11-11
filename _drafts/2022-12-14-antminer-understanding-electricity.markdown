---
title:  "Understanding Electricity: Antminer Setup"
date:   2022-12-14 13:34:00 -0500
show_title: false
show_edit_on_github: false
cover: '/img/antminers9j.jpg'
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /img/antminers9j.jpg
---

# Intro
I have very limited knowledge of electricity in general. In highschool, I took a beginner's electrician class but that knowledge has since left so now I'm trying to learn from scratch so I can properly set up my Antminer S9's.

# Where did I buy?
 
- [KaboomRacks](https://t.me/s/kaboomracks)
- [NewEgg](https://www.newegg.com/)

Specifically, I purchased two of the [Bitmain Antminer S9J](https://www.asicminervalue.com/miners/bitmain/antminer-s9j-14-5th) models. The first one I paid $480.00 and the second one I paid $390.00, both miners came with a Antminer APW7 **P**ower **S**upply **U**nit so I didn't need to purchase anything additional.

# Power the Miner
### Electricity
If you already have a 220 volt outlet available then you have NOTHING to worry about regarding your electrical infrastructure as 220 is recommended for the Antminer mining devices. If you do NOT have a 220 outlet, then my suggestion is to install one whether that be with help from a licensed electrician or if you are capable to do the work yourself then go for it! 

### Fire it Up
Hook up your **P**ower **S**upply **U**nit, it does NOT matter which PSU connectors go where when connecting it to the miner. Just make sure you have all of the hashboards and everything hooked up properly and securely. Next, plug in the ethernet cable into the miner's ethernet port. And finally, plug in the PSU to the wall socket and let the mining begin :)

# Configuration
There's a few additional steps needed to enable your miner to join a mining pool as well as deposit the mining rewards into a wallet of my choosing. Here's the steps I went through to complete my configuration.

### Locate the Antminer IP address within in LAN.
In order to log into the Antminer dashboard, we need to locate the ip address that's been assigned to it. I used [Advanced IP Scanner](https://www.advanced-ip-scanner.com/) to locate the IP address for my Antminer S9J.
![Advanced IP Scanner Results](/img/AntminerIpAddress.jpg)

### Configure the Miner
In your browser, enter in the IP address. You'll be prompted to login, by default the Antminer credentials are set:

|:-----------------------------|----------------:|
| **User Id:**                 | root            |
| **Password:**                | root            |
   
![Antminer Dashboard Login Prompt](/img/AntminerDashboardLogin.jpg)

<br/>

# Miner Configuration
 Under the configuration tab, you'll see the pool connections. Since I obviously bought this used, the person that owned this miner before me had their settings still entered here. I'm going to replace these with my pool connections.
 ![Old Antminer Connections](/img/AntminerConfigInitialOpen.jpg)

## Slushpool Stratum V1
I'm using [SlushPool](https://slushpool.com) so I'm going to locate the V1 connections which are the connections you want if you're NOT using the [Braiins OS](https://braiins.com/os/plus). 

### Server Location URLs

|:---------------------------|-----------------------------------------------------:|
| **General**                | stratum+tcp://stratum.slushpool.com:3333             |
| **Europe**                 | stratum+tcp://eu.stratum.slushpool.com:3333          |
| **USA, East Coast**        | stratum+tcp://us-east.stratum.slushpool.com:3333     |
| **Brazil, South America**  | stratum+tcp://br.stratum.slushpool.com:3333          |
| **Canada**                 | stratum+tcp://ca.stratum.slushpool.com:3333          |
| **Singapore, South Asia**  | stratum+tcp://sg.stratum.slushpool.com:3333          |
| **Japan, Pacific**         | stratum+tcp://jp.stratum.slushpool.com:3333          |
| **Russia, Moscow**         | stratum+tcp://ru-west.stratum.slushpool.com:3333     |
| **Kazakhstan**             | stratum+tcp://kz.stratum.slushpool.com:33333         |

Add the URL that's closest to your current location into the pool configuration. If desired, you can fill in the "Worker" and "Password" to make your miner more descriptive and also prevent spamming from an entity attempting to log into your instance with default credentials.

![My Pool Configuration](/img/AntminerGeneralConfigMyPoolConnection.jpg)