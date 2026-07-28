<p align="center">
  <img src="icon.png" alt="Melia" width="128" height="128">
</p>

<h1 align="center">Melia</h1>

<p align="center"><strong>The Modern Email Client for Linux</strong></p>

<p align="center">
  Direct IMAP/SMTP. Credentials in your system keyring. Mail in a local database.<br>
  No telemetry, no account, no subscription.
</p>

<p align="center">
  <a href="https://github.com/buxjr311/melia-app/releases/latest"><img src="https://img.shields.io/github/v/release/buxjr311/melia-app?label=latest&color=2f6fed" alt="Latest release"></a>
  <a href="https://github.com/buxjr311/melia-app/releases"><img src="https://img.shields.io/github/downloads/buxjr311/melia-app/total?color=2f6fed" alt="Downloads"></a>
  <img src="https://img.shields.io/badge/license-proprietary-lightgrey" alt="Proprietary">
  <img src="https://img.shields.io/badge/platform-Linux%20x86__64-lightgrey" alt="Linux x86-64">
</p>

<p align="center">
  <a href="https://melia.buxjr.com">melia.buxjr.com</a>
  &nbsp;·&nbsp;
  <a href="https://melia.buxjr.com/download">Download</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/buxjr311/melia-app/releases/latest">Latest release</a>
  &nbsp;·&nbsp;
  <a href="https://melia.buxjr.com/faq">FAQ</a>
</p>

<p align="center">
  <img src="https://melia.buxjr.com/img/melia_full_app_hero.png" alt="Melia's three-pane window: accounts and folders, message list, and reading pane" width="900">
</p>

---

## Install

Melia ships for **x86-64 Linux** in four formats, all built from the same release.

**Snap** — auto-updates through the Snap Store.

```bash
sudo snap install melia
```

**Debian / Ubuntu** — updates in-app.

```bash
curl -LO https://github.com/buxjr311/melia-app/releases/latest/download/SHA256SUMS
grep '\.deb$' SHA256SUMS   # find the current filename
# then download that file from the Releases page and:
sudo dpkg -i melia_<version>_amd64.deb
```

**AppImage** — any distribution, no install step. Updates in-app.

```bash
chmod +x melia_<version>_x64.AppImage
./melia_<version>_x64.AppImage
```

**Flatpak** — sideload bundle from the release page.

```bash
flatpak install --user melia_<version>_x64.flatpak
```

