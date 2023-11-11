---
title:  "Serializing 3D Printed Objects Using Bitcoin"
date:   2022-08-03 13:16:00 -0500
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

# Intro
The other day I was 3D printing some items (tooth brush holder and doll furniture if you must know) and had a thought about what the process would be for serializing any 3d printed objects. My mind started gearing towards Bitcoin naturally and how I might be able to utilize its functionality for serialization. I wasn't sure if there were existing processes out there so I decided to do a bit of digging... and turns out there are some options :)

# OP_RETURN
Introducing [OP_RETURN](https://en.bitcoin.it/wiki/OP_RETURN), a built in function within the Bitcoin script that allows the ability submit arbitrary data to the Bitcoin blockchain. OP_RETURN transactions contain no bitcoin value, strictly data, so these transactions are marked as invalid since they should not be mined. The invalid status informs the network that this transaction can be discarded thus alleviating any potential clogging of the network that these non-currency related transactions may cause if this functionality didn't exist.

### What's in OP_RETURN

### Example Transaction

# NBitcoin
My preferred programming language is C# so I went looking for resources and found NBitcoin, a bitcoin core API.

# Project Setup
### Dotnet new winforms

### Add Packages

### Setup UI