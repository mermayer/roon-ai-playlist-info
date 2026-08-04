# Application overview

Roon AI Playlist is a local companion application for Roon. It is not intended to replace the Roon GUI, the Roon Core, or any standard Roon function. It was created to make additional workflows available outside Roon where they are missing, within the possibilities and limits of the Roon Extension APIs.

## Ways to use the application

| Interface | Best suited for | Distinguishing features |
|---|---|---|
| Complete Windows application | Computer that also runs the application service | Main window, notification-area operation, and local administration |
| Web browser | Tablets, wall displays, and computers on the home network | no additional client installation required |
| RoonAIViewer | permanent Windows display connected to a remote server | dedicated window, notification area, autostart, persistent zoom, and encrypted token storage |

All three interfaces display the same zone and media information supplied by the application service. The viewer does not create another Roon connection.

## Main areas

### Playlist

Playlists can be created from free-form music requests, tags, Last.fm recommendations, or Wrapped favourites. Before playback, the application checks which tracks are actually available in Roon.

### Player

The player displays a configurable selection of Roon zones with user-defined order and layout, playback state, artwork, metadata, artist images, progress, and queues. The normal Player and large Browser views can have separate visible-zone selections. Live radio, Spotify streams, and audiobooks receive purpose-built layouts and controls.

![Multi-zone Player overview](../assets/screenshots/new_zone_view.png)

### Audiobooks

Audiobooks from Roon are managed with chapters, total duration, progress, and bookmarks. A book can be resumed, restarted, or continued from a saved position. A separate Audible/DNB catalogue supports discovery, while a verified TIDAL album search can add an available edition to the application's audiobook list. Optional capture through an exclusive local Roon zone creates tagged MP3 chapter files.

### Wrapped

Wrapped records qualified listening sessions locally and presents listening time, tracks, artists, albums, sources, time of day, skips, and replays. Dashboard, Show, Story, Status, and a filterable track-level history are available for multiple date ranges. Historical tracks can be replayed through Roon; exports and repair tools address missing albums and artwork.

### Direct TIDAL tools

Personal mixes, Daily Discovery, track radio, artist radio, editorial playlists, and user playlists can be filtered, previewed, started, or appended in a selected Roon zone. Selected dynamic mixes can be synchronised into stable TIDAL playlists, while `T+` stores the current or identified live-radio track in a target playlist assigned per zone.

### Roon Tools

Roon Tools combines live-radio stations, Roon playlists, queues, and configurable remote actions. Each station can have its own external-metadata policy.

### Remotes and external devices

Ten configurable action slots can start stations, playlists, or zone actions from the interface or compatible local hardware. Independent network triggers connect zone playback to HTTP-controlled amplifiers, smart plugs, IR bridges, or automation systems. An optional RoPieee dummy-zone proxy forwards play, pause, next, and previous to the most recently active music or audiobook zone.

### Configuration and maintenance

This area manages connections, optional services, interface settings, Wrapped, audiobooks, image providers, network triggers, backups, and diagnostics.

## Local operation

The application is intended for use on a private local network. Roon, Wrapped, audiobook, and cache data is managed locally. External requests occur only for enabled services and features, such as AI providers, TIDAL, or artwork and metadata providers.
