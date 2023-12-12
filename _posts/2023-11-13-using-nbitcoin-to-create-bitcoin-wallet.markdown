---
layout: page
title:  "NBitcoin Create Wallet Code"
date:   2023-11-13 19:31:00 -0500
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

I believe it's important to learn how to code in the Bitcoin ecosystem and be exposed to the functionality. This is a quick post on how I used the C# package called [NBitcoin](https://github.com/MetacoSA/NBitcoin) to create code that creates a new Bitcoin wallet. I asked myself, why trust someone else and THEIR code to create MY wallet when I can trust my OWN code. Overall, the code is extremely simple, thanks to the NBitcoin package, but the idea behind it is extremely powerful.

_Note: This code is used in a .NET API_
<br/>

# 1.) Create Wallet Code
```cs
    public async Task<ActionResult<CreateWalletResponse>> CreateNewWallet()
    {
        // Generate a new BIP39 mnemonic phrase with a secure entropy
        Mnemonic mnemonic = new Mnemonic(Wordlist.English, WordCount.Twelve);
        string generatedMnemonic = mnemonic.ToString();

        // Derive the root key from the mnemonic and passphrase
        ExtKey extendedKey = mnemonic.DeriveExtKey();

        // Derive a Bitcoin address from the extended key
        Key privateKey = extendedKey.PrivateKey;
        BitcoinAddress bitcoinAddress = privateKey.PubKey.GetAddress(ScriptPubKeyType.Legacy, Network.Main);

        // Set the response and return it
        var response = new CreateWalletResponse
        {
            Mnemonic = generatedMnemonic,
            BitcoinAddress = bitcoinAddress.ToString()
        };

        return await Task.FromResult(response);
    }
```
<br/>

# 2.) Recieve Bitcoin
```cs
    public class RecieveBitcoinController : ControllerBase
    {
      private ExtKey extendedPrivateKey;
      private ExtPubKey extendedPublicKey;
      private int addressIndex;

      /// <summary>
      /// The recieve bitcoin constructor
      /// </summary>
      public RecieveBitcoinController()
      {
          // Initialize wallet properties
          extendedPrivateKey = new ExtKey();
          extendedPublicKey = extendedPrivateKey.Neuter();

          // Defaulting to the first address index for now
          addressIndex = 0;
      }

      /// <summary>
      /// Method to generate a new receiving address
      /// </summary>
      /// <param name="existingAddress"></param>
      /// <returns></returns>
      [HttpPost]
      [Route("api/receivebitcoin")]
      public ActionResult<string> GenerateReceivingAddress([FromBody] string existingAddress)
      {
          // If an existing address is provided, use it to generate the extended key
          if(!string.IsNullOrEmpty(existingAddress))
          {
              extendedPrivateKey = new ExtKey(existingAddress);
              extendedPublicKey = extendedPrivateKey.Neuter();
          }

          // Generate a new receiving address based on the current address index
          BitcoinAddress address = extendedPublicKey.Derive((uint)addressIndex).PubKey.GetAddress(ScriptPubKeyType.Legacy, Network.Main);
          addressIndex++;

          return Ok(address.ToString());
      }
    }
  ```

<br/>

# 3.) Create a UI (Optional)
100% optional as you can directly interect with the code by create a simple API and exposing a couple endpoints. Although, I'm an extremely visual person in regards to development and learning in general so I went ahead and started with a Windows Forms client. I know barf, old tech lol but it's really easy to create code that runs directly on my personal machine, this is a critical step if I ever planned on allowing others to use the application, I would want them to download and run it on their machines. Anyways, below is the code for the application.

I created a simple setup for creating a wallet, storing multiple wallets, and encrypting/decrypting the wallet credentials.
![Alt text](/img/WalletUI/image.png)

<br/>

Once in the wallet, the main functionality is under Recieve and displays next address from the wallet.
![Alt text](/img/WalletUI/image2.png)
