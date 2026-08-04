# Application overview

Roon AI Playlist is a local companion application for Roon. It extends Roon playback but does not replace the Roon Core or the standard Roon clients.

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

The player displays Roon zones, playback state, artwork, metadata, artist images, progress, and queues. Live radio, Spotify streams, and audiobooks receive purpose-built layouts and controls.

![Multi-zone Player overview](../assets/screenshots/new_zone_view.png)

### Audiobooks

Audiobooks from Roon are managed with chapters, total duration, progress, and bookmarks. A book can be resumed, restarted, or continued from a saved position.

### Wrapped

Wrapped records qualified listening sessions locally and presents listening time, tracks, artists, albums, sources, time of day, skips, and replays. Dashboard, Show, and Story views are available for multiple date ranges.

### Roon Tools

Roon Tools combines live-radio stations, Roon playlists, queues, and configurable remote actions. Each station can have its own external-metadata policy.

### Configuration and maintenance

This area manages connections, optional services, interface settings, Wrapped, audiobooks, image providers, network triggers, backups, and diagnostics.

## Local operation

The application is intended for use on a private local network. Roon, Wrapped, audiobook, and cache data is managed locally. External requests occur only for enabled services and features, such as AI providers, TIDAL, or artwork and metadata providers.
