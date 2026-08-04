# App-Überblick

Roon AI Playlist ist eine lokale Begleitanwendung für Roon. Sie soll weder die Roon-Oberfläche, den Roon Core noch irgendeine normale Roon-Funktion ersetzen. Sie wurde geschaffen, um außerhalb von Roon zusätzliche, dort fehlende Arbeitsabläufe bereitzustellen – innerhalb der Möglichkeiten und Grenzen der Roon-Extension-APIs.

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

Hörbücher aus Roon werden mit Kapiteln, Gesamtdauer, Fortschritt und Lesezeichen verwaltet. Ein Buch lässt sich fortsetzen, neu beginnen oder an einer gespeicherten Position weiterhören. Ein eigener Audible-/DNB-Katalog unterstützt die Entdeckung; eine geprüfte TIDAL-Albensuche kann eine verfügbare Ausgabe in die Hörbuchliste der App übernehmen. Die optionale Aufnahme über eine exklusive lokale Roon-Zone erzeugt MP3-Kapiteldateien mit Metadaten.

### Wrapped

Wrapped zeichnet qualifizierte Hörsitzungen lokal auf und stellt Hörzeit, Titel, Interpreten, Alben, Quellen, Tageszeiten, Skips und Wiederholungen dar. Dashboard, Show, Story, Status und eine filterbare titelgenaue Historie lassen sich für verschiedene Zeiträume öffnen. Historische Titel können über Roon erneut abgespielt werden; Exporte und Reparaturwerkzeuge bearbeiten fehlende Alben und Cover.

### Direkte TIDAL-Werkzeuge

Persönliche Mixe, Daily Discovery, Titelradio, Interpretenradio, redaktionelle Playlisten und Benutzerplaylisten lassen sich filtern, prüfen, in einer gewählten Roon-Zone starten oder anhängen. Ausgewählte dynamische Mixe können in feste TIDAL-Playlisten synchronisiert werden; `T+` speichert den laufenden oder erkannten Live-Radio-Titel in einer pro Zone festgelegten Zielplaylist.

### Roon Tools

Roon Tools bündelt Live-Radio-Sender, Roon-Playlisten, Warteschlangen und frei belegbare Fernbedienungsaktionen. Pro Radiosender kann festgelegt werden, wie externe Metadaten behandelt werden.

### Fernbedienungen und externe Geräte

Zehn konfigurierbare Aktionsslots können Sender, Playlisten oder Zonenaktionen aus der Oberfläche oder über kompatible lokale Hardware starten. Unabhängige Netzwerk-Trigger verbinden den Zonenstatus mit HTTP-gesteuerten Verstärkern, Steckdosen, IR-Bridges oder Automationssystemen. Ein optionaler RoPieee-Dummy-Zonen-Proxy leitet Play, Pause, Next und Previous an die zuletzt aktive Musik- oder Hörbuchzone weiter.

### Konfiguration und Wartung

Hier werden Verbindungen, optionale Dienste, Oberfläche, Wrapped, Hörbücher, Bildanbieter, Netzwerk-Trigger, Sicherungen und Diagnosen verwaltet.

## Lokaler Betrieb

Die App ist für den Betrieb im eigenen Netzwerk ausgelegt. Roon-, Wrapped-, Hörbuch- und Cache-Daten werden lokal verwaltet. Externe Anfragen entstehen nur für aktivierte Dienste und Funktionen, beispielsweise KI-Anbieter, TIDAL oder Bild- und Metadatenanbieter.
