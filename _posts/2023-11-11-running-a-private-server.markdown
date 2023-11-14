---
layout: page
title:  "My Personal Server"
date:   2023-11-11 05:30:00 -0500
show_title: false
show_edit_on_github: false
#cover: '/img/start9Embassy/start9EmbassyDevice.jpg'
image: '/img/start9Embassy/start9EmbassyDevice.jpg'
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /img/start9Embassy/start9EmbassyDevice.jpg
---
# Notes
This article was originally written in early 2022, I am completing it now after reviving my blog. Dated: 2023-11-12.

# Intro
Introducing the personal server, your own cloud where you can store your data privately, where you are in charge of your data and where you decide how to best manage YOUR data. This is the alternative to centralized services that I've chosen, and this post will be about my experience with the [Start9 Embassy](https://store.start9.com/products/embassy) personal server, how I set it up, and how it has completely replaced my use of common cloud storage services such as Google Drive, OneDrive, etc.

<br/>
# Big Tech Cloud Services
Let's start out with society's ever increasing reliance on big tech. We willingly hand over our data, and along with it our privacy, in return for a shiny app that promises to handle ALL of our data responsibility for us. What they fail to mention is the trade-off, and how when you forfeit responsibility to a third party, you also transfer all ownership, security, and trust of said data because it lives within their servers. In reality, what you're saying is I 100% trust this company to do the right thing with my data throughout the remainder of our relationship.

One of the most common cloud services is that of cloud storage like Google Drive or One Drive. These services store your data for you, and over the years, I've acquired and interacted with numerous services from Google, Apple, Microsoft, Amazon, etc. thus giving them my data, my location, my activity, and so on. I want to get away from cloud services, although easier said than done, within the past year, I've slowly been converting my use from big tech services to free and open source alternatives.

<br/>
# The Embassy One

## Software
[Start9 Embassy](https://store.start9.com/products/embassy) is a plug and play personal server device. It runs using the Embassy Operating System, which is completely open source, and it enables the ability to use other open source applications without the need for a trusted third party; everything runs within the embassy device itself.

## Hardware
I bought my physical hardware [device](https://store.start9.com/products/embassy) about a year ago. The initial setup, ran off of a SD card, but recently, there was a major version upgrade to [0.3.0](https://start9labs.medium.com/embassyos-0-3-0-f3d2d2ea016f) that required an [upgrade kit](https://store.start9.com/products/upgrade-kit), so it now runs using an 1 TB Solid State Drive ([SSD](https://en.wikipedia.org/wiki/Solid-state_drive)).

## Specs

|:----------------------------|---------------------------------------------------------------------:|
| **Operating System:**       | EmbassyOS 0.3.0                                                      |
| **Single Board Computer:**  | Raspberry Pi 4b (8GB)                                                |
| **Processor:**              | broadcom BCM2711, Quad core Cortex-A72 (ARM v8) 64-bit SoC @ 1.5GHz  |
| **Memory:**                 | 8GB LPDDR4-3200 SDRAM                                                |
| **Storage:**                | 1TB Samsung T7 SSD                                                   |
| **USB Ports:**              | 2 x USB 3.0; 2 x USB 2.0                                             |
| **Networking:**             | 2.4 GHz and 5.0 GHz IEEE 802.11ac wireless, Gigabit Ethernet         |
| **Dimension:**              | 3.54″ x 2.55″ x 1.02″ (90 cm x 65 cm x 26 cm)                        |

<br/>
Here's a screenshot of the device itself.
![Embassy Device](/img/start9Embassy/start9EmbassyDevice.jpg)

<br/>
***Note:*** *there's also the option to build your own, here is the [DIY Guide](https://start9.com/latest/diy).*

<br/>
# Embassy One Benefits

## Simplicity
Simple, plug and play setup

## Data Ownership
You own your data because it lives on your personal server device. Your files, pictures, etc. are all stored within the external SSD that is connected to the Embassy device.

## Censorship Resistance
Since both the data and services live on your Embassy device, there is no need for a "trusted" third party, so you can never be censored by a third party if you think or say something against the accepted narrative.

## Privacy
The Embassy uses end-to-end encryption along with the Tor network to onion route the communication requests and responses. This puts your privacy in your hands, you control what you want and don't want to share with the world.

<br/>

# Embassy Services
Embassy has its own marketplace where you can install a variety of applications ranging from Bitcoin to data management tools. 

Below is a full list of the current Embassy services as of July 2022.

|:----------------------------|---------------------------------------------------------------------:|
| **Bitcoin Core**       | A Bitcoin full node by Bitcoin Core                                           |
| **Bitcoin Proxy**      | Bitcoin Proxy enables you to specify several users and, for each user, the list of RPC calls they are allowed to make against your Bitcoin node. It also acts as a super charger for your pruned node.                                 |
| **BTCPay Server**      | BTCPay Server is a self-hosted, open-source cryptocurrency payment processor  |
| **Balance of Satoshis**| A tool for working with the balance of your Satoshis on LND                   |
| **Burn After Reading:**| A simple, fast, standalone service that uses Tor (.onion) ephemeral links to share encrypted messages and files that are destroyed (burned) after they are viewed.                                                                |
| **Core Lightning**     | Core Lightning (CLN) (formerly c-lightning) is a lightweight, highly customizable, and standards compliant implementation of the Lightning Network protocol.                                                                          |
| **Cups Messenger**     | Cups is a private, self-hosted, peer-to-peer, Tor-based, instant messenger.   |
| **Electrs**            | An efficient re-implementation of Electrum Server, inspired by ElectrumX, Electrum Personal Server and bitcoincore-indexd.     
| **Embassy Pages**      | Embassy Pages is a simple web server that uses directories inside File Browser to serve Tor websites.                                                                                                |
| **File Browser**       | File Browser provides a simple file managing interface which can be used to upload, download, organize, edit, and share your files.                                                                                                   |
| **Lightning Daemon**   | A complete implementation of Lightning Network node by Lightning Labs         |
| **Lightning Jet**      | Fully automated rebalncer for LND lightning nodes                             |
| **Lightning Terminal** | Lightning Terminal (LiT) is a browser-based interface for managing channel liquidity on your self-hosted LND node                                                                                                     |
| **LNDg**               | File Browser provides a simple file managing interface which can be used to upload, download, organize, edit, and share your files.                                                                                                   |
| **Mastadon**           | A free open-source social network server                                      |
| **Mempool**            | A Bitcoin node and network visualizer                                         |
| **Photoview**          | An easy way to organize and share your personal photos                        |
| **Ride the Lightning** | A full function, device agnostic, web user interface for managing lightning node operations |
| **Spark Wallet**       | A minimalistic wallet GUI for Core Lightning (CLN)                            |
| **Sphinx Chat**        | Messaging service built on top of the Lightning Network. Each message sent and received on Sphinx is actually a transaction on Lightning                                                                                             |
| **Synapse**            | Synapse is the battle-tested, reference implementation of the Matrix protocol |
| **Syncthing**          | Simple cloud data storage and sharing                                         |
| **Thunderhub**         | LND node manager where you can manage and monitor your node on any device or browser                                                                                                  |
| **Vaultwarden**        | A lightweight and secure password manager for storing and autofilling sensitive information such as usernames and passwords, credit cards, identities, and notes                                                                      |