Every file is listed on the [latest release](https://github.com/buxjr311/melia-app/releases/latest). See [Verify your download](#verify-your-download) before installing.

### Staying up to date

Melia checks for new versions and tells you what changed, then does the right thing for how you installed it:

| How you installed | How updates arrive |
|---|---|
| Snap Store | Automatic, in the background |
| `.deb` or AppImage | **Update Now** in Settings → Updates downloads and installs it |
| Flatpak (from Flathub, once listed) | `flatpak update com.buxjr.melia` — offered with a copy button |
| Sideloaded snap or Flatpak | Points you back to the download page |

A **Release Tide** timeline in Settings → Updates lets you scroll back through every version you skipped and read what each one changed.

## What makes it different

**Your mail lives on your machine.** Local-first storage, direct IMAP/SMTP, zero telemetry — and a built-in **Connection Monitor** that lets you *watch* every outbound connection the app makes, with a full log of what was sent where. The privacy claim is one you can verify rather than take on faith.

**Every email rendered the way it was meant to look.** Automatic contrast and spacing audits run on *every* message, and a real dark mode transforms even stubborn HTML mail. Newsletters, receipts, and marketing blasts read cleanly in either theme.

**Instant, and it works offline.** The whole mailbox is cached locally, so it opens at SSD speed and keeps working when the network doesn't. Every action applies immediately; sync runs in the background and never makes you wait. Replies written offline queue in the Outbox and go out on reconnect.

**Knows who's really emailing you.** Real cryptographic SPF/DKIM/DMARC verification rather than blind header-trust, plus brand-impersonation and suspicious-sender detection, and a Trust Center to block or trust senders by address, domain, or pattern.

**Shuts out the spies in your inbox.** Tracking pixels detected and neutralized, remote images blocked by default, read receipts never sent automatically, and one-click unsubscribe. Senders don't get to know when, or whether, you opened their mail.

**Shows you where a link really goes.** Hover any link to see its true destination with the real domain highlighted, and Melia names the trick when one is in play: text that lies about where it points, look-alike domains using Cyrillic characters, redirect wrappers unwrapped to the final address. Every check is lexical and on-device — Melia never contacts the link, so reading your mail never tips off a server.

**A native Linux app, not a web page in disguise.** Credentials sealed in your system keyring, real keyboard shortcuts throughout, and a UI that behaves like a desktop application.

**Dressed to match your desktop.** Light, Dark, and time-based Auto, plus around 25 popular Linux palettes — Catppuccin, Nord, Dracula, Gruvbox, Tokyo Night, Solarized, Rosé Pine, Everforest and more — and a customizable accent color.

## Features

<details>
<summary><strong>Mail &amp; accounts</strong></summary>

- Unlimited IMAP/SMTP accounts, each in its own folder tree
- One-click setup for 30+ providers — Gmail, Outlook/Office 365, Yahoo, Fastmail, Proton Mail Bridge, self-hosted
- OAuth2 sign-in for Microsoft accounts; Gmail and other providers use app passwords
- Optional **All Inboxes** and **All Spam** views that merge every account, while each message still acts on its real account and folder
- IMAP IDLE push with polling fallback, plus a configurable sync interval
- Choose how much history to download per account, from recent mail to everything on the server
- Offline-first: read, search, and act with no connection; deferred operations replay on reconnect
- Outbox queues mail written offline
- Full-text search across every account and folder

</details>

<details>
<summary><strong>Reading</strong></summary>

- Three-pane or two-pane layout, switchable
- Smart padding detection, contrast auditing, and dark-mode transformation on every message
- Inline CID images (Outlook signatures, company logos) render correctly
- Pop any message out into its own window, with the main list marking it as checked out
- Attachment lightbox, `.eml` viewer that opens attached mail in place, raw header inspector, print
- Message density, preview snippets, and email font/size of your choosing
- Delivery and read-receipt tracking for mail you sent

</details>

<details>
<summary><strong>Composing</strong></summary>

- Rich-text editor with inline images and drag-and-drop attachments
- Inline reply, or compose in a separate window
- Per-account signatures, plain or full HTML with a live preview
- Send-as aliases: additional addresses per account, each with its own name, reply-to, and signature — replies auto-select the alias the mail was addressed to
- Drafts auto-save; **Undo Send** holds outgoing mail for a few seconds
- Contact autocomplete, spell check, configurable send shortcuts

</details>

<details>
<summary><strong>Organizing</strong></summary>

- Drag-and-drop between folders, including across accounts, with undo
- Create, rename, and delete folders and subfolders
- Opt-in per-account Archive with a one-key sweep
- Inbox rules that file, spam, trash, or auto-forward matching mail
- Gmail labels for Gmail and Workspace accounts: colored chips and folder-tree dots, apply/remove/create over plain IMAP with no Google API, custom colors, and conversation-sticky labels
- Filters for unread, flagged, and attachments, stackable with search
- Tidy merges duplicate folders; Trim bulk-deletes old mail
- Keyboard-navigable folder tree — hold Ctrl and use the arrows

</details>

<details>
<summary><strong>Privacy &amp; security</strong></summary>

- Connection Monitor with a per-connection activity log
- Trust Center for blocked and trusted senders, by address, domain, or pattern
- Tracking-pixel detection and neutralization; remote images blocked by default
- SPF/DKIM/DMARC/ARC verification with honest badges — "Authenticated" means the sending domain is genuine, not that the message is safe
- Suspicious-sender and brand-impersonation detection
- Link-safety hover previews, entirely on-device
- Read receipts never sent automatically
- RFC 8058 one-click unsubscribe
- Credentials stored in the OS keyring, never in a config file

</details>

<details>
<summary><strong>Interface</strong></summary>

- Light, Dark, Auto, and around 25 community palettes, plus a custom accent color
- Interface zoom for the whole UI, independent of email text size
- Contacts manager with VIP marking, notes, and domain grouping
- Desktop notifications with custom sounds, per-account overrides, and a dock unread badge
- Frameless window with integrated controls
- Release Tide timeline showing what changed in every version

</details>

## Pricing

**Free for one account, forever** — every feature, no trial countdown, no feature gates.

**$10 once** unlocks unlimited accounts, on up to 5 machines. No subscription, no "Pro" tier, no recurring charges.

## Verify your download

Every release ships a `SHA256SUMS` file signed with Melia's GPG key, so you can confirm a download came from us and arrived intact. Worth doing for any app you install outside a distribution repository.

```bash
# 1. Fetch the checksums, the signature, and the signing key
curl -LO https://github.com/buxjr311/melia-app/releases/latest/download/SHA256SUMS
curl -LO https://github.com/buxjr311/melia-app/releases/latest/download/SHA256SUMS.asc
curl -LO https://melia.buxjr.com/keys/melia-public-key.asc

# 2. Verify the checksums were signed by us
gpg --import melia-public-key.asc
gpg --verify SHA256SUMS.asc SHA256SUMS

# 3. Verify your download matches its checksum
sha256sum -c SHA256SUMS --ignore-missing
```

Signing key fingerprint:

```
FB77 913C 2C0C 2747 5E40  1B95 50C4 B20B F021 80A0
```

## System requirements

| | Minimum | Recommended |
|---|---|---|
| Architecture | x86-64 | x86-64 |
| OS | Ubuntu 22.04 or equivalent | Ubuntu 24.04 or newer |
| Display server | Wayland or X11 | Wayland |
| RAM | 512 MB | 1 GB |
| Disk | 200 MB plus your mail | 500 MB plus your mail |
| Resolution | 1280×720 | 1920×1080 or higher |

## About this repository

This repository hosts release artifacts only: the `.deb`, `.AppImage`, `.flatpak`, and `.snap` builds, the binary tarball the Flatpak build pulls from, the packaging-assets tarball, and `SHA256SUMS` / `SHA256SUMS.asc` for each release. Melia's source is proprietary and lives in a private repository.

Issues here are the right place for bug reports and feature requests, and they get read.

## Issues and feedback

Bug reports and feature requests: [Issues](https://github.com/buxjr311/melia-app/issues).

Licensing, purchases, and commercial inquiries: melia@buxjr.com

## License

Melia is proprietary software. See the [EULA](https://melia.buxjr.com/eula), or the copy shown on first launch.
