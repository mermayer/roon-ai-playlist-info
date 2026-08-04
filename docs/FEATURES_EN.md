# Feature overview

This overview describes functions that Roon AI Playlist adds to a standard Roon system. Roon continues to provide the library, zones, and playback engine.

## AI and recommendation playlists

- free-form music requests in natural language
- choice of Ollama, OpenRouter, OpenAI, Gemini, and Claude
- filters for genre, decade, mood, and language
- playlist suggestions from Last.fm tags, maintained tag lists, and Wrapped Top 20
- matching against the actual Roon library
- visible matches, missing tracks, and possible replacements before playback
- playback in a selected zone or export as M3U

## Direct TIDAL tools

- track, album, and artist searches through TIDAL
- import of suitable TIDAL mixes with custom exclusion filters
- a fixed target TIDAL playlist for each Roon zone
- adding the current track through the `T+` button
- saving identified live-radio tracks to the selected target playlist

## Enhanced player

- combined overview of multiple Roon zones
- detail view with artwork, metadata, progress, and queue
- pending-track count and total remaining time
- appropriate controls for music, live radio, Spotify streams, and audiobooks
- browser view for large displays and remote devices
- artist portraits and wide backgrounds from multiple sources
- configurable artist-image provider order
- combined artist lookup for duos and groups before an optional split into individual artists

## Live radio

- detection and repair of swapped or damaged metadata fields
- repair of common character-encoding errors affecting umlauts and apostrophes
- enrichment of missing track, artist, album, and artwork information
- searches through TIDAL, stored matches, MusicBrainz/Cover Art Archive, Last.fm, and Deezer
- filtering of jingles, advertisements, news, intros, outros, station IDs, and technical automation labels
- protection against confusing a station logo with track artwork
- three persistent modes for every station:
  - **Normal:** enrichment and regular inclusion in Wrapped
  - **Cautious:** the same search and display as Normal, but no Wrapped entry without a usable match
  - **Off:** no external enrichment and no Wrapped entry

## Artwork and artist images

- configurable search order for fanart.tv, TIDAL, Roon, Last.fm, Deezer, and TheAudioDB
- local storage of retrieved images
- pinning preferred images, rejecting unsuitable results, or uploading custom images
- targeted lookup for an individual artist
- automatic completion of missing Wrapped albums and covers
- list of unresolved covers with editable artist, track, and album fields
- targeted retry or safe removal of affected Wrapped entries

## Audiobooks

- synchronization of Roon albums recognised as audiobooks
- complete analysis of books with very large chapter counts
- chapter count, total duration, current position, and remaining time
- resume, restart, and direct chapter selection
- manual and automatic bookmarks independent of the playback zone
- optional enrichment of audiobook metadata and covers
- exclusion of recognised audiobooks from music Wrapped and artist-image searches
- optional capture through a dedicated Roon zone with chapter splitting and embedded MP3 metadata

## Roon Wrapped

- local recording of qualified music, live-radio, and Spotify listening sessions
- analysis of listening time, sources, time of day, tracks, artists, and albums
- recognition of skips and replays
- Dashboard, Show, cover mosaic, and Story
- year, quarter, month, rolling 30/90 days, all time, and custom ranges
- direct playback of historical tracks in a Roon zone
- PNG, PDF, and CSV exports
- data-quality reporting and tools for missing albums and artwork

## Remote control and external devices

- up to ten configurable Roon action slots
- quick launch of radio stations, playlists, and zone actions
- multiple independent network triggers for Roon zones
- separate HTTP commands for ON and OFF
- delayed power-off after pause or stop
- cancellation of pending power-off when playback resumes
- manual OFF button in affected zone views
- optional remote-control proxy through a dedicated Roon dummy zone

## Operation and maintenance

- automatic and manual backups
- restoration on a new system
- local image and cover storage with a selectable location
- separate media processing so extensive artwork searches do not interrupt the Roon connection or interface
- health checks, error log, and status displays
- German and English user interface
