# Roon AI Playlist user guide

[Deutsche Version](BENUTZERHANDBUCH_DE.md) · [Back to overview](../README.md)

Documentation status: Roon AI Playlist **1.0.463**, RoonAIViewer **1.0.3**.

## Contents

1. [Purpose of the application](#1-purpose-of-the-application)
2. [Requirements](#2-requirements)
3. [Installation and first launch](#3-installation-and-first-launch)
4. [Navigation and interfaces](#4-navigation-and-interfaces)
5. [Player and zones](#5-player-and-zones)
6. [Creating playlists](#6-creating-playlists)
7. [Live radio](#7-live-radio)
8. [TIDAL tools](#8-tidal-tools)
9. [Audiobooks](#9-audiobooks)
10. [Roon Wrapped](#10-roon-wrapped)
11. [Artwork and artist images](#11-artwork-and-artist-images)
12. [Roon Tools](#12-roon-tools)
13. [Remote slots](#13-remote-slots)
14. [Network triggers](#14-network-triggers)
15. [Remote-control proxy](#15-remote-control-proxy)
16. [Browser and RoonAIViewer](#16-browser-and-roonaiviewer)
17. [Configuration](#17-configuration)
18. [Backup and restore](#18-backup-and-restore)
19. [Storage and maintenance](#19-storage-and-maintenance)
20. [Security and privacy](#20-security-and-privacy)
21. [Troubleshooting](#21-troubleshooting)
22. [Recommended setup sequence](#22-recommended-setup-sequence)

## 1. Purpose of the application

Roon AI Playlist extends an existing Roon system. It is not a replacement for the Roon GUI or Roon's own functions. Roon remains responsible for the music library, streaming, RAAT, DSP, zones, queues, and audio playback. The application exists to make additional workflows available outside Roon where Roon does not provide them, within the possibilities and limits of the Roon Extension APIs:

- intelligent and external playlist generation,
- visual multi-zone control,
- improved live-radio metadata and imagery,
- audiobook progress and bookmarks,
- personal Wrapped statistics,
- cover and artist-image maintenance,
- TIDAL quick actions,
- remote slots and network triggers,
- browser and viewer access.

The application does not replace the Roon library and does not modify audio processing. Playback actions are passed to Roon.

## 2. Requirements

Normal operation requires:

- 64-bit Windows 10 or Windows 11,
- a running Roon Core reachable on the local network,
- permission to authorise the application under **Roon > Settings > Extensions**,
- a Roon zone for playback.

Optional services include:

- Google Antigravity CLI for fully automatic AI playlists without an API key; the free Google tier can be used after a one-time account sign-in,
- Ollama, OpenRouter, OpenAI, Gemini, Claude, or guided ChatGPT Work as alternative AI routes,
- TIDAL for direct search and playlist actions,
- Last.fm and Deezer for music lookup and metadata,
- fanart.tv and TheAudioDB for artist images,
- MusicBrainz and Cover Art Archive for album information and artwork,
- Audible for audiobook information.

Services that are not needed can remain disabled. Player, Roon Tools, audiobooks, and large parts of Wrapped remain available without an AI provider.

## 3. Installation and first launch

### Installation

1. Open the separately supplied Windows installer.
2. Complete installation and start Roon AI Playlist.
3. Follow the setup assistant on first launch.

### Authorising Roon

1. Wait until the application discovers the Roon Core on the network.
2. Open **Roon > Settings > Extensions**.
3. Authorise **AI Playlist Generator**.
4. Authorise **Roon AI Hoerbuchaufnahme** as well only when audiobook capture will be used.

The normal Roon connection does not require a manually created Roon API key.

### Setup assistant

The assistant guides the user through:

1. restoring an existing application backup or starting fresh,
2. establishing the Roon connection,
3. selecting local-only or LAN access,
4. choosing language and basic interface settings,
5. enabling or skipping AI and optional services,
6. testing credentials,
7. saving the configuration.

The assistant can be opened again later through **Configuration > Setup assistant**.

### Checks after first launch

- Is the Roon Core shown as connected?
- Do the desired zones appear in Player?
- Does a zone respond to play and pause?
- Are artwork and queue information displayed?
- Is an API token configured for LAN access?
- Has an initial backup been created?

## 4. Navigation and interfaces

The main navigation contains:

- **Player:** zone overview, playback, and detail views.
- **Playlist:** AI, Last.fm, tag, and Wrapped playlists.
- **Audiobooks:** library, analysis, progress, chapters, and bookmarks.
- **Wrapped:** personal listening statistics, Show, Story, and data quality.
- **Roon Tools:** live-radio stations, Roon playlists, queue, and quick actions.
- **Configuration:** services, interface, Wrapped, remote control, maintenance, and backups.

### Complete Windows application

The complete application contains both the user interface and the central application service. Closing the window can leave the application running in the Windows notification area. Its tray menu opens the application or browser, starts or stops the service, reloads it, or exits completely.

### Browser view

The browser view is suitable for tablets, wall displays, and other computers on the private network. It uses the same state as the regular Player while removing unnecessary window elements from the zone presentation.

### RoonAIViewer

RoonAIViewer is a separate Windows client for a remote application service. It is summarised in [section 16](#16-browser-and-roonaiviewer) and has its own [detailed user guide](ROONAI_VIEWER.md).

## 5. Player and zones

![Multi-zone Player overview](../assets/screenshots/new_zone_view.png)

### Zone overview

The zone overview is configurable under **Configuration > UI**. The normal Player view and the large Browser view have separate selections: choose which discovered Roon zones are visible, arrange their order, and select an automatic, one-column, or two-column layout. Hiding a zone only removes it from that view; it does not disable or rename the zone in Roon.

Each zone card can display:

- zone name,
- state such as Playing, Paused, Stopped, or Loading,
- track, artist, and album,
- album artwork or an appropriate fallback image,
- progress and duration,
- upcoming tracks,
- remaining track count and time,
- transport controls.

The application reuses its existing Roon zone monitoring. Additional browsers and viewers do not create independent Roon connections.

### Zone detail view

![Zone detail with queue and artist artwork](../assets/screenshots/player.png)

Opening a zone shows a larger presentation. Depending on the content, it displays:

- large album or track artwork,
- artist portrait and artist background,
- current metadata,
- progress bar,
- queue,
- playback controls,
- optional TIDAL and network actions.

In normal queue mode, the current and upcoming tracks are central. Roon Radio gives more room to the artist presentation until Roon reports a regular follow-up queue.

### Controls

Depending on the content, controls can include:

- back or previous track,
- play and pause,
- next track,
- ten-second backward or forward seek where meaningful,
- `T+` to save to the zone-specific TIDAL target playlist,
- **OFF** for zones with a configured network trigger.

Seek buttons are hidden in music-only presentations where they serve no useful purpose. Live radio also receives an appropriate reduced control set.

### Queue and remaining time

The application shows an upcoming-track preview, track durations, and the total remaining count and time. Briefly delayed queue details are recovered in a controlled way without continuous additional requests.

### Images and source labels

Small letters on an image can identify its source, such as Roon or fanart.tv. Album artwork, artist portrait, and wide background are handled separately so the same image does not have to fill every surface.

For groups and duos, the complete combined artist name is searched first. Individual participants are considered only when no suitable result exists for the combined identity.

### Roon Radio, Spotify, and audiobooks

- **Roon Radio:** receives an adapted presentation until a regular queue is available.
- **Spotify or external streams:** supplied metadata and artwork are preferred; unsuitable duration or seek elements are hidden.
- **Audiobooks:** chapters, position, bookmarks, and resume controls take priority.

![Spotify playback presented in a dedicated zone view](../assets/screenshots/spotify_pl.png)

The Spotify layout is a presentation for playback that arrives through Roon, not a separate Spotify client. The application does not browse a Spotify account or take over Spotify playback. When the stream provides usable artist, title, album, and artwork information, the player separates the album cover from artist portrait and background. Qualified listening sessions are labelled as Spotify in Wrapped so they can be inspected and filtered independently.

#### Supplying Spotify to Roon with SpotBridge

SpotBridge 1.0.0 is a separate native macOS menu-bar application. It provides the connection that is deliberately outside Roon AI Playlist:

`Spotify on macOS → CoreAudio Process Tap → SpotBridge → Roon Audio Input → selected Roon zone → Roon AI Playlist display and Wrapped`

SpotBridge captures audio from the local Spotify process through a CoreAudio Process Tap. It can deliver the captured signal to Roon Audio Input as AAC or as losslessly encoded Ogg-FLAC. Ogg-FLAC avoids an additional lossy encoding step between the bridge and Roon, but it cannot restore information that was not present in the original Spotify stream.

Alongside audio, SpotBridge forwards artist, title, album, and artwork. It can also coordinate Spotify and Roon transport events automatically, so changes on either side can be reflected in the combined workflow. The selected Roon zone then exposes the playback through Roon in the usual way.

Roon AI Playlist consumes the playback only after it reaches Roon. It provides the dedicated zone presentation, image handling, controls made possible by the available Roon data, and qualified Wrapped recording. No Spotify login or Spotify audio-capture configuration is required inside Roon AI Playlist. SpotBridge and Roon AI Playlist remain two independent companion applications with clearly separated responsibilities.

## 6. Creating playlists

![AI-assisted playlist matched against Roon](../assets/screenshots/playlist.png)

### Available sources

- **AI playlist:** a free-form request with additional filters.
- **Last.fm:** suggestions based on tags and moods.
- **Tag lists:** maintained categories for several playlist sources.
- **Wrapped Top 20:** personal favourites from the local Wrapped history.

### Creating an AI playlist

1. Open **Playlist**.
2. Select AI playlist as the source.
3. Describe the desired music, occasion, or mixture.
4. Optionally restrict decade, genre, mood, energy, and language.
5. Select the target zone and desired track count.
6. Generate the playlist.

The description may be left empty when the structured filters already express the request. Mood and energy, decade, genre, and artist language are combined with the current provider and model. The footer identifies which model generated the result and which Roon-matching strategy was applied.

The result is an editable working list rather than an opaque one-click action. Individual candidates can be auditioned, queued, replaced, or removed before the complete result is sent to Roon. Provider badges, year, and energy labels make it easier to spot an unsuitable edition or an outlier.

### Using Google Antigravity without an API key

Antigravity is the most direct API-key-free AI route. Unlike the guided ChatGPT Work method, it requires no copying between applications after setup:

1. Install the official Google Antigravity CLI on the same Windows system that runs Roon AI Playlist. Google's Windows installer can be started in PowerShell with `irm https://antigravity.google/cli/install.ps1 | iex`.
2. Open **Configuration > AI**, enable AI generation, and select **Antigravity** as `ai.mode`.
3. Leave the executable as `agy.exe` when the CLI is in Windows PATH; otherwise enter its full path.
4. Select **Open sign-in**. A visible terminal opens on the app system. Complete the Google sign-in and first-run setup once, then close the terminal. On a system without an interactive desktop session, open PowerShell there manually and run `agy`.
5. Select **Check CLI**. This verifies the program and authentication, reports the paid-credit safeguard, and adds models returned by `agy models` to the selector.
6. Select a model and, if required, its reasoning effort. **Gemini 3.1 Pro (High)** is the proven quality-oriented default; Gemini 3.5/3.6 Flash variants offer useful alternatives. **Automatic** uses the Antigravity account default, while **Custom** accepts future model IDs.
7. Save the configuration and create the playlist normally. The application runs the CLI in the background, imports its JSON track list, and then performs the same Roon matching, replacement, review, and playback confirmation used by every other generator.

No separate AI API key or usage-based API account is required. Google's free Individual/Standard tier currently exposes modern Gemini models and other selectable models, but availability and quotas are controlled by Google and can change. The application never buys credits. If paid G1/AI credits have already been enabled globally in Antigravity, Roon AI Playlist blocks generation until **Explicitly allow existing paid Antigravity credits** is selected. Current information is available on Google's [model](https://antigravity.google/docs/models) and [pricing](https://antigravity.google/pricing) pages.

### Creating a Last.fm tag playlist

![Last.fm tags and the resulting Roon-matched playlist](../assets/screenshots/lastfm.png)

1. Select **Last.fm playlist** as the source.
2. Choose one or more decade/year, language, genre, style, or atmosphere tags.
3. Select the Roon zone and number of tracks.
4. Choose **Load Last.fm top tracks**.

Last.fm supplies popular candidates for the combined tags; the application then performs the normal Roon match. The result heading preserves the selected tags, while the footer separates found and missing candidates. **Reset all** clears the selection, and a previously saved playlist can be loaded without repeating the Last.fm request.

### Understanding Roon matching

Suggestions are not played blindly. The application searches every candidate in the actual Roon library and displays:

- confidently matched tracks,
- uncertain or alternative results,
- missing candidates,
- possible replacement tracks.

Only then can the list be played, queued, or saved. External identifiers are not treated as Roon library objects without matching.

### Using the result

Depending on the view, actions include:

- play immediately in the selected zone,
- append to the existing queue,
- shuffle the order,
- save as M3U,
- load a stored list and validate it again.

### Managing tag lists

Categories used by Last.fm, AI, and Deezer-based sources can be edited and checked under **Configuration > Services**. Validate changes before saving them. These maintained tags determine the selectable chips in the Playlist view, so installations can adapt the vocabulary without changing the application.

## 7. Live radio

![Enriched live-radio metadata with cover and artist images](../assets/screenshots/radio_new.png)

### Why enrichment is needed

Roon receives live-radio metadata from the stream. Some stations provide complete fields, while others send only one line, swapped names, damaged characters, or advertising text. The application attempts to turn this into reliable music metadata.

### Lookup and display chain

Depending on available information, the application uses:

1. explicit Roon album information,
2. TIDAL and previously stored reliable matches,
3. MusicBrainz and Cover Art Archive,
4. Last.fm,
5. Deezer as a further fallback.

Artist, title, and album can be corrected when a reliable match exists. Unsuitable compilation, best-of, soundtrack, live, or remaster candidates are downgraded when they conflict with the supplied hints.

### Non-music content

Typical jingles, adverts, news, weather, intros, outros, station IDs, and technical automation labels are rejected before provider lookup whenever possible. This reduces false artwork and unwanted Wrapped entries.

### Character repair

Broken umlauts, apostrophes, and similar characters are normalised before lookup. The visible display uses the repaired spelling whenever possible.

### Metadata modes per station

The mode is stored for each station under **Roon Tools**:

- **Normal (`N`):** full lookup and presentation; qualified music is recorded in Wrapped.
- **Cautious (`V`):** exactly the same lookup, display, artwork, artist images, and `T+` behaviour as Normal. Only Wrapped differs: without a usable provider result, the item is not recorded.
- **Off (`A`):** no external lookup and no Wrapped entry; the station or Roon values are displayed unchanged.

The mode symbol appears beside the station name in zone cards and detail views.

### `T+` for live radio

In Normal and Cautious mode, an identified track can be added to the TIDAL target playlist configured for that zone. External actions are unavailable in Off mode.

### Handling an incorrect result

- Wait for the next title update to exclude a stale intermediate state.
- Check the station's metadata mode.
- Inspect the error log for a provider or encoding problem.
- If the item was stored in Wrapped, correct it through **Manage missing covers**.

## 8. TIDAL tools

After a successful TIDAL connection, the application can:

- search tracks, albums, and artists,
- resolve relationships between track, album, and performer,
- import TIDAL mixes,
- retain exclusion filters for mixes,
- assign a TIDAL target playlist to each Roon zone,
- add current or identified radio tracks through `T+`.

### Personal mixes and radio

![Personal TIDAL mixes, discoveries, track radio, and artist radio](../assets/screenshots/personal_radio.png)

The **Mixes** view reads the recommendations available to the connected TIDAL account and presents them in one place. Depending on the account, this can include My Daily Discovery, numbered My Mixes, My New Arrivals, custom mixes, track radio, and artist radio. Every entry shows its type and a short description or seed artists.

The toolbar provides:

- a Roon target zone,
- a text filter for the visible mixes,
- tile and list presentation,
- selection of all currently visible entries,
- optional exclusion of videos, artist radio, or track radio,
- manual refresh and synchronisation,
- an optional daily synchronisation time and history of the last run.

**Start mix** replaces playback in the chosen Roon zone. **Append mix** adds the result to the existing queue. Selecting entries and choosing **Save selection** turns those dynamic recommendations into regular TIDAL playlists; a later synchronisation updates the saved copies instead of creating uncontrolled duplicates.

### TIDAL playlists

![Search, preview, start, or append TIDAL playlists](../assets/screenshots/tidal_pl.png)

The **Playlists** view searches editorial TIDAL playlists and playlists belonging to the connected account. Search terms can be combined with decade, genre, mood, and topic chips. The source filter supports all results, TIDAL-only, or user-only lists. Cards identify the source and track count. Before playback, a preview can expose the first tracks, which is useful for broad names such as “Party” or “Classics”.

Choose the Roon zone before using **Start PL** or **Append PL**. Starting replaces the current queue; appending preserves it. This workflow controls Roon playback—the TIDAL item is still resolved into something Roon can play, and a TIDAL object is not treated as a Roon library object without that handover.

### Configuring a target playlist

1. Enable and connect TIDAL under **Configuration > Services**.
2. Load the available playlists.
3. Select a target playlist for the desired Roon zone.
4. Save the settings.

The `T+` button appears only where a meaningful TIDAL action is available.

### Error states

- An empty result is not necessarily a connection error.
- Reconnect when authentication has expired.
- Check connection and service status for provider failures.
- A TIDAL result is not automatically the same object in the Roon library, so the application keeps the matching processes separate.

## 9. Audiobooks

![Audiobook player with chapters and bookmarks](../assets/screenshots/audiobooks.png)

### Catalogue search with Audible and DNB

![Filterable Audible and DNB audiobook catalogue](../assets/screenshots/audible.png)

The **Audiobook search** tab is for discovery before a title is part of the local audiobook library. Its catalogue source can be switched between current Audible.de releases and the German National Library catalogue. Title, author, keyword, genre, publication years, and sort order narrow the result. Depending on the source, cards show author, narrator, series, duration, year, genres, rating, and an audio sample.

**Details** opens the available catalogue information. **Audible.de** opens the source page. **TIDAL** transfers the selected title and author to the separate album search described next; it does not assume that every catalogue result is available on TIDAL.

### Finding the audiobook on TIDAL

![Verified TIDAL album candidates for an audiobook](../assets/screenshots/tidal_search.png)

The TIDAL dialog searches album candidates and then resolves their artist relationship separately. Only albums whose TIDAL artist fits the searched author are retained. Every candidate shows artwork, artist, year, duration, and track count so editions and volumes can be distinguished before **Add to my albums** is used. No result is a valid availability outcome and is presented differently from authentication, timeout, or provider errors.

Adding a result creates the application's audiobook record; it does not purchase content and does not import audio files. Playback availability remains governed by TIDAL and Roon.

### Synchronising the library

1. Open **Audiobooks**.
2. Select **Synchronise audiobooks**.
3. Wait until all corresponding Roon albums have loaded.
4. Run **Analyse audiobooks** to obtain complete chapters and duration.

The analysis uses full pagination and is designed for books with hundreds of chapters.

### Library view

Available functions include:

- list and tile views,
- sorting by title, author, progress, or update time,
- cover, author, chapter count, and total duration,
- current position and remaining time,
- resume and restart.

### Audiobook player

The detail view includes:

- large cover,
- title and author,
- playback zone,
- current position,
- chapter list,
- chapter numbers and durations,
- automatic and manual bookmarks,
- transport and seek controls.

### Progress and bookmarks

Progress belongs to the audiobook rather than one particular zone. When a known book is played in a monitored Roon zone, the same book record can be updated.

- **Automatic bookmark:** follows active playback.
- **Manual bookmark:** preserves a deliberately saved position and can be deleted.
- **Resume:** starts at the stored position.
- **Start from beginning:** restarts the book.

Recognised audiobooks are not recorded as ordinary music in Wrapped and do not launch overnight music artist-image searches.

### Optional audiobook capture

Capture is intended for audiobooks that have already been synchronised and analysed.

Before the first capture:

1. choose the destination and exclusive capture zone under **Configuration > Basic > Audiobook capture**,
2. run **Check system**,
3. satisfy all reported requirements,
4. authorise the additional **Roon AI Hoerbuchaufnahme** Roon extension.

The system check validates audio tools, input device, Roon zone, write access, and free storage.

During capture:

- the configured zone is reserved exclusively,
- continuous master segments are recorded first,
- observed chapter transitions are tracked,
- **Pause after this chapter** can be queued and cancelled,
- resuming begins the next chapter in a new segment.

After capture, numbered MP3 chapters are created with title, author, album, track number, and embedded artwork. Existing master segments remain available as rescue files after a real failure.

## 10. Roon Wrapped

![Personal Roon Wrapped show](../assets/screenshots/wrapped.png)

### What is recorded?

Wrapped stores qualified local listening sessions from:

- regular Roon music playback,
- live radio using an appropriate station mode,
- identified Spotify or external music streams.

Short false starts are excluded from listening time and top lists but may remain relevant for skip and quality metrics. Audiobooks and filtered non-music content are excluded.

### Views

- **Dashboard:** core figures, top lists, time of day, sources, and recent sessions.
- **Show:** compact visual summary with cover mosaic and highlights.
- **Story:** sequential chapter cards with navigation and autoplay.
- **Status:** tracking period, data quality, cover coverage, and missing data.
- **Listening history:** filterable list of historical playback.

### Track-level listening history

![Wrapped Tracks with date and source filters](../assets/screenshots/tracks.png)

The **Tracks** view exposes the individual plays behind the summary values. Each row includes cover, title, artist, album, timestamp, source, station when applicable, and counted listening time. The period selector can show a day or a broader Wrapped range; the source selector can isolate normal Roon playback, Live Radio, or Spotify.

Selecting a row opens a zone chooser. The application searches the historical title in Roon and sends the resolved result to the selected zone. This view also helps locate entries whose artist, album, or cover needs repair, because the original source and listening time remain visible.

### Date ranges

- current year,
- current quarter,
- current month,
- rolling 30 days,
- rolling 90 days,
- all time,
- custom range.

### Playing a historical track

Selecting a track or top-track entry opens a zone chooser. The application searches Roon and starts playback in the selected zone. If Roon supplies better metadata, missing album or artwork information can be completed.

### Exports

Depending on the interface, exports include:

- PNG card,
- PDF report,
- CSV data.

PDF is intended for the complete Windows application. Browser and viewer users primarily use PNG, CSV, and the on-screen views.

### Completing Wrapped data

Under **Configuration > Wrapped > Data management**, **Complete Wrapped data** runs three stages:

1. resolve missing albums,
2. find missing covers,
3. store external images locally.

All open groups are processed until no further progress is possible. **Complete automatically** starts the same workflow immediately and checks for new gaps every five minutes. **Stop run** ends the active job.

### Managing missing covers

Under **Advanced actions > Manage missing covers**, unresolved tracks are grouped. For each group, the user can:

- correct artist, title, and album,
- save the corrected values and search again immediately,
- retry without changing metadata,
- delete the affected Wrapped plays after confirmation.

Before deletion, the application displays the exact number of affected plays. A second check prevents accidental deletion if the group changed in the meantime.

## 11. Artwork and artist images

### Provider order

Under **Configuration > Wrapped > Manage artist images**, the following providers can be reordered or disabled:

- fanart.tv,
- TIDAL,
- Roon,
- Last.fm,
- Deezer,
- TheAudioDB.

The first usable result in the selected order wins. Manually pinned images retain priority.

### Image actions

- inspect available local results,
- pin an image for one artist,
- reject an unsuitable result only for that artist,
- allow a rejected result again,
- launch a targeted external refresh,
- provide a custom JPEG, PNG, or WebP image.

### Portrait and background

The application distinguishes normal artist images from wide backgrounds. A live-radio view can therefore show a portrait above and separate fan-art banner below. If no background is available, a normal artist image can be used as a fallback.

### Multiple artists

Duos, bands, and combined credits are searched as one identity first. Individual performers are considered only when the complete identity has no usable image. A split presentation is used only when the individual results form a meaningful complete set.

## 12. Roon Tools

Roon Tools combines quick Roon actions:

- load and start live-radio stations,
- select the metadata mode for each station,
- load and start Roon playlists,
- select the playback zone,
- choose playlist sorting,
- inspect the selected zone's queue,
- trigger configured remote slots.

The queue card in Roon Tools is a compact queue view and is not identical to the full zone detail view.

### Playlist sorting

Roon playlists can be sorted alphabetically, by track count, or in the order visible in Roon. The most recent selection is retained.

## 13. Remote slots

![Configuration of ten IR and WLAN remote slots](../assets/screenshots/remote_v2.png)

Up to ten quick actions can be created under **Configuration > Remote**. A slot has:

- a number,
- visible label,
- target zone,
- action.

Possible actions include:

- starting a live-radio station,
- starting a Roon playlist,
- starting or toggling playback in a zone.

Each slot can be tested from Configuration. Active slots appear in the intended interface locations and can also be triggered by compatible local remote-control solutions.

The **Toggle** setting is useful when one hardware button should alternate an action such as play and pause. **Load targets** retrieves the stations or playlists appropriate for the selected action from Roon. The visible label is independent of the Roon target name, so a short hardware-friendly name can be used without renaming the zone or playlist in Roon. Disabled slots keep their configuration but do not react.

Compatible ESP32, IR/WLAN, or home-automation controllers can call a protected local endpoint for a numbered slot. The API token and local-network security remain the responsibility of the installation; these endpoints should not be exposed directly to the internet.

## 14. Network triggers

Network triggers connect Roon playback state to external devices.

![Two independent network triggers with live state and countdown](../assets/screenshots/remote_trigger_2.png)

### Typical uses

- switch on an amplifier when playback starts,
- switch off active speakers or smart plugs after a delay,
- control an IR or home-automation bridge,
- manage several devices assigned to one zone.

### Creating a trigger

1. Open **Configuration > Remote > Network triggers**.
2. Add a trigger and give it a clear name.
3. Assign one or more Roon zones.
4. Enter an ON and/or OFF address; at least one direction is required.
5. Choose a switch-off delay when an OFF command exists.
6. Validate the configuration.
7. Test ON and OFF separately.
8. Save the settings and observe the status.

### Supported variants

- **ON and OFF:** complete automatic control.
- **ON only:** switch on at playback start; no switch-off timer.
- **OFF only:** arm the next pause or stop when playback starts without sending an ON command.

### Scheduler behaviour

- When at least one assigned zone starts or loads, a pending OFF action is cancelled and ON is sent when configured.
- When all assigned zones are paused or stopped, the switch-off delay starts.
- Resuming playback cancels the timer.
- If an assigned zone is missing or its state is uncertain, OFF is withheld for safety.
- At expiry, OFF is sent once when every zone remains inactive.

### Manual OFF control

Zones with an active trigger and OFF command receive a manual OFF control in every zone view. It:

1. stops the Roon zone,
2. cancels associated switch-off timers,
3. immediately sends the OFF commands of the assigned triggers.

For a shared trigger, the interface warns when another assigned zone remains active. The manual action must not block the next genuine playback start.

The status panel is intended for more than setup: it reports the aggregated zone state, current trigger output, remaining timer, latest command result, and response latency. This makes a real automatic transition distinguishable from a successful isolated test. Multiple triggers are processed independently, so one failing HTTP endpoint does not redefine another trigger's state.

## 15. Remote-control proxy

![RoPieee dummy-zone proxy configuration and live status](../assets/screenshots/ropieee_remote.png)

The optional dummy-zone proxy can forward play, pause, next, and previous from a Bluetooth or similar remote to the most recently active music or audiobook zone.

It requires:

- a dedicated Roon dummy zone,
- a selected music zone,
- a selected audiobook zone,
- the supplied long marker tracks in the specified order.

The application distinguishes intentional marker movement from natural track completion and feedback. Target zone, marker, last command, and acknowledgement time are shown in Configuration. Volume and mute are not forwarded.

Validate the configuration and synchronise the dummy zone before use.

### RoPieee workflow

RoPieee is configured to control only the dedicated dummy zone. No custom component is installed on RoPieee. The dummy output should be silent and its queue contains the supplied long tracks **Remote Marker A**, **Remote Marker B**, and **Remote Marker C** in that order. The application enables repeat and disables shuffle and Roon Radio for this queue.

- A play or pause change on the dummy zone is forwarded as play or pause.
- A deliberate marker movement is interpreted as next or previous.
- Natural marker completion and changes generated by the application itself are suppressed so they do not create control loops.
- The most recently active configured music or audiobook zone becomes the destination; a default applies before any activity, and the last destination can optionally survive a restart.

The live panel shows readiness, active destination, dummy-zone state, last forwarded command, marker validation, and confirmation time. **Synchronise dummy** restores the expected queue and state after configuration changes. Volume and mute are intentionally outside the implemented proxy.

## 16. Browser and RoonAIViewer

### Browser access

To use another device:

1. enable LAN access in the application,
2. configure an API token,
3. allow the selected port through the server computer's firewall,
4. open the server address and port in a browser.

Access is intended for a trusted private network and should not be exposed directly to the internet.

### RoonAIViewer

RoonAIViewer displays the same interface in a dedicated Windows window. It:

- starts no application service of its own,
- creates no direct Roon connection,
- supports notification-area operation and autostart,
- stores a zoom from 90 to 130 percent,
- checks the server address and token natively,
- protects the token with Windows DPAPI,
- can automatically reload a falsely reported offline page.

Complete setup, operation, troubleshooting, and uninstallation are covered in the [RoonAIViewer guide](ROONAI_VIEWER.md).

## 17. Configuration

Configuration is divided into **Basic**, **UI**, **AI**, **Services**, **Wrapped**, **Remote**, **Maintenance**, and **Save & Logs**. Status cards above the tabs report whether the application package, Roon, selected AI provider, optional services, and data stores are ready. Grey commonly means intentionally disabled or not selected; it does not automatically indicate a fault.

Most server settings are applied only with **Save changes**. Client connection, TIDAL authorisation, individual Wrapped maintenance actions, and several remote tests have their own controls and run independently. **Reload** discards unsaved form changes. **Load defaults** only fills the form with default values; they become permanent after saving.

Credentials are stored locally. Because application backups can include API keys, tokens, and personal data, treat them like passwords.

### Basic: client connection

- **Mode – Local server:** the interface uses the application service that delivered it. This is the normal setting for a complete Windows installation.
- **Mode – Remote server:** the interface sends API calls to an installation running on another computer.
- **Server address:** base address including `http://` or `https://` and the port, without `/api`. It is used only in Remote mode.
- **API token for this client:** must match the target server's `server.apiToken`. It is neither a TIDAL nor an AI key and is stored only in this client's local profile.
- **Save client settings:** stores these values separately from the server configuration.
- **Test connection:** checks reachability and token without changing the remaining application settings.

RoonAIViewer manages its server and token through its native connection dialog; see the [RoonAIViewer guide](ROONAI_VIEWER.md).

### Basic: desktop startup

- **Start with Windows:** starts the Electron application and its local service after Windows sign-in.
- **Start minimised in the tray:** initially opens no visible main window. The interface remains available through the notification-area icon.

Both options apply only to the complete Windows application. Browsers and RoonAIViewer use their own startup mechanisms.

### Basic: image and cover storage

- **Storage folder:** shared location for the Roon/TIDAL/audiobook cover cache, local artist images, and Wrapped artwork. An empty value uses the application data directory.
- **Used storage / Objects / Breakdown:** report the size and distribution of the current image collection.
- **Move contents:** copies and verifies the existing collection before switching to the new directory. Other application data is not moved.
- **Recalculate size:** refreshes space and object counts without changing files.

The new folder must remain reachable and writable. The verified move and failure behaviour are described in [section 19](#19-storage-and-maintenance).

### Basic: audiobook capture

- **Audio output folder:** absolute writable path on the Windows computer running the application service. In a browser, enter a path on the server—not on the browser device.
- **Capture zone:** exclusive local Roon zone on that Windows computer. Only its audio signal is recorded.
- **Output format:** fixed MP3 format at 192 kbit/s CBR.

The system check in [section 9](#9-audiobooks) must pass before the first capture.

### Basic: server, Roon, and logs

- **`server.host`:** network address to which the web server binds. `127.0.0.1` allows local access only; LAN binding should be combined with an API token on a trusted network.
- **`server.port`:** HTTP port of the application service. Browser and viewer addresses must be adjusted after a change; the application may restart.
- **`server.apiToken`:** optional protection for control and write access. A configured token must be entered identically in browsers and viewers.
- **`music.service`:** prefers TIDAL or Qobuz results during Roon search and queueing. It does not enable a direct Qobuz application integration.
- **`roon.matching.mode`:** `strict` accepts only very close matches; `relaxed` tolerates larger differences and can return more but less accurate matches.
- **`roon.matching.strategy`:** `smart` uses multi-stage title, alias, and `feat.` fallbacks; `strict` deliberately avoids aggressive fallbacks. `smart` is usually the more robust everyday setting.
- **`playlists.directory`:** location for saved M3U playlists. Empty uses the automatically determined Music folder.
- **`roon.configFile`:** path to the Roon pairing/state file. Change this expert option only for deliberate recovery or after diagnosis.
- **`logs.generationLogRetentionDays`:** automatic generation-log retention in days; `0` disables time-based retention.
- **Roon now-playing raw log:** writes detailed unprocessed now-playing data to a diagnostic file. Enable it only while investigating a problem because the file and its listening information can grow.

### UI: language, default zone, and playlist presentation

- **`ui.language`:** changes the interface between German and English.
- **`ui.defaultPlayZoneId`:** zone preselected after startup in Playlist, TIDAL, and tool views. Empty selects the first available zone.
- **Translate free text internally to English:** turns a non-English free-form playlist request into an English AI working instruction. The visible interface and structured filters remain unchanged.
- **Show matched Roon/TIDAL title:** displays the spelling of the resolved result rather than only the original suggestion.
- **Show match confidence:** exposes the Roon-match assessment. The **High** and **Medium** thresholds define which scores appear secure, medium, or uncertain; High must be above Medium.
- **Replace uncertain results only:** enables a targeted retry for uncertain candidates without touching secure entries.

### UI: repeat filter and model comparison

- **Playlist-history repeat prevention:** checks new suggestions against recently generated playlists.
- **Lookback playlists:** number of earlier playlists included in that check.
- **Maximum repeats:** frequency from which a track is considered overused. Stricter values improve variety but can lower the match rate in a small library.
- **Enable model comparison:** exposes the Ollama model bake-off on the Playlist page.
- **Models (CSV):** comma-separated Ollama model names to run with the same request.
- **Metric:** `foundRate` favours the highest Roon hit rate, `duration` the shortest runtime, and `balanced` weighs both.

### UI: Player and Browser presentation

- **Queue preview:** selects three to eight upcoming tracks per zone card.
- **Browser zone zoom / detail zoom:** scales the complete reduced zone overview or a detail opened from it from 70 to 160 percent.
- **Browser zone text / detail text:** scales only the text in those Browser views, allowing image and type size to be tuned independently.
- **Cover backdrop scope:** confines the blurred cover background to the artwork area or extends it across the detail panes and track list.
- **Track-list brightness:** controls the brightness of that backdrop behind the right-hand track list.
- **Player zone view:** visibility, order, and per-zone TIDAL target playlist can be assigned for every discovered Roon zone. Layout can be one column, two columns, or automatic. **Load TIDAL playlists** refreshes the targets available to `T+`.
- **Browser zone view:** maintains its own visibility, order, and column selection. These settings affect only the reduced Browser presentation and do not alter a Roon zone.

### AI: general control

- **Enable AI playlist generation:** switches only the AI source on or off. Player, Last.fm/Deezer/Wrapped playlists, TIDAL, audiobooks, and Roon Tools remain available.
- **`ai.mode`:** selects Antigravity, ChatGPT Work, Ollama, OpenRouter, OpenAI, Gemini, or Claude. Only the chosen route's settings are used for new AI playlists.
- **Request timeout:** maximum wait per AI HTTP request. A larger value accommodates slower models but delays failure detection.
- **Cloud ultra-saver mode:** attempts cloud generation with one request and no refill. It lowers cost and request volume but may return fewer tracks than requested.
- **German reference catalogue:** uses a local JSON list as a title basis for German vocals or Schlager. Path selects the file; **Max Hints** limits entries added to each prompt; **Diversity Lookback** avoids recently used reference tracks.
- **Minimum found rate:** Roon match ratio from which a list is considered sufficient.
- **Automatically replace missing tracks / maximum passes:** control whether and how often missing candidates are repaired automatically.

### AI: shared provider options

Depending on the provider, fields for **URL**, **API key**, **model preset**, **custom model**, and additional runtime options are offered; not every provider has or supports every setting below. A custom name overrides the preset. API keys are stored locally and included in application backups.

- **Temperature:** lower values produce more stable, less varied answers; higher values increase variation. `auto` lets the application or provider choose. Not every reasoning model accepts temperature.
- **Reasoning/Think:** controls reasoning effort for compatible models. Unsupported models may ignore or reject it.
- **Quality mode:** uses a more conservative process and potentially additional checks, requiring more time.
- **Fast mode:** reduces retries and delays; faster, with less resilience to temporary provider problems.
- **Saver mode:** attempts a single request and does not refill missing tracks.

### AI: Google Antigravity CLI

- **Executable:** `agy.exe` uses Windows PATH; a full path is accepted for installations outside PATH.
- **Open sign-in:** launches the interactive Antigravity terminal visibly on the app system for the one-time Google authentication. It is not opened on a remote browser or RoonAIViewer computer.
- **Check CLI:** verifies executable, version, authentication, credit policy, and available account models without creating a playlist.
- **Model selector:** offers current Gemini variants and other known Antigravity choices. The check supplements these with `agy models`. **Automatic** uses the account default; **Custom** keeps arbitrary future IDs possible.
- **Reasoning effort:** can be left automatic when it is already part of the selected model name. Higher effort may improve difficult curation requests but usually consumes more quota and time.
- **Timeout:** limits the complete background CLI run. It should allow enough time for a longer playlist and the selected effort level.
- **Allow existing paid credits:** disabled by default. Enable it only when global Antigravity G1/AI credits are intentionally available for this application. Roon AI Playlist itself cannot purchase credits.

The free plan, model catalogue, and quota windows are Google services and are not guaranteed by Roon AI Playlist. If a model disappears or becomes unavailable, run **Check CLI** again and choose an entry currently reported for the account.

### AI: Ollama

- **URL:** Ollama endpoint from the application server's perspective. If Ollama runs on another computer, use its LAN address instead of `localhost`.
- **Test connection:** checks the endpoint independently of playlist generation.
- **Preset / custom model:** selects an installed model. The custom field overrides the preset.
- **Think, Temperature, Quality, Saver, and Fast mode:** control reasoning, variation, and the speed/quality balance of the local model.

### AI: OpenRouter

- **URL / API key / model:** connect the OpenRouter endpoint and select a model ID in `provider/model` form.
- **Custom model list:** **Add custom model** deliberately adds the free field to the dropdown. Individual custom entries or the complete custom list can be deleted; built-in presets remain. The change becomes permanent with **Save changes**.
- **Reasoning, Temperature, Quality, and Fast mode:** apply only when supported by the selected model.
- **Max retries, Retry delay, Max retry delay, Inter-batch delay:** limit retry count and waiting during rate limits or temporary failures. Very small values fail faster; very large values can extend a run substantially.

### AI: OpenAI and Gemini

Both sections provide **URL**, **API key**, model preset, custom model, reasoning effort, temperature, and Fast mode. The custom field overrides the preset. Use reasoning and temperature only in combinations supported by the chosen model; if uncertain, leave reasoning empty and temperature on `auto`.

### AI: Claude

- **URL / API key / model:** select the Anthropic endpoint and Claude model.
- **Max tokens:** upper bound for the generated response. Too small a value can truncate a track list.
- **Temperature:** response variation where the model supports it.
- **Anthropic version:** API version header. Change it only when required by the Anthropic endpoint in use.
- **Enable Thinking / Budget tokens:** reserves a separate reasoning budget for supported models; it increases runtime and usage.
- **Fast mode:** uses a shorter retry/delay strategy.

### Services: TIDAL

- **Enable direct TIDAL integration:** exposes the application's TIDAL areas and permits search, mix/playlist synchronisation, audiobook search, and `T+`. A TIDAL account configured inside Roon is unaffected.
- **Client ID / Client secret:** application OAuth credentials. They are stored locally and in application backups.
- **Connect / Authorise TIDAL:** starts device authorisation, displays the code, and opens the TIDAL confirmation page.
- **Disconnect:** removes the stored application login and local mix selection; it does not disconnect TIDAL from Roon.

### Services: Last.fm

- **Enable mood hints:** enriches matched tracks through Last.fm tags and can support the Last.fm playlist source or mood assignment.
- **API key:** without a key, Last.fm calls and the corresponding selector remain disabled.
- **Reload / edit tag list:** reloads the saved list or opens the editor for Last.fm tags offered on the Playlist page. Validate edits before saving.

### Services: Deezer

- **Enable Deezer:** uses its keyless API as an additional source for covers, artist images, and release data.
- **Prefer during cover backfill:** places Deezer before Last.fm in that cover workflow. General artist-image order remains independently controlled under Wrapped.
- **Timeout:** maximum wait per request. Higher values tolerate slow responses; lower values abort earlier.
- **Reload / edit tag list:** manages the chips used by the Deezer playlist source.

### Services: fanart.tv and AI tags

- **Enable fanart.tv:** activates high-quality artist portraits and backgrounds.
- **Project API key:** required credential. **Personal API key** is optional and does not replace the Project key.
- **Timeout:** shared maximum wait for fanart.tv and the required MusicBrainz lookup.
- **AI tag list:** controls the genre chips of the AI playlist source. The second value on each editor line is inserted into the AI prompt.

Other automatic sources such as MusicBrainz/Cover Art Archive and TheAudioDB have no general service fields in this version; their use follows the relevant metadata or artwork workflow.

### Wrapped: counting rules

- **Polling interval:** interval for local state observation. Shorter reacts faster but adds load; the allowed range is one to 30 seconds.
- **Pause timeout:** uninterrupted pause duration after which a listening session is closed.
- **Minimum heard seconds:** fallback for tracks without known duration, especially Live Radio.
- **Minimum heard ratio:** percentage of a known track duration required for a regular counted play.
- **Short Track Seconds / Short Track Min Ratio:** retained legacy fields from an earlier short-track rule. They currently do not affect counting and should normally remain unchanged.
- **Replay window:** period during which a repeated play is evaluated as a replay.
- **Max stored sessions:** local-history limit. The oldest sessions may be removed when it is exceeded.

Changes affect new or still-open sessions. Historical statistics are not automatically recalculated.

### Wrapped: artist images

- **Image-provider order:** enabled sources are checked from top to bottom and the first usable result wins. Providers can be disabled or moved with the arrow controls. Manually pinned images always take priority.
- **Search stored images:** initially searches only local assignments for an artist.
- **Query Roon once during Refresh:** permits an additional Roon request for that targeted refresh.
- **Image actions:** results can be pinned, rejected for that artist, allowed again, or replaced by JPEG, PNG, or WebP between 10 KB and 3 MB.

The complete workflow is described in [section 11](#11-artwork-and-artist-images).

### Wrapped: data management

- **Complete Wrapped data:** fully runs missing albums, missing covers, and local image copies in that order.
- **Complete automatically:** starts the same sequence immediately and then checks every five minutes for new gaps.
- **Stop run:** stops the active stage after its current provider request.
- **Resolve unknown albums / Backfill covers / Localise external covers:** run the three stages separately for diagnosis or targeted maintenance.
- **fanart.tv artist images:** cautiously re-evaluates existing Wrapped artist images against fanart.tv.
- **Fill Roon image cache:** copies known Roon image keys into the local cache in throttled batches. Limit controls images per run; Auto pause controls the interval between automatic batches. **Start automatic Roon image cache** continues those batches with the configured pauses and can be stopped again.
- **External covers per step:** limits a batch to 25, 50, or 100 images.
- **Reset cover search:** resets only stored backfill progress and permits another pass.
- **Clean skips:** removes historical skip flags from test or legacy data.
- **Delete Wrapped data:** irreversibly deletes the complete Wrapped history. Create a backup first.
- **Manage missing covers:** groups unresolved tracks and permits metadata correction, targeted retry, or confirmed deletion of the affected plays.

Progress bars and counters distinguish checked tracks, hits, and open candidates. Detailed safe procedures are in [section 10](#10-roon-wrapped).

### Remote

This tab contains three independent systems:

- **Roon dummy-zone proxy:** enable switch, music, audiobook, and dummy zones, default target, and persistence of the last target. **Validate configuration**, **Refresh status**, and **Synchronise dummy** inspect marker queue, active target, last command, and latency. See [section 15](#15-remote-control-proxy).
- **Network triggers:** each trigger has an enable switch, name, one or more zones, optional ON and/or OFF HTTP GET command, and a switch-off delay when applicable. Configuration, both directions, and live state are checked per trigger; obsolete triggers can be deleted individually. See [section 14](#14-network-triggers).
- **IR/WLAN slots:** up to ten slots with enable switch, optional toggle, visible label, action, zone, and—depending on the action—a station or playlist target. **Load targets** refreshes Roon objects and **Test** checks the slot. See [section 13](#13-remote-slots).

### Maintenance: automatic backups

- **Enable automatic backups:** activates the scheduled compact backup.
- **Backup folder:** destination; empty uses the backups subdirectory in application data.
- **Check interval in hours:** how often the application determines whether a backup is due.
- **Maximum age in hours:** latest point at which a new automatic backup is created.
- **Retained versions:** number of automatic backups kept.

An automatic backup is deliberately smaller than a full backup. Contents, protection, and restore are described in [section 18](#18-backup-and-restore).

### Maintenance: checks, export, and import

- **Check data:** validates the package, central data stores, SQLite/JSON consistency, and selected storage state.
- **Health check:** examines Roon connection, services, media process, storage, and configuration and presents every check with status and details.
- **Export backup:** creates a normal downloadable backup.
- **Export full backup:** additionally includes database, metadata, and image/cover cache and can be much larger.
- **Create full backup in backup folder:** writes the same comprehensive archive directly to the configured server directory.
- **Import backup:** validates a ZIP or compatible older JSON backup before applying it. Stop media maintenance and audiobook capture first.
- **Test API token:** checks the current access protection.
- **Delete stored token:** removes only the locally stored client token; the server token remains configured.

While a backup runs, other backup actions are disabled. Visible progress reports stage, data source, counters, and elapsed time.

### Save & Logs

- **Save changes:** validates and stores server configuration. Host or port changes can restart the service.
- **Reload:** loads the stored state again and discards unsaved form edits.
- **Load defaults:** fills the form with defaults; only saving makes them permanent. Create a backup before a broad reset.
- **Open / purge log:** opens or clears the AI generation log. Automatic retention is configured under Basic.
- **Provider and status filters:** restrict visible generation statistics; **Export CSV** saves that report.
- **Error log:** groups UI, API, network, provider, and server errors with timestamp, area, details, and occurrence count. Refresh reads the latest state; Clear deletes the current error collection.

The error log is a diagnostic aid. A single network or provider failure may be temporary; repeated errors together with their time and the function used immediately beforehand provide stronger evidence.

## 18. Backup and restore

### Backup contents

Depending on the backup type, it can contain:

- application configuration,
- credentials and tokens,
- Wrapped data,
- audiobook library and progress,
- remote slots and network triggers,
- metadata and image assignments,
- SQLite database and portable snapshot.

Backups must be treated as confidential.

### Manual backup

1. Open **Configuration > Maintenance**.
2. Start backup export.
3. Select the destination.
4. Wait for progress and completion confirmation.
5. Store the backup in a protected location.

Additional backup actions remain disabled while a backup is active.

### Restore

1. Preserve the current state separately where possible.
2. Stop active media-maintenance jobs and audiobook capture.
3. Open Restore and select the backup file.
4. Wait for file validation.
5. Confirm the restore.
6. After restart, check Roon, services, zones, and maintenance status.

A current backup is recommended before every application update.

## 19. Storage and maintenance

### Moving image and cover storage

**Configuration > Basic > Image and cover storage** shows the active folder, size, and item count.

1. choose a new folder or enter an absolute path,
2. start **Move contents**,
3. wait for confirmation.

The application copies and verifies files before switching to the new location. If a collision or validation error occurs, the original data remains in place.

### Media processing

Provider requests, image downloads, image validation, hashing, and cache work are supervised separately. Extensive cover maintenance should therefore not interrupt Player, the Roon connection, web interface, or network triggers.

### Health check

The health check includes:

- Roon connection,
- central data stores,
- media processing,
- cache and storage state,
- selected configuration errors.

### Error log

The combined error log contains time, source, area, message, details, and occurrence count. Repeated identical errors can be grouped. The time, active playback, and function used immediately beforehand are particularly useful for diagnosis.

## 20. Security and privacy

- Operate the application only on a trusted private network.
- Use an API token for browsers and viewers.
- Do not expose the application service directly to the internet.
- Do not show API keys or tokens in screenshots or public documents.
- Treat backups like passwords because they can contain credentials and listening history.
- Enable only required external services.
- Carefully verify network-trigger addresses because they control real devices.

Wrapped, audiobook data, and image caches are managed locally. External requests occur only through enabled features and remain subject to the respective provider's policies.

## 21. Troubleshooting

### Roon is not connected

- Is the Roon Core running?
- Is **AI Playlist Generator** authorised under Roon Extensions?
- Are both systems on the same network?
- Is discovery blocked by a firewall?
- Restart the application service from the tray menu.

### A zone is missing

- Enable and name the zone in Roon.
- Check whether it belongs to another zone group.
- Reconnect Roon.
- Then update any affected remote or trigger configuration.

### Queue count is visible but tracks are missing

- Wait briefly for the queue update.
- Verify that another track really exists.
- Reconnect the application after a Roon Core restart.

### AI playlist generation fails

- Is AI enabled in Configuration?
- Check provider, model, and credentials.
- Run the connection test.
- For Ollama on another computer, use that computer's LAN address instead of `localhost`.
- For Antigravity, run **Check CLI** first. Use **Open sign-in** if authentication is missing; use a model reported by `agy models` if the selected ID is unavailable.
- If the Antigravity quota is exhausted, wait for Google's displayed reset or select another model with available quota. The application does not bypass limits by purchasing credits.

### TIDAL search or `T+` fails

- Check TIDAL connection and authentication.
- Verify the target playlist assigned to the zone.
- Ensure that the current item was identified as music.
- Inspect provider errors in the log.

### Live radio receives no enrichment

- Check the station mode: `A` disables external enrichment.
- Verify that artist and title can be recognised as music.
- In `V`, display remains identical to Normal; only Wrapped is cautious.
- Missing lookup is intentional for jingles and advertising segments.

### Live radio shows an incorrect match

- Check the station's raw data and the current title transition.
- Look for damaged characters or swapped fields.
- Inspect provider errors and best-candidate information.
- If the item is in Wrapped, correct its metadata under **Manage missing covers** and retry.

### Artist image is missing

- Check provider order.
- Ensure at least one provider is enabled.
- Allow the full artist identity to be searched first.
- Start a targeted refresh.
- Pin a custom image if necessary.

### A track is missing from Wrapped

- Is Wrapped enabled?
- Was playback long enough to qualify?
- Is it an audiobook, jingle, or another filtered segment?
- Check the live-radio station mode.
- In Cautious mode, no entry is created without a usable result.

### Wrapped artwork remains unresolved

- Run **Complete Wrapped data**.
- Then open **Manage missing covers**.
- Correct artist, title, and album spelling.
- Start a targeted retry or use a custom image.

### Audiobook chapters are incomplete

- Synchronise the audiobook again.
- Run analysis again.
- Check that Roon presents the book as one browsable album.
- Inspect maintenance logs for browse or connection errors.

### Audiobook capture does not start

- Run **Check system** again.
- Verify exclusive zone, input device, destination, and free space.
- Authorise the additional Roon extension.
- Ensure the book has been synchronised and fully analysed.

### Network trigger responds only to Test

- Is the trigger enabled and assigned to the correct zone?
- Has a genuine new playback start occurred since the last manual OFF action?
- Check Playing or Loading state in the trigger card.
- For groups, verify whether another zone remains active.
- Check ON/OFF configuration and scheduler state.

### Browser or viewer reports offline

- Check server address and port.
- Verify the API token.
- Check firewall and network connection.
- In RoonAIViewer, open connection settings and run the connection test.
- Then perform a complete reload.

## 22. Recommended setup sequence

For a new installation, the following order is useful:

1. Connect Roon and verify zones in Player.
2. Set language and UI zoom.
3. Configure an API token and secure LAN access when browsers or viewers will be used.
4. Enable only required external services and test them individually.
5. Assign TIDAL target playlists to zones.
6. Load live-radio stations and choose their modes.
7. Enable Wrapped and select the desired rules.
8. Arrange artist-image providers.
9. Synchronise and analyse audiobooks.
10. Create and test remote slots and network triggers individually.
11. Select image storage.
12. Run the health check.
13. Create the first complete backup.

This verifies the core installation before automatic data completion, audiobook capture, or external-device control is enabled permanently.
