# Release notes

## Information and documentation release 1.0.5 — August 21, 2026

- documents **Create AI playlist** for one exact historical recording under `Wrapped > Tracks`
- explains the AI-only profile for narrow genre/subgenre, actual sung language, style, instrumentation and sonic palette, era/production, vocal character, and energy
- documents the binding profile, independent audit by automatic providers, replacement of incompatible candidates, and the editable Roon-matched result
- explains automatic zone loading and live updates in an already open action menu during a Roon reconnect
- foregrounds the advantage over Roon Radio for controlled use: a visible exact seed, explicit constraints, finite preview, pre-playback review, editing, saving, and reproducibility
- clarifies that Roon Radio remains the convenient option for effortless continuous discovery and that Last.fm is not involved in this recording profile
- updates the documented application version to 1.0.549

## Information and documentation release 1.0.4 — August 16, 2026

- documents the direct TIDAL audiobook search by title or artist, broader series-aware matching, prepared covers and album metadata, up to 200 results, and sorting including oldest first
- explains **Add album**, **Listen later**, and **Fast capture** as distinct actions
- introduces the virtual TIDAL audiobook library with chapters, progress, automatic and named manual bookmarks
- documents direct playback through Roon Audio Input or a selected Windows/USB Bluetooth output
- covers independent speed from 1.00× to 2.00× and pitch from 0.50 to 1.50 in 0.05 steps, speech-oriented Rubber Band processing, and AVRCP Play/Pause
- states the client-dependent Roon live-input pause limitation and recommends application Play/Pause as the dependable control
- documents the fast-capture wizard, verified 4×/192 kHz and 2×/96 kHz profiles, full status page, chapter-boundary pause, abort, TIDAL playback lock, managed-Chrome cleanup, and continuous post-processing
- adds current search and playback screenshots in both English and German documentation paths
- updates the documented application version to 1.0.531

## Information and documentation release 1.0.3 — August 13, 2026

- documents the new installer choice between Complete application and Server + Configuration
- explains the intended always-on server arrangement with RoonAIViewer or a browser on another system
- describes that server mode does not keep the full local Player window loaded and opens Configuration locally only on demand
- confirms that the same configuration, Roon connection, SQLite data, caches, background workers, and backups are used in both modes
- confirms that Roon control, Wrapped, media processing, network triggers, remote slots, scheduled work, and audiobook capture continue in server mode
- explains how the desktop operating mode can be changed later and applied by restarting the application
- updates the documented application version to 1.0.466

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

## Roon AI Playlist 1.0.549

The newly documented application capabilities include:

- one shared `Wrapped > Tracks` action for direct Roon-zone playback or AI-playlist generation from the exact played recording
- AI-only classification of that recording across narrow genre, actual sung language, style, instrumentation, production era, vocal character, and energy
- a visible binding seed profile plus an independent per-suggestion audit for automatic providers
- the exact seed first once and a finite result that remains fully editable, replaceable, queueable, saveable, and playable
- immediate server-side zone refresh and live updates when an open action menu spans a Roon reconnect
- a controlled, inspectable alternative to Roon Radio's hands-off continuous recommendation stream

The capabilities documented for application 1.0.531 below remain part of the current application.

## Roon AI Playlist 1.0.531

The newly documented application capabilities include:

- direct TIDAL audiobook search by title or artist with broad matching, complete album preparation, improved artwork, and selectable sorting
- a separate virtual TIDAL library populated from TIDAL search, Audible/DNB hand-off, or capture candidate selection
- direct audiobook playback with chapter selection, progress, automatic and manual bookmarks, independent speed and pitch, and remembered output selection
- selectable Roon Audio Input or Windows/USB Bluetooth output, including AVRCP Play/Pause for compatible headsets on Windows output
- speech-oriented Rubber Band R3/Finer pitch processing with a complete bypass at pitch 1.00
- one managed TIDAL Chrome window with duplicate-tab monitoring and reconnection handling
- a guided fast-capture setup that verifies the companion, concrete virtual route, native PCM capture, real signal, and the usable accelerated profile
- a full production capture status page with elapsed and remaining time, chapter, destination, pause-at-boundary, resume, and genuine abort
- an exclusive TIDAL capture lock across direct audiobooks, mixes, playlists, and manual controls in the managed Chrome window
- fresh managed-Chrome lifecycle between capture jobs and continuous restoration before MP3 chapter splitting to protect chapter boundaries
- complete German/English localisation and contextual tooltips for the new TIDAL listening and capture controls

The previously documented 1.0.466 server-mode capabilities remain part of the current application.

## Roon AI Playlist 1.0.466

The newly documented application capabilities include:

- selectable Complete application or Server + Configuration operating mode in the Windows installer
- lower-overhead continuous operation without a permanently loaded local Player window
- local configuration opened on demand from the Windows notification area and released again after closing
- later operating-mode changes through Configuration with a controlled application restart
- unchanged remote browser and RoonAIViewer access to the complete interface
- unchanged server-side Roon, Wrapped, automation, media-worker, and audiobook-capture functions

The Antigravity capabilities documented for application 1.0.463 remain part of the current application:

- fully automatic playlist generation through Google Antigravity CLI on the same Windows system
- API-key-free operation after a one-time Google account sign-in
- selectable Gemini 3.6 Flash, Gemini 3.5 Flash, and Gemini 3.1 Pro effort variants, plus account-reported and custom future models
- the proven Gemini 3.1 Pro (High) quality-oriented default
- CLI, authentication, quota, and model diagnostics through **Check CLI**
- automatic structured result transfer into the existing Roon search and replacement workflow
- protection against unintended use of already enabled paid Antigravity credits

The feature set documented for 1.0.458 below also remains part of the current application:

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
