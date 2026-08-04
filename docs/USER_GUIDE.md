# Roon AI Playlist user guide

[Deutsche Version](BENUTZERHANDBUCH_DE.md) · [Back to overview](../README.md)

Documentation status: Roon AI Playlist **1.0.458**, RoonAIViewer **1.0.3**.

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

Roon AI Playlist extends an existing Roon system. Roon remains responsible for the music library, streaming, RAAT, DSP, zones, queues, and audio playback. The application adds further control and management features:

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

- Ollama, OpenRouter, OpenAI, Gemini, or Claude for AI playlists,
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

![Zone detail with queue and artist artwork](../assets/screenshots/player.png)

### Zone overview

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

Categories used by Last.fm, AI, and Deezer-based sources can be edited and checked under **Configuration > Services**. Validate changes before saving them.

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

## 14. Network triggers

Network triggers connect Roon playback state to external devices.

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

## 15. Remote-control proxy

The optional dummy-zone proxy can forward play, pause, next, and previous from a Bluetooth or similar remote to the most recently active music or audiobook zone.

It requires:

- a dedicated Roon dummy zone,
- a selected music zone,
- a selected audiobook zone,
- the supplied long marker tracks in the specified order.

The application distinguishes intentional marker movement from natural track completion and feedback. Target zone, marker, last command, and acknowledgement time are shown in Configuration. Volume and mute are not forwarded.

Validate the configuration and synchronise the dummy zone before use.

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

### Basic

- server and desktop behaviour,
- Windows startup and minimised startup,
- image and cover storage,
- audiobook capture and target zone,
- fundamental Roon settings.

### UI

- language,
- visible views,
- presentation options,
- browser zoom for overview and detail views.

### AI

- enable or completely disable AI features,
- select provider and model,
- configure local or external connection,
- test the connection.

### Services

- TIDAL,
- Last.fm,
- Deezer,
- fanart.tv,
- further metadata and image sources,
- playlist tag lists.

### Wrapped

- enable tracking,
- time and quality rules,
- export options,
- complete data,
- manage missing covers and artist images,
- configure provider order.

### Remote

- up to ten remote slots,
- network triggers,
- dummy-zone proxy.

### Maintenance and logs

- health check,
- service status,
- backup and restore,
- data validation,
- error log and export,
- storage and cache information.

Most changes take effect after **Save changes**. Fundamental server-address or port changes can restart the application service automatically.

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
