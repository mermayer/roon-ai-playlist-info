# Roon AI Playlist

**A local companion for Roon that adds intelligent playlist creation, richer live-radio metadata, visual multi-zone control, audiobook tools, personal listening statistics, artwork management, and home-automation actions.**

[Deutsche Version](README_DE.md)

> Roon AI Playlist is an independent project and is not affiliated with, endorsed by, or supported by Roon Labs, TIDAL, Last.fm, Deezer, fanart.tv, Audible, or any supported AI provider.

## Current versions

- Roon AI Playlist: **1.0.458**
- RoonAIViewer: **1.0.3**

## What is Roon AI Playlist?

Roon AI Playlist is designed for people who already use Roon and want more control over discovery, presentation, listening history, live radio, audiobooks, and connected devices.

Roon remains responsible for the music library, streaming, RAAT, DSP, zones, queues, and audio playback. Roon AI Playlist connects to that existing system and adds workflows that standard Roon does not provide on its own.

The application runs locally and can be operated in three ways:

- as a complete Windows application on the server computer,
- from a regular web browser on the private network,
- through the lightweight **RoonAIViewer** Windows client on another computer or display.

## What does it add to Roon?

### Intelligent playlist creation

- Describe a desired playlist in natural language.
- Choose Ollama, OpenRouter, OpenAI, Gemini, or Claude as the AI provider.
- Combine the request with genre, decade, mood, energy, and language filters.
- Build playlists from Last.fm, Deezer, maintained tag collections, or Wrapped favourites.
- Match every suggestion against the actual Roon library before playback.
- See successful matches, uncertain results, missing tracks, and possible replacements.
- Play the result in a chosen Roon zone or save it as an M3U playlist.

### Better live radio metadata

Live-radio streams often provide incomplete, swapped, or incorrectly encoded text. Roon AI Playlist can:

- distinguish station name, artist, track, and album,
- repair common character-encoding problems involving umlauts and apostrophes,
- resolve missing albums and artwork through several metadata providers,
- replace incorrect artist or title information when a reliable match is found,
- distinguish a station logo from real track artwork,
- retrieve artist portraits and wide fan-art backgrounds,
- filter jingles, adverts, news, intros, outros, station IDs, and automation labels,
- save identified tracks to a configured TIDAL playlist with `T+`.

Every station has its own persistent metadata policy:

- **Normal:** enrich the presentation and record the music in Wrapped.
- **Cautious:** use the same search and presentation, but record only when a usable provider result exists.
- **Off:** display only the station information and do not add the item to Wrapped.

![Enriched live-radio metadata with cover and artist images](assets/screenshots/radio_new.png)

### A more visual multi-zone player

- Show all relevant Roon zones in one dashboard.
- Display artwork, playback state, progress, transport controls, and queue information.
- Show upcoming tracks, remaining track count, and total remaining time.
- Use dedicated views for normal music, Roon Radio, live radio, Spotify streams, and audiobooks.
- Present album cover, artist portrait, and artist background separately.
- Keep browser and viewer displays stable during short Roon reconnects.
- Add the current track directly to a per-zone TIDAL target playlist.

![Zone detail with queue and artist artwork](assets/screenshots/player.png)

### Audiobooks inside the Roon environment

- Synchronise Roon albums identified as audiobooks.
- Analyse books containing hundreds of chapters.
- Display chapter count, total duration, current position, and remaining time.
- Resume a book, restart it, or select a chapter directly.
- Store manual and automatic bookmarks independently of the playback zone.
- Keep recognised audiobooks and authors out of music Wrapped and artist-image searches.
- Optionally enrich audiobook metadata and artwork.
- Optionally capture an audiobook through a dedicated local Roon zone and create numbered MP3 chapter files with embedded metadata and cover art.

![Audiobook player with chapters and bookmarks](assets/screenshots/audiobooks.png)

### Personal Roon Wrapped

- Record qualified listening sessions from normal Roon playback, live radio, and Spotify streams locally.
- Analyse listening time, sources, time of day, top tracks, top artists, and top albums.
- Distinguish short false starts, skips, and replays.
- Explore Dashboard, Show, cover mosaic, and autoplay Story views.
- Select year, quarter, month, rolling 30/90 days, all time, or a custom date range.
- Start historical tracks directly in a selected Roon zone.
- Export results as PNG, PDF, or CSV.
- Inspect data quality and repair missing albums or covers.

