---
title:  "Sparrow Wallet and my BitBox02"
date:   2022-06-20 11:00:00 -0500
show_title: false
show_edit_on_github: false
cover: '/img/SparrowWallet/sparrow-logo.jpg'
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /img/SparrowWallet/sparrow-logo.jpg
---
# Intro
This post will be about my use of the [Sparrow Wallet](https://sparrowwallet.com/) along with my [BitBox02](https://shiftcrypto.ch/bitbox02/) hardware wallet. In combination these devices are helping me accomplish great privacy and security when sending and receiving Bitcoin transactions, while at the same time increasing my understanding of these transactions by providing extreme detail using the Sparrow private explorer.

# Why BitBox02
A couple years back I purchased the [BitBox02](https://shiftcrypto.ch/bitbox02/) Bitcoin-only edition and I haven't regretted it for a second. It has top of the line security and a great user interface which allows for simple and easy usage. The BitBox02 has been designed around security and the potential vulnerabilities that its users could face when sending and receiving Bitcoin, so when I use the device I'm confident that my risk of compromise is extremely low.

One item to call out here, the Bitcoin-only edition is the ONLY option that you should buy if you're planning on purchasing a BitBox02. This edition has its firmware exclusively dedicated to supporting Bitcoin, which in turn means less code and less attack surface for potential malicious attacks.

## Features
- Open source hardware security
- Numerous ways to backup your wallet (SD Card, 24 word seed phrase)
- Uses [ATECC608A](https://www.mouser.com/new/microchip/microchip-atecc608a-crypto-devices/) secure chip
- 120 MHz microcontroller chip (faster than the ColdCard)
- [Anti-klepto](https://shiftcrypto.ch/blog/anti-klepto-explained-protection-against-leaking-private-keys/) technology, protects you against exposing your private keys
- Allows you to connect to your own Bitcoin node
- Connect via Tor functionality for increased privacy

<br/>

# Why Sparrow Wallet
[Sparrow Wallet](https://sparrowwallet.com/) is a non-custodial Bitcoin wallet with a strong focus on privacy, security, and usability. It is designed to be connected to your own Bitcoin full node and can operate in both online and offline fashions. It provides great advanced features that allow the ability to dig into your Bitcoin transactions for a clearer understanding, thus leading to a better control of your Bitcoin transactions.

## Features
- Desktop based wallet. Safer than a browser based wallet.
- Adheres to the PSBTs standard
- Supports Single sig and multisig
- All common hardware wallets are supported
- Utilizes the [Argon2](https://github.com/P-H-C/phc-winner-argon2) is a password-hashing function for increased encryption
- Lightweight wallet
- Has built in blockchain explorer so you can search any Bitcoin transactions since its inception back in 2009
- Allows [coinjoins](https://www.investopedia.com/terms/c/coinjoin.asp) with Whirlpool for increased privacy
- Provides a detailed view of byte level transactions.
- Provides full control and configuration during the transaction creation and signing process

<br/>

# Setup

## Sparrow Wallet Install
Download the Sparrow Wallet from the [downloads](https://www.sparrowwallet.com/download/) page.

## Verify the Release
I've preached this before, but ALWAYS verify your installation file is the one you expected to download and was not compromised during the download.

## Configuration
After you've verified your download, start the configuration.

Since I'm using my own node, I'm going to select the "Private Electrum server" option and enter the IP address for my node.

![Private Server Connection](/img/SparrowWallet/server-connection.jpg)

*Note: Click on the "Test Connection" button to confirm your connection is successful. You should see a message like shown in the screenshot above.*

## Create Wallet
Creating a wallet is extremely easy, simply navigate under the File menu and then select "New Wallet" (Shortcut CTRL+N).

Enter the wallet name and then click on "Create Wallet".

![Enter Wallet Name](/img/SparrowWallet/new-bitcoin-wallet.jpg)

## Wallet Settings

### Default Settings
For this post, I'm going to leave the "Policy Type" and "Script Type" settings defaulted but just be aware that these settings can be tweaked to your liking and to match whichever situation you are needing to address, whether that be a multisig situation or maybe you want to utilize Bitcoin Taproot; whatever it may be, Sparrow Wallet has you covered.

### Keystores
Now comes the fun :) connecting our BitBox02 wallet.

#### Connect Hardware Wallet
Under Keystores, click on the "Connected Hardware Wallet" button

![Connect Hardware Wallet](/img/SparrowWallet/keystores-connected-hardware-wallet.jpg)

#### Scan for device
At this point, we need to connect our BitBox02 wallet to our computer so it can be scanned and found by Sparrow Wallet.

Once you have your BitBix02 device connected to the computer, click on the "Scan..." button.
![Scan For BitBox02](/img/SparrowWallet/scan-for-devices.jpg)

#### Import BitBox02 Keystore
You should see your BitBox02 device displayed like shown below, simply click on the "Import Keystore" which will 
![Select BitBox Device](/img/SparrowWallet/select-bitbox-wallet-to-import.jpg)

You should now see your wallet and settings. Take note of the master fingerprint as this is how you can confirm the wallet identity if you have to restore it again in the future.

Then, click on the "Apply" button.
![Apply Settings](/img/SparrowWallet/apply-bitbox02-settings.jpg)

<br/>
# Send Bitcoin
Now that we have our BitBox02 setup in combination with the Sparrow Wallet, let's go ahead and demonstrate sending a Bitcoin transaction.

### Create Send Transaction
Click on the "Send" tab to open the Send Transaction window.

Within the top section of this screen you'll need to provide the Bitcoin address where you are sending the transaction, the amount of Bitcoin to send, and a label for your transaction.

![Send Bitcoin Settings](/img/SparrowWallet/send-bitcoin-settings.jpg)

One great feature to mention here is the ability to configure our "Fee" to the exact amount that we want.

If you drag the fee slider back and forth, you'll see different messages display such as "High Priority" or "Overpaid". I personally love this feature, as I've been a victim of a stuck Bitcoin transaction due to my fee being too low. 

![Overpaid Fee Message](/img/SparrowWallet/overpaid-fee-message.jpg)

For this example, I'll leave the transaction set to a high priority amount.

![High Priority Create Transaction](/img/SparrowWallet/high-priority-fee-create-transaction.jpg)

Then, click on the "Create Transaction" button.

<br/>
### Sign Transaction
On the next screen, you'll see the overview of your transaction where you can review the details once more before you sign and broadcast the transaction. Review this carefully to ensure you didn't make any mistakes.

You can even configure settings here to add a transaction delay based on either the block height or a specific date.

![Send Details For Delay](/img/SparrowWallet/send-transaction-details-tab.jpg)

Once you've reviewed the everything, click on the "Finalize Transaction for Signing" button.

![Send Final Overview](/img/SparrowWallet/send-transaction-final-overview.jpg)

<br/>

You'll need to sign the transaction using your BitBox02 device like you would for any other send transaction.

You should see the transaction details appear on your BitBox02 device.

![BitBox02 Sign Transaction](/img/SparrowWallet/bitbox-sign-transaction.jpeg)

Review the amount and address and if all looks correct, sign the transaction.

<br/>
### Broadcast Transaction
Once signed from your BitBox02 device, another screen will display in Sparrow Wallet for you to broadcast the transaction to the Bitcoin Blockchain.

Simply, click on the "Broadcast Transaction".

![Broadcast Bitcoin Send Transaction](/img/SparrowWallet/broadcast-send-bitcoin-transaction.jpg)

<br/>
If broadcasted successfully, you should see a similar message as shown below.

![Broadcast Bitcoin Send Transaction Confirmed](/img/SparrowWallet/broadcast-send-bitcoin-transaction-confirmed.jpg)

<br/>
And finally, as the confirmations are completed on the Bitcoin blockchain you should receive confirmation messages to inform you.

![Transaction Confirmations](/img/SparrowWallet/transaction-send-confirmed-completed.jpg)

<br/>

## Receive Bitcoin
In order to receive bitcoin, click on the "Receive" tab. You'll immediately see that your address is already loaded up with the QR Code displaying. You can click on the "Get Next Address" button to get your another address of yours to have the bitcoin sent to.

![Receive Bitcoin Screen](/img/SparrowWallet/receive-bitcoin.jpg)

Once you have your Bitcoin address, use that address to send some bitcoin to :)

<br/>
After sending it to your Bitcoin address, you'll receive a notification as soon as the transaction is detected.

![Receive Bitcoin Notification](/img/SparrowWallet/receive-bitcoin-notification.jpg)

<br/>

# Conclusion
Overall, those are the first steps I've taken with Sparrow Wallet and my BitBox02 device. It's been only a positive experience so far and I look forward to using more advanced functionlity like the capability for PSBT, multisig, etc. 

Good day y'all!


