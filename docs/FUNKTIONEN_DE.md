# Funktionsübersicht

Diese Übersicht beschreibt Funktionen, die Roon AI Playlist zusätzlich zu einem normalen Roon-System bereitstellt. Die App verwendet weiterhin Roon für Bibliothek, Zonen und Wiedergabe.

## KI- und Empfehlungs-Playlisten

- freie Musikwünsche in natürlicher Sprache
- Auswahl zwischen Ollama, OpenRouter, OpenAI, Gemini und Claude
- zusätzliche Filter für Genre, Jahrzehnt, Stimmung und Sprache
- Playlist-Vorschläge aus Last.fm-Tags, gepflegten Taglisten und Wrapped Top 20
- Abgleich der Vorschläge mit der tatsächlichen Roon-Bibliothek
- sichtbare Treffer, fehlende Titel und mögliche Ersatztreffer vor dem Start
- Wiedergabe in einer gewählten Zone oder Speicherung als M3U

## Direkte TIDAL-Werkzeuge

- Suche nach Titeln, Alben und Interpreten über TIDAL
- Übernahme geeigneter TIDAL-Mixe mit eigenen Ausschlussfiltern
- feste TIDAL-Zielplaylist pro Roon-Zone
- Übernahme des laufenden Titels über die Schaltfläche `T+`
- Speichern erkannter Live-Radio-Titel in der gewählten Zielplaylist

## Erweiterter Player

- gemeinsame Übersicht mehrerer Roon-Zonen
- Detailansicht mit Cover, Metadaten, Fortschritt und Warteschlange
- Anzeige der ausstehenden Titel und gesamten Restzeit
- passende Bedienelemente für Musik, Live Radio, Spotify-Streams und Hörbücher
- Browseransicht für große Displays und entfernte Geräte
- Interpretenbilder und breite Hintergründe aus mehreren Quellen
- konfigurierbare Reihenfolge der Interpretenbild-Anbieter
- gemeinsame Künstlersuche für Duos und Gruppen vor einer möglichen Aufteilung in Einzelinterpreten

## Live Radio

- Erkennung und Reparatur vertauschter oder beschädigter Metadatenfelder
- Reparatur typischer Zeichensatzfehler bei Umlauten und Apostrophen
- Ergänzung fehlender Titel-, Interpreten-, Album- und Coverinformationen
- Suche über TIDAL, gespeicherte Treffer, MusicBrainz/Cover Art Archive, Last.fm und Deezer
- Filterung von Jingles, Werbung, Nachrichten, Intros, Outros, Senderkennungen und technischen Automationsnamen
- Schutz vor der Verwechslung von Senderlogo und Titelcover
- drei dauerhaft gespeicherte Modi pro Sender:
  - **Normal:** Anreicherung und reguläre Aufnahme in Wrapped
  - **Vorsichtig:** gleiche Suche und Anzeige wie Normal, aber keine Wrapped-Aufnahme ohne verwertbaren Treffer
  - **Aus:** keine externe Anreicherung und keine Wrapped-Aufnahme

## Cover und Interpretenbilder

- konfigurierbare Suchreihenfolge für fanart.tv, TIDAL, Roon, Last.fm, Deezer und TheAudioDB
- lokales Speichern gefundener Bilder
- bevorzugte Bilder festlegen, unpassende Treffer ablehnen oder eigene Bilder hochladen
- gezielte Neusuche für einzelne Interpreten
- automatische Ergänzung fehlender Wrapped-Alben und -Cover
- Liste weiterhin offener Cover mit Korrektur von Interpret, Titel und Album
- gezielte Neusuche oder sichere Löschung betroffener Wrapped-Einträge

## Hörbücher

- Synchronisierung als Hörbuch erkannter Roon-Alben
- vollständige Analyse auch bei sehr vielen Kapiteln
- Anzeige von Kapitelanzahl, Gesamtdauer, aktueller Position und Restzeit
- Fortsetzen, Neustart und direkte Kapitelauswahl
- manuelle und automatische Lesezeichen unabhängig von der verwendeten Zone
- optionale Ergänzung von Hörbuch-Metadaten und Cover
- Ausschluss erkannter Hörbücher aus Musik-Wrapped und Interpretenbildsuchen
- optionale Aufnahme in einer eigenen Roon-Zone mit Kapitelaufteilung und eingebetteten MP3-Metadaten

## Roon Wrapped

- lokale Erfassung qualifizierter Musik-, Live-Radio- und Spotify-Hörsitzungen
- Auswertung von Hörzeit, Quellen, Tageszeiten, Titeln, Interpreten und Alben
- Erkennung von Skips und Wiederholungen
- Dashboard, Show, Covermosaik und Story
- Jahr, Quartal, Monat, letzte 30/90 Tage, Gesamtzeitraum und freie Auswahl
- direkte Wiedergabe historischer Titel in einer Roon-Zone
- Export als PNG, PDF und CSV
- Datenqualitätsanzeige sowie Werkzeuge für fehlende Alben und Cover

## Fernsteuerung und externe Geräte

- bis zu zehn frei belegbare Roon-Aktionsfelder
- Schnellstart von Radiosendern, Playlisten und Zonenaktionen
- mehrere unabhängige Netzwerk-Trigger für Roon-Zonen
- getrennte HTTP-Befehle für EIN und AUS
- Ausschaltverzögerung nach Pause oder Stopp
- Abbruch des Ausschaltens bei erneutem Wiedergabestart
- manueller AUS-Schalter in betroffenen Zonenansichten
- optionaler Fernbedienungs-Proxy über eine eigene Roon-Dummy-Zone

## Betrieb und Wartung

- automatische und manuelle Sicherungen
- Wiederherstellung auf einem neuen System
- lokaler Bild- und Cover-Speicher mit wählbarem Speicherort
- getrennte Medienverarbeitung, damit umfangreiche Bildsuchen die Roon-Verbindung und Bedienoberfläche nicht unterbrechen
- Healthcheck, Fehlerprotokoll und Statusanzeigen
- deutsche und englische Benutzeroberfläche