![Personal Roon Wrapped show](assets/screenshots/wrapped.png)

### Artwork and artist-image management

- Choose and reorder fanart.tv, TIDAL, Roon, Last.fm, Deezer, and TheAudioDB for artist-image searches.
- Disable individual image providers.
- Search combined artist names and duos before falling back to individual performers.
- Manage portraits and wide artist backgrounds separately.
- Pin a preferred image, reject an unsuitable result for one artist, or upload a custom image.
- Store retrieved images locally and avoid duplicate files.
- Find unresolved Wrapped covers, correct artist/title/album information, and retry only the affected entry.
- Complete missing Wrapped albums, covers, and local image copies through one guided workflow.

### Direct TIDAL tools

- Search TIDAL directly for artists, tracks, and albums.
- Import suitable TIDAL mixes with custom exclusion rules.
- Configure a dedicated TIDAL target playlist for each Roon zone.
- Add the currently playing track or an identified live-radio track through `T+`.
- Keep mix search text and filters in the local application profile.

### Remote actions and external devices

- Configure up to ten shortcuts for live-radio stations, Roon playlists, and zone actions.
- Define multiple independent network triggers for one or more Roon zones.
- Send separate HTTP or HTTPS commands when playback starts and after playback stops.
- Control amplifiers, smart plugs, IR bridges, or home-automation devices.
- Schedule switch-off after pause or stop and cancel it automatically when playback resumes.
- Use a manual OFF control to stop the zone, cancel its scheduler, and switch assigned devices off immediately.
- Optionally use a dedicated Roon dummy zone as a Bluetooth remote-control proxy for play, pause, next, and previous.

### Maintenance and reliability

- Create and restore complete application backups.
- Store Wrapped sessions primarily in SQLite while retaining a portable backup snapshot.
- Move the artwork cache to another local drive with verification.
- Inspect service status, storage, caches, provider errors, and Roon connectivity.
- Run extensive metadata requests, image downloads, validation, hashing, and cache work separately so the player, web interface, Roon connection, and network triggers remain responsive.

## Playlist example

![AI-assisted playlist matched against Roon](assets/screenshots/playlist.png)

## RoonAIViewer

RoonAIViewer is a dedicated 64-bit Windows client for a Roon AI Playlist installation running on another computer. It provides the complete interface in its own window without starting another application service or creating another Roon connection.

Viewer features include:

- Windows notification-area operation,
- optional autostart and minimised startup,
- persistent interface zoom from 90 to 130 percent,
- native server and token connection test,
- API-token protection through Windows DPAPI for the current user,
- full reload through the tray menu, `F5`, or `Ctrl+R`,
- automatic recovery when the web page reports an incorrect offline state,
- optional removal of settings and browser data during uninstallation.

See the [complete RoonAIViewer user guide](docs/ROONAI_VIEWER.md).

## Requirements

For normal Windows use:

- 64-bit Windows 10 or Windows 11,
- a reachable Roon Core on the local network,
- authorisation of the extension under **Roon > Settings > Extensions**.

AI playlist generation is optional and can be disabled. Optional integrations include TIDAL, Last.fm, Deezer, fanart.tv, MusicBrainz/Cover Art Archive, TheAudioDB, Audible, and a supported AI provider.

## Local data and network access

The application is intended for a trusted private network. Listening history, audiobook information, configuration, logs, and cached images are stored on the application system. External requests occur only for enabled services and features.

Browser and RoonAIViewer access should be protected with an API token. Application backups may contain credentials and personal listening history and should be stored securely.

## Documentation

- [Complete user guide](docs/USER_GUIDE.md)
- [Features beyond standard Roon](docs/FEATURES_BEYOND_ROON.md)
- [Application overview](docs/APP_OVERVIEW.md)
- [Getting started](docs/GETTING_STARTED.md)
- [RoonAIViewer user guide](docs/ROONAI_VIEWER.md)
- [Privacy and security](docs/PRIVACY_AND_SECURITY.md)
- [Frequently asked questions](docs/FAQ.md)
- [Release notes](docs/RELEASE_NOTES.md)
- [Deutsche Dokumentation](README_DE.md)

## Availability

This information repository contains no installer and no source code. Distribution of Roon AI Playlist and RoonAIViewer is handled separately.
