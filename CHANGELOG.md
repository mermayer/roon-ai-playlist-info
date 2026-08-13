# Changelog

This changelog records public information and documentation releases for Roon AI Playlist. Application and RoonAIViewer versions are listed separately because this repository contains neither their source code nor installers.

## [1.0.3](https://github.com/mermayer/roon-ai-playlist-info/releases/tag/v1.0.3) — 2026-08-13

### Added

- Complete English and German documentation for the selectable **Server + Configuration** Windows operating mode.
- Installer and first-launch guidance explaining the difference between the complete local application and an always-on server operated through a browser or RoonAIViewer.
- Instructions for opening the on-demand local configuration window, switching operating modes later, and understanding the required application restart.
- Explicit confirmation that Roon control, Wrapped, media processing, network triggers, scheduled tasks, and remotely controlled audiobook capture remain available in server mode.

### Changed

- Updated the documented Roon AI Playlist version to 1.0.466 and the public information release to 1.0.3.
- Expanded README, application overview, feature comparison, user guide, getting-started guide, Viewer guide, FAQ, privacy/security notes, release notes, and both changelogs.
- Clarified that Server + Configuration uses the existing data and service architecture while avoiding a permanently loaded local Player window.

## [1.0.2](https://github.com/mermayer/roon-ai-playlist-info/releases/tag/v1.0.2) — 2026-08-06

### Added

- Prominent English and German introduction to fully automatic AI playlist generation through the official Google Antigravity CLI without an AI API key or manual copy-and-paste step.
- Complete Antigravity setup and operating instructions covering installation, one-time Google sign-in, CLI verification, model selection, reasoning variants, automatic JSON hand-off, Roon matching, and troubleshooting.
- Explanation of the current free Antigravity tier and its high-quality Gemini models, with links to Google's live model and pricing pages and a clear warning that availability and quotas can change.
- Documentation of the application's cost safeguard: it never purchases credits and blocks already enabled paid G1/AI credits unless explicitly permitted.

### Changed

- Updated the documented Roon AI Playlist version to 1.0.463 and the public information release to 1.0.2.
- Expanded README, application overview, feature comparison, user guide, getting-started guide, FAQ, privacy/security notes, release notes, and both changelogs.

## [1.0.1](https://github.com/mermayer/roon-ai-playlist-info/releases/tag/v1.0.1) — 2026-08-04

### Added

- Detailed documentation of SpotBridge 1.0.0 as the separate native macOS bridge from the local Spotify process to Roon Audio Input.
- Description of the complete Spotify signal path, AAC and losslessly encoded Ogg-FLAC bridge transport, forwarded artist, title, album, and artwork information, and optional transport coordination.
- A dedicated rights notice covering the original documentation and clearly separating third-party trademarks, artwork, artist images, logos, and other embedded material.
- English and German changelogs.

### Changed

- Clarified that Roon AI Playlist presents and records Spotify playback only after it reaches Roon; it neither captures Spotify audio nor logs in to Spotify.
- Updated the public information release number to 1.0.1.

## [1.0.0](https://github.com/mermayer/roon-ai-playlist-info/releases/tag/v1.0.0) — 2026-08-04

### Added

- First public information release with an English default landing page and a complete German counterpart.
- Extensive English and German user guides, configuration reference, feature comparison, getting-started guide, privacy and security information, FAQ, application overview, RoonAIViewer documentation, and release notes.
- Screenshots and descriptions for the multi-zone Player, AI and Last.fm playlists, Live Radio, Spotify presentation, TIDAL tools, audiobook discovery, Wrapped, remote slots, network triggers, and RoPieee remote proxy.
- Clear product boundary: Roon AI Playlist complements Roon outside its GUI within the possibilities of the Roon Extension APIs and does not replace Roon.

[Deutsches Änderungsprotokoll](CHANGELOG_DE.md)
