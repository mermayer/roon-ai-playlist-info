# Getting started

## Requirements

- 64-bit Windows 10 or Windows 11
- a reachable Roon Core on the same local network
- permission to authorise extensions in Roon
- optional credentials only for services that will actually be used
- for API-key-free automatic AI playlists: Google Antigravity CLI installed on the same Windows system and a Google account for the one-time sign-in

## First launch

The Windows installer first offers two operating modes:

- **Complete application:** central service and full local Player interface.
- **Server + Configuration:** central service without a permanently loaded local Player; intended for operation through a browser or RoonAIViewer.

Both modes provide the same Roon, Wrapped, automation, media, and audiobook-capture functions. In Server + Configuration mode, open the notification-area icon and select **Configuration** when local settings are required.

On first launch, a setup assistant guides the user through the essential settings:

1. restore an existing application backup or begin a fresh setup
2. discover the Roon Core and authorise the extension under **Roon > Settings > Extensions**
3. choose local-only access or protected access from the home network
4. enable or skip optional services
5. select a playback zone and verify the connection
6. save the configuration

The setup assistant can be opened again later from Configuration.

## Recommended steps after setup

1. Confirm that all desired Roon zones appear in Player.
2. Start normal playback and verify artwork, metadata, and queue information.
3. Load desired live-radio stations in Roon Tools and choose their metadata mode.
4. Enable Wrapped and choose the desired reporting period.
5. Optionally synchronise and analyse audiobooks.
6. For direct TIDAL audiobooks, connect TIDAL, open **TIDAL search**, and mark a result **Listen later**.
7. Before the first TIDAL fast capture, open its separate setup wizard and complete the companion, audio-route, profile, and real-signal checks. A passed, version-bound readiness result is reused until a relevant component changes.
8. Optionally arrange artist-image providers and connect external services.
9. For free automatic AI playlists, select **Antigravity** under **Configuration > AI**, complete **Open sign-in**, run **Check CLI**, choose a model, and save.
10. Create the first application backup.

Antigravity does not require an AI API key. After setup, playlist requests and results are transferred automatically through the local CLI. Google's current free tier, model availability, and usage limits apply; the application never purchases credits.

The TIDAL capture wizard and the production status page are separate views. Reopening setup always displays the complete wizard; starting **Fast capture** displays the current job with progress, remaining time, chapter-boundary pause, resume, and abort controls.

## Access from the home network

For a browser or RoonAIViewer, the application service must accept connections from the local network. Its port must be reachable through the firewall on the server computer. An API token should be configured for this use, and access should be limited to a trusted private network.

Server + Configuration mode is particularly suitable for this arrangement. It keeps the service and background functions running while avoiding a permanent local Player window. The operating mode can be changed later under **Configuration > Basic**; saving the change restarts the desktop application.

## Updates

Create a current backup before updating. Existing settings and local data are normally retained after installation. Following the first launch of a new version, briefly check the Roon connection, Player view, and maintenance status.

For detailed operation of every application area, continue with the [complete user guide](USER_GUIDE.md).
