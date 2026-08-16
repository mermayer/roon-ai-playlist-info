# App-Überblick

Roon AI Playlist ist eine lokale Begleitanwendung für Roon. Sie soll weder die Roon-Oberfläche, den Roon Core noch irgendeine normale Roon-Funktion ersetzen. Sie wurde geschaffen, um außerhalb von Roon zusätzliche, dort fehlende Arbeitsabläufe bereitzustellen – innerhalb der Möglichkeiten und Grenzen der Roon-Extension-APIs.

## Bedienmöglichkeiten

| Oberfläche | Geeignet für | Besonderheiten |
|---|---|---|
| Vollständige Windows-App | Rechner, auf dem auch der App-Dienst läuft | Hauptfenster, Tray-Betrieb und lokale Verwaltung |
| Nur Server + Konfiguration | dauerhaft laufender, entfernt bedienter App-Rechner | vollständiger zentraler Dienst, lokale Konfiguration bei Bedarf, kein dauerhaftes lokales Playerfenster |
| Browser | Tablets, Wanddisplays und beliebige Rechner im Heimnetz | keine zusätzliche Client-Installation erforderlich |
| RoonAIViewer | dauerhaft genutzte Windows-Anzeige auf einem entfernten Rechner | eigenes Fenster, Tray, Autostart, fester Zoom und verschlüsselte Token-Speicherung |

Alle Anzeige-Clients verwenden dieselben vom App-Dienst bereitgestellten Zonen- und Mediendaten. Nur Server + Konfiguration verändert ausschließlich die lokale Desktop-Darstellung und entfernt keine Dienstfunktion. Browser und Viewer erzeugen keine zweite Roon-Verbindung.

## Hauptbereiche

### Playlist

Playlisten können aus freien Musikwünschen, Tags, Last.fm-Empfehlungen oder Wrapped-Favoriten entstehen. Für KI-Wünsche stehen lokale oder API-basierte Anbieter, die geführte ChatGPT-Work-Übergabe und die vollautomatische Google Antigravity CLI zur Verfügung. Antigravity benötigt keinen API-Key und kann nach einmaliger Anmeldung aktuelle hochwertige Modelle aus Googles kostenlosem Tarif verwenden. Vor der Wiedergabe prüft die App, welche Titel tatsächlich in Roon verfügbar sind.

### Player

Der Player zeigt eine konfigurierbare Auswahl von Roon-Zonen mit frei bestimmbarer Reihenfolge und Darstellung, Wiedergabestatus, Cover, Metadaten, Interpretenbilder, Fortschritt und Warteschlangen. Normale Playeransicht und große Browseransicht können getrennte Sichtbarkeitsauswahlen besitzen. Für Live Radio, Spotify-Streams und Hörbücher gelten jeweils passende Darstellungen und Bedienelemente.

![Übersicht des Mehrzonen-Players](../assets/screenshots/new_zone_view.png)

### SpotBridge und Spotify

SpotBridge 1.0.0 ist eine eigenständige native macOS-Menüleisten-App, die den lokalen Spotify-Prozess über einen CoreAudio Process Tap aufnimmt und das Signal als AAC oder verlustfrei codiertes Ogg-FLAC an Roon Audio Input liefert. Sie übermittelt Interpret, Titel, Album und Cover und kann den Transport von Spotify und Roon koordinieren. Roon AI Playlist stellt die Wiedergabe anschließend dar und zeichnet sie auf, nachdem sie in einer ausgewählten Roon-Zone verfügbar ist; die Spotify-Aufnahme selbst gehört nicht zu Roon AI Playlist.

### Hörbücher

Hörbücher aus Roon werden mit Kapiteln, Gesamtdauer, Fortschritt und Lesezeichen verwaltet. Ein eigener Audible-/DNB-Katalog und eine direkte TIDAL-Suche nach Titel oder Interpret unterstützen die Entdeckung. TIDAL-Treffer können in eine virtuelle **Später anhören**-Bibliothek übernommen, direkt über Roon Audio Input oder einen gewählten Windows-/USB-Bluetooth-Ausgang wiedergegeben und über automatische oder manuelle Lesezeichen fortgesetzt werden. Geschwindigkeit und Pitch sind unabhängig in 0,05-Schritten einstellbar.

