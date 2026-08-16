# Frequently asked questions

## Does Roon AI Playlist replace the Roon GUI or Roon Core?

No. The application deliberately complements Roon instead of reproducing its GUI, library management, playback engine, RAAT, DSP, queues, or standard controls. It requires a reachable Roon Core and adds workflows outside Roon only where the Roon Extension APIs make that possible.

## Must I use an AI provider?

No. AI playlist generation can be disabled. Player, live radio, audiobooks, Wrapped, Roon Tools, and other non-AI features remain available.

## Can I create high-quality AI playlists without buying an API key?

Yes. Install the official Google Antigravity CLI on the same Windows system as Roon AI Playlist and complete its one-time Google sign-in. The application can then run current Antigravity models automatically in the background, receive the track list directly, and pass it through the normal Roon matching and replacement workflow. No copying between applications is required.

Google currently offers modern Gemini models in its free Antigravity tier, subject to the current model catalogue and usage quotas. Roon AI Playlist never purchases credits and blocks already enabled paid G1/AI credits by default.

## Which Antigravity model should I select?

**Gemini 3.1 Pro (High)** is the proven default for quality-focused playlist curation. Gemini 3.5 Flash and Gemini 3.6 Flash are useful faster alternatives. **Automatic** uses the account default. Since Google can change availability, **Check CLI** imports models reported by `agy models`, and the custom field supports future IDs.

## Does Antigravity require a browser to remain open?

No. A visible terminal or browser-based Google confirmation may be needed only for the one-time sign-in. Playlist generation afterwards is automatic through the CLI running on the application system.

## Can the application be used without TIDAL?

Yes. TIDAL extends search, live-radio identification, and playlist actions, but is not required for every part of the application. Other sources or local Roon data remain available depending on the feature.

## Does the TIDAL audiobook library download audio files?

No. **Listen later** stores a virtual local record with album, chapters, progress, and bookmarks. The audio remains at TIDAL and direct listening uses the official browser player under the connected subscription.

## Can speed and pitch be changed separately during TIDAL audiobook playback?

Yes. Speed ranges from 1.00× to 2.00× and pitch from 0.50 to 1.50 in 0.05 steps. Changes can be made during playback. Pitch 1.00 bypasses processing; other pitch values use speech-oriented Rubber Band processing.

## Can a TIDAL audiobook play without a Roon zone?

Yes. Select **Windows output** and choose the default device or a specific USB/USB-Bluetooth output. Compatible Bluetooth-headset AVRCP Play/Pause is handled while that Windows audiobook session is active.

## Why should I pause a direct TIDAL audiobook in the application?

The app pause updates the automatic bookmark and keeps its listening session controlled. Roon Previous/Next can change chapters, but some Roon clients remove the resumable Play action after stopping a live Audio Input stream. App Play/Pause is therefore the dependable pause path.

## What prevents another TIDAL stream from interrupting fast capture?

During an active capture, the application blocks its direct TIDAL audiobook, mix, and playlist starts. Manual player actions are also blocked in the separately managed TIDAL Chrome window. The managed session is closed after completion, cancellation, or failure so stale playback state does not carry into the next job.

## How does Spotify playback reach Roon AI Playlist?

Through Roon. The separate native macOS application SpotBridge can capture the local Spotify process with a CoreAudio Process Tap and send it to Roon Audio Input as AAC or losslessly encoded Ogg-FLAC. SpotBridge also forwards artist, title, album, and artwork and can coordinate transport events. After the stream appears in a selected Roon zone, Roon AI Playlist can display it and record a qualified Wrapped session. Roon AI Playlist does not capture Spotify audio or log in to Spotify itself.

Ogg-FLAC preserves the captured signal on its way to Roon; it does not turn the original Spotify source into higher-quality audio.

## Why can live-radio information differ from Roon?

Radio stations supply widely varying and sometimes incomplete metadata. The application attempts to enrich artist, track, album, and artwork through multiple sources and may therefore select a different suitable album result than Roon.

## What do N, V, and A next to a radio station mean?

- `N` – Normal: enrichment and regular Wrapped recording
- `V` – Cautious: the same display and search, but no Wrapped entry without a usable match
- `A` – Off: no external enrichment and no Wrapped entry

## Are jingles and advertisements stored in Wrapped?

Typical jingles, intros, outros, news, advertisements, station IDs, and technical automation labels are filtered before music lookup whenever possible. For ambiguous music-like data, the result depends on the selected station mode and available matches.

## Why is artwork or an artist image missing?

A provider may not have an image, spelling may differ, or a match may be too uncertain. Wrapped and artist-image management can correct metadata, prioritise providers, retry searches, pin images, or use custom images.

## How are duos and groups handled?

A combined name such as “John Travolta & Olivia Newton-John” is searched as one identity first. Only when no suitable combined result exists may the application examine individual participants.

## Where is Wrapped data stored?

Wrapped data is stored locally on the application system. RoonAIViewer does not duplicate it.

## Can I use the application from another computer?

Yes. On the home network, the interface can be opened in a browser or through RoonAIViewer. The application service must allow network access and should be protected by an API token.

## What is Server + Configuration mode?

It is an installer and configuration option for a Windows computer that runs the central application service but does not need a permanently loaded local Player window. Roon, Wrapped, network triggers, media processing, scheduled work, and audiobook capture continue normally. Local settings remain available from the notification-area icon, while the complete interface is used through a browser or RoonAIViewer.

## Can I change the operating mode later?

Yes. Open **Configuration > Basic**, select the desktop operating mode, and save. The desktop application restarts into the selected mode. Existing settings, databases, caches, and backups are shared and are not converted or duplicated.

## Does audiobook capture work in server mode?

Yes. Capture remains a server-side function and can be started or monitored from a remote browser or RoonAIViewer. The configured audio input, exclusive Roon zone, output folder, and generated files remain on the server computer.

## Is RoonAIViewer a second server?

No. The viewer only displays the interface of the existing application system. It starts no application service, does not connect directly to Roon, and stores no independent listening history.

## What happens when I close the viewer?

The window is hidden in the Windows notification area. Only **Beenden** in the tray menu exits the viewer completely. The remote application service remains active in both cases.

## Does this public package include an installer?

No. Installers and source code are not distributed publicly.
