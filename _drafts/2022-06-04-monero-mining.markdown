---
title:  "Monero Mining"
date:   2022-06-04 06:46:00 -0500
show_title: false
show_edit_on_github: false
article_header:
  type: overlay
  theme: dark
  background_color: '#203028'
  background_image:
    gradient: 'linear-gradient(135deg, rgba(34, 139, 87 , .4), rgba(139, 34, 139, .4))'
    src: /img/Whirlpool/whirlpool.jpg
---

Monero is a cryptocurrency that should be used in combination with Bitcoin. Bitcoin is pseudoanonymous in nature, meaning no personal identification is tied to your Bitcoin wallets/transactions but Bitcoin is completely transparent so your wallet can be monitored. This monitoring is not ideal for our digital privacy so I suggest using Monero in combination with Bitcoin, as it has superior privacy properties that allow its users to be completely anonymous.

# Monero Privacy
How Monero privacy works...

# Install Monero Wallet
Navigate to the [Monero downloads](https://www.getmonero.org/downloads/) page, and then select the download depending on what system you are using.

Since I'm using Linux Mint, a Debian based system, I navigated to this [page](https://gitlab.com/whonix/monero-gui#how-to-install-monero-using-apt-get) for steps on installing the Monero GUI.

### Step 1: Download Signing Key
Download the signing key first using this command:
{% highlight CMD %}
   wget https://www.whonix.org/derivative.asc
{% endhighlight %}

### Step 2: Add the Signing Key
{% highlight CMD %}
   sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
{% endhighlight %}

### Step 3: Add the Repository
{% highlight CMD %}
   echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.whonix.org bullseye main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
{% endhighlight %}

### Step 4: Update Packages
{% highlight CMD %}
   sudo apt-get update
{% endhighlight %}

### Step 5: Download Monero GUI
{% highlight CMD %}
   sudo apt-get install monero-gui
{% endhighlight %}

<br/>
# Configuration
### Desktop Entry
When you open the Monero GUI for the first time you'll be prompted to enter a desktop entry. Go ahead and select "Yes".
![Create Desktop Entry](/img/Monero/create-desktop-entry.jpg)

### Mode
Select the mode for your wallet. I'm using advanced mode because I want a copy of the Monero blockchain downloaded locally on my computer. I suggest this for ALL setups, you can select the "Simple" setup as well, but just realize that you're putting the trust of the Monero blockchain data in someone else's hands since you're relying on their copy of the Monero blockchain.

![Mode](/img/Monero/mode-selection.jpg)

<br/>

# Create Monero Wallet

### Wallet Options
Since this was my first time using Monero, I selected the "Create a new wallet" option.
![Create Wallet Options](/img/Monero/welcome-create-wallet-options.jpg)

### Daemon
We're going for the strongest privacy possible here, so I selected the first option which will spin up a Monero node to run in the background. This will be our node that we can connect to, thus eliminating the need to trust anyone else's node.