Die Schnellaufnahme verwendet eine geführte Audio- und Chrome-Begleiter-Einrichtung, bevorzugt ein geprüftes 4×-Profil mit 2×-Kompatibilitätsfallback und zeigt einen vollständigen Auftragsstatus mit Kapitelpause, Fortsetzen und Abbruch. Andere TIDAL-Wiedergaben sind währenddessen gesperrt. Die Masteraufnahme wird anschließend auf Normalgeschwindigkeit zurückgeführt und in MP3-Kapitel mit Metadaten zerlegt.

![Direkte TIDAL-Hörbuchwiedergabe](../assets/screenshots/tidal_audiobook.png)

### Wrapped

Wrapped zeichnet qualifizierte Hörsitzungen lokal auf und stellt Hörzeit, Titel, Interpreten, Alben, Quellen, Tageszeiten, Skips und Wiederholungen dar. Dashboard, Show, Story, Status und eine filterbare titelgenaue Historie lassen sich für verschiedene Zeiträume öffnen. Historische Titel können über Roon erneut abgespielt werden; Exporte und Reparaturwerkzeuge bearbeiten fehlende Alben und Cover.

### Direkte TIDAL-Werkzeuge

Persönliche Mixe, Daily Discovery, Titelradio, Interpretenradio, redaktionelle Playlisten und Benutzerplaylisten lassen sich filtern, prüfen, in einer gewählten Roon-Zone starten oder anhängen. Ausgewählte dynamische Mixe können in feste TIDAL-Playlisten synchronisiert werden; `T+` speichert den laufenden oder erkannten Live-Radio-Titel in einer pro Zone festgelegten Zielplaylist. Die getrennte Hörbuchsuche bereitet Cover und Albumdaten auf, unterstützt eine breite serienbezogene Titelsuche mit bis zu 200 Treffern sowie Sortierungen einschließlich **Älteste zuerst**.

![Direkte TIDAL-Hörbuchsuche](../assets/screenshots/tidal_audiobook_search.png)

### Roon Tools

Roon Tools bündelt Live-Radio-Sender, Roon-Playlisten, Warteschlangen und frei belegbare Fernbedienungsaktionen. Pro Radiosender kann festgelegt werden, wie externe Metadaten behandelt werden.

### Fernbedienungen und externe Geräte

Zehn konfigurierbare Aktionsslots können Sender, Playlisten oder Zonenaktionen aus der Oberfläche oder über kompatible lokale Hardware starten. Unabhängige Netzwerk-Trigger verbinden den Zonenstatus mit HTTP-gesteuerten Verstärkern, Steckdosen, IR-Bridges oder Automationssystemen. Ein optionaler RoPieee-Dummy-Zonen-Proxy leitet Play, Pause, Next und Previous an die zuletzt aktive Musik- oder Hörbuchzone weiter.

### Konfiguration und Wartung

Hier werden Verbindungen, optionale Dienste, Oberfläche, Wrapped, Hörbücher, Bildanbieter, Netzwerk-Trigger, Sicherungen, Diagnosen und der Desktop-Betriebsmodus verwaltet. Im Modus Nur Server + Konfiguration lässt sich dieser Bereich lokal über den Windows-Infobereich öffnen und wird beim Schließen wieder freigegeben.

## Lokaler Betrieb

Die App ist für den Betrieb im eigenen Netzwerk ausgelegt. Roon-, Wrapped-, Hörbuch- und Cache-Daten werden lokal verwaltet. Externe Anfragen entstehen nur für aktivierte Dienste und Funktionen, beispielsweise KI-Anbieter, TIDAL oder Bild- und Metadatenanbieter. Bei Antigravity startet die lokale App die CLI auf demselben Windows-System; Google verarbeitet den übermittelten Playlistauftrag im angemeldeten Antigravity-Konto nach den jeweils aktuellen Bedingungen und Kontingenten.
