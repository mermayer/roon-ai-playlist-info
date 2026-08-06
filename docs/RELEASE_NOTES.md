# Release notes

## Information and documentation release 1.0.2 — August 6, 2026

- places free, fully automatic AI playlist generation with Google Antigravity CLI prominently in the public overview
- documents that no AI API key, usage-based API account, or manual copy-and-paste step is needed after setup
- explains installation on the application system, one-time Google sign-in, **Check CLI**, the real model selector, account-specific `agy models` entries, reasoning variants, and future custom model IDs
- describes the current free-tier access to high-quality Gemini models while clearly identifying model availability and quotas as Google-controlled services
- documents automatic transfer into the unchanged Roon matching, replacement, review, and playback-confirmation workflow
- records that the application never purchases credits and blocks existing paid G1/AI credits by default
- updates the documented application version to 1.0.463

## Information and documentation release 1.0.1 — August 4, 2026

- explain how the separate native macOS application SpotBridge 1.0.0 carries local Spotify playback to Roon Audio Input
- document AAC and losslessly encoded Ogg-FLAC bridge transport, forwarded metadata and artwork, and optional Spotify/Roon transport coordination
- clarify the boundary between SpotBridge audio capture and the Roon AI Playlist presentation and Wrapped features
- add a clear rights notice for the original documentation while excluding third-party trademarks, artwork, images, and other embedded material
- introduce English and German changelogs for public information releases

## Information and documentation release 1.0.0 — August 4, 2026

This is the first public information release for Roon AI Playlist. It contains no installer and no source code.

- English default landing page and complete German-language counterpart
- extensive overview of the ways Roon AI Playlist complements standard Roon
- complete English and German user guides
- field-by-field reference for all current configuration areas
- dedicated RoonAIViewer instructions
- getting-started, privacy, security, FAQ, and application-overview documents
- screenshots and explanations for multi-zone playback, AI and Last.fm playlists, Live Radio, Spotify, TIDAL mixes and playlists, audiobook discovery, Wrapped, network triggers, remote slots, and the RoPieee proxy
- explicit product boundary: the application complements Roon outside its GUI within the possibilities of the Roon Extension APIs and does not replace Roon

## Roon AI Playlist 1.0.463

The newly documented application capabilities include:

- fully automatic playlist generation through Google Antigravity CLI on the same Windows system
- API-key-free operation after a one-time Google account sign-in
- selectable Gemini 3.6 Flash, Gemini 3.5 Flash, and Gemini 3.1 Pro effort variants, plus account-reported and custom future models
- the proven Gemini 3.1 Pro (High) quality-oriented default
- CLI, authentication, quota, and model diagnostics through **Check CLI**
- automatic structured result transfer into the existing Roon search and replacement workflow
- protection against unintended use of already enabled paid Antigravity credits

The feature set documented for 1.0.458 below remains part of the current application:

### Earlier documented capabilities from 1.0.458

The documented feature set includes:

- more stable media processing during extensive cover and artist-image searches
- separate processing of media tasks so Player, the Roon connection, and network triggers remain responsive
- configurable artist-image provider order
- improved combined lookup for duos and artist groups
- Normal, Cautious, and Off live-radio modes, with identical searches in Normal and Cautious
- improved live-radio identification, character repair, and filtering of non-music content
- management of unresolved Wrapped covers with correction, retry, and removal actions
- a unified workflow for completing Wrapped albums and artwork
- SQLite as the primary Wrapped store with a portable backup snapshot
- automatic and manual backups with visible progress
- audiobook progress, bookmarks, and optional chapter-based capture
- network triggers with a manual OFF control and safe scheduler behaviour
- detailed status and maintenance information

## RoonAIViewer 1.0.3

- dedicated Windows client for a remote Roon AI Playlist installation
- connection test before settings are saved
- encrypted token storage for the current Windows user account
- persistent zoom from 90 to 130 percent
- optional Windows autostart and minimised notification-area launch
- full reload through the notification-area menu, `F5`, and `Ctrl+R`
- automatic recovery of a falsely displayed offline page after a successful server check
- clean uninstallation with optional removal of settings and browser profile
