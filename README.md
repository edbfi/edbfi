# Hi, I'm @edbfi 👋

Self-hosted tools for Plex and the \*arr stack, plus Docker images.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/edbfi/github-stats/generated/overview.svg#gh-dark-mode-only">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/edbfi/github-stats/generated/overview.svg#gh-light-mode-only">
  <img alt="GitHub statistics overview" src="https://raw.githubusercontent.com/edbfi/github-stats/generated/overview.svg#gh-light-mode-only">
</picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/edbfi/github-stats/generated/languages.svg#gh-dark-mode-only">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/edbfi/github-stats/generated/languages.svg#gh-light-mode-only">
  <img alt="GitHub language statistics" src="https://raw.githubusercontent.com/edbfi/github-stats/generated/languages.svg#gh-light-mode-only">
</picture>

## Released

| Project | What it is | Docker |
| --- | --- | --- |
| [EasyHDR](https://github.com/edbfi/EasyHDR) | Windows tray app. Turns HDR on when a configured app starts, and off when it closes | — |
| [mover-status](https://github.com/edbfi/mover-status) | Monitors Unraid Mover progress and sends notifications | — |
| [obzorarr](https://github.com/edbfi/obzorarr) | Year in review for Plex — "Spotify Wrapped", as a story-mode slideshow or a scrollable recap. Reads the Plex API, no Tautulli | [obzorarr-docker](https://github.com/edbfi/obzorarr-docker) |

## Functional, but WIP

Expect breaking changes.

| Project | What it is | Docker |
| --- | --- | --- |
| [docrewind](https://github.com/edbfi/docrewind) | Browser extension that reconstructs and replays the revision history of a Google Doc, locally. No backend, account, or telemetry | — |
| [otpravkarr](https://github.com/edbfi/otpravkarr) | Provisions Plex users into [Dispatcharr](https://github.com/Dispatcharr/Dispatcharr) and serves each user their own IPTV credentials and playlist | [otpravkarr-docker](https://github.com/edbfi/otpravkarr-docker) |
| [setun](https://github.com/edbfi/setun) | Self-hosted AI learning environment for classrooms. Students use pseudonymous access cards; educators control models, tools, schedules, and budgets | — |
| [zondarr](https://github.com/edbfi/zondarr) | Invite and user manager for Plex and Jellyfin, an alternative to Wizarr. Wizard steps around the invite: clicks, timers, ToS, text input, quizzes | [zondarr-docker](https://github.com/edbfi/zondarr-docker) |

## WIP, not yet functional

| Project | What it is |
| --- | --- |
| [comradarr](https://github.com/edbfi/comradarr) | Finds missing or upgradeable content across Sonarr, Radarr, and Whisparr, then requests it |
| [zimuarr](https://github.com/edbfi/zimuarr) | Subtitle translation for Bazarr. A translation is provably complete, or it did not happen |

## Homebrew taps

One tap, [homebrew-taps](https://github.com/edbfi/homebrew-taps), for macOS apps that homebrew-cask does not carry. A workflow checks upstream every 6 hours, re-hosts the release there, proposes cask updates for full CI and manual review, and appends a VirusTotal report when configured.

| App | Install |
| --- | --- |
| [FCast Sender](https://fcast.org/) | `brew install --cask edbfi/taps/fcast-sender` |
| [Flixor](https://github.com/Flixorui/flixor) | `brew install --cask edbfi/taps/flixor` |
| [Fred TV](https://github.com/Fredolx/open-tv) | `brew install --cask edbfi/taps/fredtv` |
| [Paicord](https://github.com/llsc12/Paicord) | `brew install --cask edbfi/taps/paicord` |
| [qView](https://github.com/jurplel/qView) | `brew install --cask edbfi/taps/qview` |

## Docker images

Forks of [hotio](https://github.com/hotio)'s images, with extra features.

Documentation and image tags: [web.edb.fi](https://web.edb.fi/).

```bash
docker pull ghcr.io/edbfi/<image>
```

| Image | Difference from upstream |
| --- | --- |
| [base-image](https://github.com/edbfi/base-image) | s6-overlay and VPN base for the images below, synced from `hotio/base` |
| [qbittorrent](https://github.com/edbfi/qbittorrent) | libtorrent v2 by default, plus the themes hotio dropped (VueTorrent) |
| [qflood](https://github.com/edbfi/qflood) | jesec's flood + qBittorrent, libtorrent v2 by default. hotio archived his |
| [sabnzbd](https://github.com/edbfi/sabnzbd) | SABnzbd with `ffprobe`, for post-processing scripts |

---

<sub>Last edited: 2026-09-23</sub>
