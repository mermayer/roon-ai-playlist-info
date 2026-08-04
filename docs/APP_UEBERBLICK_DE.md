# App-Überblick

Roon AI Playlist ist eine lokale Begleitanwendung für Roon. Sie ergänzt die Wiedergabe in Roon, ersetzt aber weder den Roon Core noch die normalen Roon-Clients.

## Bedienmöglichkeiten

| Oberfläche | Geeignet für | Besonderheiten |
|---|---|---|
| Vollständige Windows-App | Rechner, auf dem auch der App-Dienst läuft | Hauptfenster, Tray-Betrieb und lokale Verwaltung |
| Browser | Tablets, Wanddisplays und beliebige Rechner im Heimnetz | keine zusätzliche Client-Installation erforderlich |
| RoonAIViewer | dauerhaft genutzte Windows-Anzeige auf einem entfernten Rechner | eigenes Fenster, Tray, Autostart, fester Zoom und verschlüsselte Token-Speicherung |

Alle drei Oberflächen zeigen dieselben vom App-Dienst bereitgestellten Zonen- und Mediendaten. Der Viewer erzeugt keine zweite Roon-Verbindung.

## Hauptbereiche

### Playlist

Playlisten können aus freien Musikwünschen, Tags, Last.fm-Empfehlungen oder Wrapped-Favoriten entstehen. Vor der Wiedergabe prüft die App, welche Titel tatsächlich in Roon verfügbar sind.

### Player

Der Player zeigt Roon-Zonen, Wiedergabestatus, Cover, Metadaten, Interpretenbilder, Fortschritt und Warteschlangen. Für Live Radio, Spotify-Streams und Hörbücher gelten jeweils passende Darstellungen und Bedienelemente.

![Übersicht des Mehrzonen-Players](../assets/screenshots/new_zone_view.png)

### Hörbücher

Hörbücher aus Roon werden mit Kapiteln, Gesamtdauer, Fortschritt und Lesezeichen verwaltet. Ein Buch lässt sich fortsetzen, neu beginnen oder an einer gespeicherten Position weiterhören.

### Wrapped

Wrapped zeichnet qualifizierte Hörsitzungen lokal auf und stellt Hörzeit, Titel, Interpreten, Alben, Quellen, Tageszeiten, Skips und Wiederholungen dar. Dashboard, Show und Story lassen sich für verschiedene Zeiträume öffnen.

### Roon Tools

Roon Tools bündelt Live-Radio-Sender, Roon-Playlisten, Warteschlangen und frei belegbare Fernbedienungsaktionen. Pro Radiosender kann festgelegt werden, wie externe Metadaten behandelt werden.

### Konfiguration und Wartung

Hier werden Verbindungen, optionale Dienste, Oberfläche, Wrapped, Hörbücher, Bildanbieter, Netzwerk-Trigger, Sicherungen und Diagnosen verwaltet.

## Lokaler Betrieb

Die App ist für den Betrieb im eigenen Netzwerk ausgelegt. Roon-, Wrapped-, Hörbuch- und Cache-Daten werden lokal verwaltet. Externe Anfragen entstehen nur für aktivierte Dienste und Funktionen, beispielsweise KI-Anbieter, TIDAL oder Bild- und Metadatenanbieter.
