# Frequently asked questions

## Does Roon AI Playlist replace the Roon GUI or Roon Core?

No. The application deliberately complements Roon instead of reproducing its GUI, library management, playback engine, RAAT, DSP, queues, or standard controls. It requires a reachable Roon Core and adds workflows outside Roon only where the Roon Extension APIs make that possible.

## Must I use an AI provider?

No. AI playlist generation can be disabled. Player, live radio, audiobooks, Wrapped, Roon Tools, and other non-AI features remain available.

## Can the application be used without TIDAL?

Yes. TIDAL extends search, live-radio identification, and playlist actions, but is not required for every part of the application. Other sources or local Roon data remain available depending on the feature.

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

## Is RoonAIViewer a second server?

No. The viewer only displays the interface of the existing application system. It starts no application service, does not connect directly to Roon, and stores no independent listening history.

## What happens when I close the viewer?

The window is hidden in the Windows notification area. Only **Beenden** in the tray menu exits the viewer completely. The remote application service remains active in both cases.

## Does this public package include an installer?

No. Installers and source code are not distributed publicly.
