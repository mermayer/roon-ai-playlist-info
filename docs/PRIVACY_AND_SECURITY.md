# Privacy and security

## Basic principle

Roon AI Playlist is designed for local operation on a private network. Zone state, Wrapped history, audiobook data, settings, logs, and cached artwork and artist images are managed on the application system.

## External connections

Requests to external services occur only when the corresponding feature is enabled and used. These services may include:

- the selected AI provider for playlist suggestions
- Google Antigravity when that AI route is selected; the local CLI sends the playlist instruction to Google's service under the signed-in account
- TIDAL for search, album actions, audiobook metadata, and subscribed browser playback
- Last.fm and Deezer for music and image information
- fanart.tv and TheAudioDB for artist images
- MusicBrainz and Cover Art Archive for album information and artwork
- Audible for optional audiobook information
- local or external HTTP targets configured by the user for network triggers

The search terms or metadata sent to a provider depend on the function being used. Optional services are also governed by their own privacy policies.

When **Create AI playlist** is selected for a Wrapped recording, title, artist, album, and the generated recording-profile request are sent to the configured AI provider. That provider classifies narrow genre, actual sung language, style, instrumentation, era/production, vocal character, and energy; automatic modes may send the proposed candidates for a second independent profile audit. Last.fm is not contacted for this recording profile. The resulting profile and playlist remain in the local application state except for the normal requests required by the selected AI service and Roon matching.

## Credentials

API keys, tokens, and sign-in details are stored in the local application configuration. Application backups may contain these credentials and should therefore be protected like passwords.

Antigravity authentication is managed by the official CLI on the application system rather than by an AI API key stored in Roon AI Playlist. The application submits the playlist request and receives the generated track list; it does not receive the user's Google password. Google's privacy terms, model availability, and account quotas apply. Paid G1/AI credits are blocked by default, and the application never initiates a credit purchase.

RoonAIViewer protects the server token with Windows DPAPI and binds it to the current Windows user account.

## Home-network access

- Enable network access only on a trusted private network.
- Configure an API token for browser and RoonAIViewer access.
- Allow only the required port through the firewall.
- Do not expose the application directly to the internet.
- Carefully verify external HTTP or HTTPS commands used by network triggers.

Complete application and Server + Configuration mode use the same local data and network endpoints. Server mode does not publish an additional service or copy data to a Viewer; it only avoids keeping the complete local Player window loaded. Closing its on-demand configuration window does not stop the protected application service.

## Local images and listening history

Artwork, artist images, and provider responses may be cached locally. Wrapped maintains a local listening history when enabled. Maintenance tools can correct and remove corresponding entries.

The virtual TIDAL audiobook library stores album references, chapters, progress, and bookmarks locally; it does not copy the subscribed audio into the library. Direct listening and fast capture use the official TIDAL browser player in a separately managed local Chrome profile. The narrowly scoped companion coordinates that player and its selected audio output but does not extract TIDAL credentials, licence keys, or protected stream data. Captured PCM, speed/pitch processing, temporary master segments, and generated chapter files remain on the application system.

## Backups

An application backup is intended to restore settings and local data. Because it may contain personal listening history and credentials:

- store backups only on trusted media,
- never upload them publicly,
- encrypt them or remove sensitive content before sharing,
- securely remove old backups when no longer needed.

## Independence

Roon AI Playlist is an independent project. External services may require separate accounts and remain subject to the terms of their respective providers.
