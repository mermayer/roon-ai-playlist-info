# Privacy and security

## Basic principle

Roon AI Playlist is designed for local operation on a private network. Zone state, Wrapped history, audiobook data, settings, logs, and cached artwork and artist images are managed on the application system.

## External connections

Requests to external services occur only when the corresponding feature is enabled and used. These services may include:

- the selected AI provider for playlist suggestions
- TIDAL for search and playlist actions
- Last.fm and Deezer for music and image information
- fanart.tv and TheAudioDB for artist images
- MusicBrainz and Cover Art Archive for album information and artwork
- Audible for optional audiobook information
- local or external HTTP targets configured by the user for network triggers

The search terms or metadata sent to a provider depend on the function being used. Optional services are also governed by their own privacy policies.

## Credentials

API keys, tokens, and sign-in details are stored in the local application configuration. Application backups may contain these credentials and should therefore be protected like passwords.

RoonAIViewer protects the server token with Windows DPAPI and binds it to the current Windows user account.

## Home-network access

- Enable network access only on a trusted private network.
- Configure an API token for browser and RoonAIViewer access.
- Allow only the required port through the firewall.
- Do not expose the application directly to the internet.
- Carefully verify external HTTP or HTTPS commands used by network triggers.

## Local images and listening history

Artwork, artist images, and provider responses may be cached locally. Wrapped maintains a local listening history when enabled. Maintenance tools can correct and remove corresponding entries.

## Backups

An application backup is intended to restore settings and local data. Because it may contain personal listening history and credentials:

- store backups only on trusted media,
- never upload them publicly,
- encrypt them or remove sensitive content before sharing,
- securely remove old backups when no longer needed.

## Independence

Roon AI Playlist is an independent project. External services may require separate accounts and remain subject to the terms of their respective providers.
