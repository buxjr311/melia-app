<p align="center">
  <img src="icon.png" alt="Melia" width="128" height="128">
</p>

<h1 align="center">Melia</h1>

<p align="center">
  A privacy-first desktop email client for Linux.<br>
  Direct IMAP/SMTP, OS-keyring credentials, local SQLite, zero telemetry.
</p>

<p align="center">
  <a href="https://melia.buxjr.com">melia.buxjr.com</a>
  &nbsp;·&nbsp;
  <a href="https://github.com/buxjr311/melia-app/releases/latest">Latest release</a>
</p>

---

## Install

| Format | Command |
|---|---|
| **Flathub** | `flatpak install flathub com.buxjr.melia` |
| **Snap Store** | `sudo snap install melia` |
| **.deb (Debian/Ubuntu)** | Download `melia_<ver>_amd64.deb` from [Releases](https://github.com/buxjr311/melia-app/releases/latest) and `sudo dpkg -i` |
| **AppImage (any distro)** | Download `melia_<ver>_x64.AppImage` from [Releases](https://github.com/buxjr311/melia-app/releases/latest), `chmod +x`, and run |

All four formats track the same release cadence. Flathub and Snap Store auto-update; the .deb and AppImage do not — re-download for new versions.

## What it does

- IMAP and SMTP for Gmail, Outlook, Yahoo, Fastmail, and any standard mail server
- OAuth2 for Microsoft accounts; app-password setup with a built-in trust center
- Offline-first: read, search, and queue replies with no connection
- Full-text search across every account and folder
- Per-message dark mode rendering with contrast and padding correction
- Tracking-pixel neutralization, suspicious-sender warnings, DKIM/SPF/DMARC trust badges
- Drag-and-drop folder organization with multi-account sidebar
- Compose with rich text, inline images, attachments, signatures
- Desktop notifications, dock unread badge, EML file viewer

## Pricing

Free for one email account. A one-time **$10** unlock removes the account cap. No subscription, no trial, no recurring charges.

## About this repository

This repository hosts **release artifacts only** — `.deb`, `.AppImage`, `.flatpak`, `.snap`, the Flatpak `extra-data` binary tarball, the packaging-assets tarball, and `SHA256SUMS` / `SHA256SUMS.asc` per release. The source is proprietary and lives in a private repository.

Verifying a download:

```bash
# 1. Download SHA256SUMS, SHA256SUMS.asc, and the signing key
curl -LO https://github.com/buxjr311/melia-app/releases/latest/download/SHA256SUMS
curl -LO https://github.com/buxjr311/melia-app/releases/latest/download/SHA256SUMS.asc
curl -LO https://melia.buxjr.com/melia-public-key.asc

# 2. Verify the signature
gpg --import melia-public-key.asc
gpg --verify SHA256SUMS.asc SHA256SUMS

# 3. Verify the file you downloaded matches
sha256sum -c SHA256SUMS --ignore-missing
```

## Issues and feedback

Bug reports and feature requests: [Issues](https://github.com/buxjr311/melia-app/issues).
For licensing or commercial inquiries: melia@buxjr.com.

## License

Melia is proprietary software. See the EULA shown on first launch, or visit [melia.buxjr.com](https://melia.buxjr.com) for purchase and license terms.
