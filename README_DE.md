# Roon AI Playlist

**Eine lokale Roon-Erweiterung für intelligente Playlisten, bessere Live-Radio-Metadaten, visuelle Mehrzonensteuerung, Hörbuchfunktionen, persönliche Hörstatistiken, Bildverwaltung und Hausautomationsaktionen.**

[English version – default](README.md)

> Roon AI Playlist ist ein unabhängiges Projekt und steht in keiner Verbindung zu Roon Labs, TIDAL, Last.fm, Deezer, fanart.tv, Audible oder den unterstützten KI-Anbietern.

## Aktuelle Versionen

- Roon AI Playlist: **1.0.458**
- RoonAIViewer: **1.0.3**

## Was ist Roon AI Playlist?

Roon AI Playlist richtet sich an Menschen, die Roon bereits verwenden und mehr Kontrolle über Musikentdeckung, Darstellung, Hörhistorie, Live Radio, Hörbücher und angeschlossene Geräte wünschen.

Roon bleibt für Musikbibliothek, Streaming, RAAT, DSP, Zonen, Warteschlangen und Audiowiedergabe zuständig. Roon AI Playlist verbindet sich mit diesem vorhandenen System und ergänzt Arbeitsabläufe, die Roon selbst nicht bereitstellt.

Die Anwendung läuft lokal und lässt sich auf drei Arten bedienen:

- als vollständige Windows-App auf dem Serverrechner,
- über einen normalen Browser im privaten Netzwerk,
- über den schlanken Windows-Client **RoonAIViewer** auf einem anderen Rechner oder Display.

## Was ergänzt die App zu Roon?

### Intelligente Playlist-Erzeugung

- Musikwünsche frei in natürlicher Sprache beschreiben.
- Ollama, OpenRouter, OpenAI, Gemini oder Claude als KI-Anbieter wählen.
- Wünsche mit Genre, Jahrzehnt, Stimmung, Energie und Sprache kombinieren.
- Playlisten aus Last.fm, Deezer, gepflegten Taglisten oder Wrapped-Favoriten erzeugen.
- Jeden Vorschlag vor der Wiedergabe mit der tatsächlichen Roon-Bibliothek abgleichen.
- Treffer, unsichere Ergebnisse, fehlende Titel und mögliche Alternativen anzeigen.
- Ergebnis in einer gewählten Roon-Zone starten oder als M3U speichern.

### Bessere Live-Radio-Metadaten

Live-Radio-Streams liefern häufig unvollständige, vertauschte oder falsch codierte Texte. Roon AI Playlist kann:

- Sendername, Interpret, Titel und Album voneinander unterscheiden,
- typische Zeichensatzfehler bei Umlauten und Apostrophen reparieren,
- fehlende Alben und Cover über mehrere Metadatenanbieter ermitteln,
- falsche Künstler- oder Titelangaben durch sichere Treffer korrigieren,
- Senderlogo und echtes Titelcover voneinander unterscheiden,
- Künstlerporträts und breite Fanart-Hintergründe laden,
- Jingles, Werbung, Nachrichten, Intros, Outros, Senderkennungen und Automationsnamen filtern,
- erkannte Titel über `T+` in einer konfigurierten TIDAL-Playlist speichern.

Jeder Sender besitzt einen dauerhaft gespeicherten Metadatenmodus:

- **Normal:** Darstellung anreichern und Musik in Wrapped aufnehmen.
- **Vorsichtig:** identische Suche und Darstellung, aber nur mit verwertbarem Providertreffer in Wrapped aufnehmen.
- **Aus:** nur die Senderinformationen anzeigen und nicht in Wrapped aufnehmen.

![Aufbereitete Live-Radio-Metadaten mit Cover und Interpretenbildern](assets/screenshots/radio_new.png)

### Visueller Mehrzonen-Player

![Übersicht des Mehrzonen-Players](assets/screenshots/new_zone_view.png)

- Alle relevanten Roon-Zonen gemeinsam in einem Dashboard darstellen.
- Cover, Wiedergabestatus, Fortschritt, Transportsteuerung und Warteschlange anzeigen.
- Kommende Titel, verbleibende Titelanzahl und gesamte Restzeit anzeigen.
- Eigene Ansichten für normale Musik, Roon Radio, Live Radio, Spotify-Streams und Hörbücher verwenden.
- Albumcover, Künstlerporträt und Künstlerhintergrund getrennt darstellen.
- Browser- und Viewer-Anzeigen bei kurzen Roon-Neuverbindungen stabil halten.
- Den aktuellen Titel direkt einer zonenbezogenen TIDAL-Zielplaylist hinzufügen.

![Zonendetail mit Warteschlange und Interpretenbild](assets/screenshots/player.png)

### Hörbücher innerhalb der Roon-Umgebung

- Als Hörbuch erkannte Roon-Alben synchronisieren.
- Bücher mit mehreren hundert Kapiteln vollständig analysieren.
- Kapitelanzahl, Gesamtdauer, aktuelle Position und Restzeit anzeigen.
- Buch fortsetzen, neu beginnen oder ein Kapitel direkt auswählen.
- Manuelle und automatische Lesezeichen unabhängig von der Wiedergabezone speichern.
- Erkannte Hörbücher und Autoren aus Musik-Wrapped und Interpretenbildsuchen ausschließen.
- Hörbuch-Metadaten und Cover optional ergänzen.
- Hörbücher optional über eine eigene lokale Roon-Zone aufnehmen und nummerierte MP3-Kapiteldateien mit Metadaten und Cover erzeugen.

![Hörbuchplayer mit Kapiteln und Lesezeichen](assets/screenshots/audiobooks.png)

### Persönliches Roon Wrapped

- Qualifizierte Hörsitzungen aus normaler Roon-Wiedergabe, Live Radio und Spotify-Streams lokal erfassen.
- Hörzeit, Quellen, Tageszeiten, Top-Titel, Top-Interpreten und Top-Alben auswerten.
- Kurze Fehlstarts, Skips und Wiederholungen unterscheiden.
- Dashboard, Show, Covermosaik und automatisch ablaufende Story öffnen.
- Jahr, Quartal, Monat, letzte 30/90 Tage, Gesamtzeitraum oder freie Zeitspanne wählen.
- Historische Titel direkt in einer ausgewählten Roon-Zone starten.
- Ergebnisse als PNG, PDF oder CSV exportieren.
- Datenqualität prüfen und fehlende Alben oder Cover nacharbeiten.

![Persönliche Roon-Wrapped-Show](assets/screenshots/wrapped.png)

### Cover- und Interpretenbildverwaltung

- fanart.tv, TIDAL, Roon, Last.fm, Deezer und TheAudioDB für Interpretenbilder frei sortieren.
- Einzelne Bildanbieter deaktivieren.
- Gemeinsame Künstlernamen und Duos suchen, bevor einzelne Beteiligte geprüft werden.
- Porträts und breite Künstlerhintergründe getrennt verwalten.
- Bevorzugte Bilder festlegen, unpassende Treffer für einen Künstler ablehnen oder eigene Bilder hochladen.
- Gefundene Bilder lokal speichern und doppelte Dateien vermeiden.
- Offene Wrapped-Cover finden, Interpret/Titel/Album korrigieren und nur den betroffenen Eintrag erneut suchen.
- Fehlende Wrapped-Alben, Cover und lokale Bildkopien in einem gemeinsamen Ablauf vervollständigen.

### Direkte TIDAL-Werkzeuge

- TIDAL direkt nach Interpreten, Titeln und Alben durchsuchen.
- Geeignete TIDAL-Mixe mit eigenen Ausschlussregeln übernehmen.
- Pro Roon-Zone eine feste TIDAL-Zielplaylist konfigurieren.
- Den laufenden Titel oder einen erkannten Live-Radio-Titel über `T+` hinzufügen.
- Mix-Suchtext und Filter im lokalen App-Profil speichern.

### Fernbedienung und externe Geräte

- Bis zu zehn Schnellzugriffe für Live-Radio-Sender, Roon-Playlisten und Zonenaktionen konfigurieren.
- Mehrere unabhängige Netzwerk-Trigger für eine oder mehrere Roon-Zonen definieren.
- Getrennte HTTP- oder HTTPS-Befehle beim Wiedergabestart und nach Wiedergabeende senden.
- Verstärker, Steckdosen, IR-Bridges oder Hausautomationsgeräte steuern.
- Ausschalten nach Pause oder Stopp planen und bei erneuter Wiedergabe automatisch abbrechen.
- Mit einem manuellen AUS-Schalter die Zone stoppen, den Scheduler beenden und zugeordnete Geräte sofort ausschalten.
- Optional eine eigene Roon-Dummy-Zone als Bluetooth-Fernbedienungsproxy für Play, Pause, Next und Previous verwenden.

### Wartung und Stabilität

- Vollständige App-Sicherungen erstellen und wiederherstellen.
- Wrapped-Sitzungen primär in SQLite und zusätzlich als portablen Sicherungsstand speichern.
- Den Bildspeicher geprüft auf ein anderes lokales Laufwerk verschieben.
- Dienstestatus, Speicher, Caches, Providerfehler und Roon-Verbindung kontrollieren.
- Umfangreiche Metadatenabfragen, Bilddownloads, Prüfung, Hashing und Cache-Arbeiten getrennt ausführen, damit Player, Weboberfläche, Roon-Verbindung und Netzwerk-Trigger ansprechbar bleiben.

## Playlist-Beispiel

![Mit Roon abgeglichene KI-Playlist](assets/screenshots/playlist.png)

## RoonAIViewer

RoonAIViewer ist ein eigener 64-Bit-Windows-Client für eine Roon-AI-Playlist-Installation auf einem anderen Rechner. Er stellt die vollständige Oberfläche in einem eigenen Fenster bereit, ohne einen weiteren App-Dienst zu starten oder eine zusätzliche Roon-Verbindung aufzubauen.

Zu den Viewer-Funktionen gehören:

- Betrieb im Windows-Infobereich,
- optionaler Autostart und minimierter Start,
- dauerhaft gespeicherter Oberflächenzoom von 90 bis 130 Prozent,
- native Prüfung von Server und Token,
- Schutz des API-Tokens durch Windows DPAPI für den aktuellen Benutzer,
- vollständiges Neuladen über Tray-Menü, `F5` oder `Strg+R`,
- automatische Wiederherstellung bei einer fälschlich offline angezeigten Webseite,
- optionale Entfernung von Einstellungen und Browserdaten bei der Deinstallation.

Siehe [vollständiges RoonAIViewer-Benutzerhandbuch](docs/ROONAI_VIEWER_DE.md).

## Voraussetzungen

Für den normalen Windows-Betrieb:

- Windows 10 oder Windows 11, 64 Bit,
- ein erreichbarer Roon Core im lokalen Netzwerk,
- Autorisierung der Erweiterung unter **Roon > Einstellungen > Erweiterungen**.

Die KI-Playlistfunktion ist optional und kann deaktiviert werden. Zu den optionalen Integrationen gehören TIDAL, Last.fm, Deezer, fanart.tv, MusicBrainz/Cover Art Archive, TheAudioDB, Audible und ein unterstützter KI-Anbieter.

## Lokale Daten und Netzwerkzugriff

Die Anwendung ist für ein vertrauenswürdiges privates Netzwerk vorgesehen. Hörhistorie, Hörbuchinformationen, Konfiguration, Protokolle und zwischengespeicherte Bilder liegen auf dem App-System. Externe Anfragen entstehen nur für aktivierte Dienste und Funktionen.

Browser- und RoonAIViewer-Zugriff sollten mit einem API-Token geschützt werden. App-Sicherungen können Zugangsdaten und persönliche Hörhistorien enthalten und müssen sicher aufbewahrt werden.

## Dokumentation

- [Vollständiges Benutzerhandbuch](docs/BENUTZERHANDBUCH_DE.md)
- [Funktionen über Roon hinaus](docs/FEATURES_BEYOND_ROON_DE.md)
- [App-Überblick](docs/APP_UEBERBLICK_DE.md)
- [Erste Schritte](docs/ERSTE_SCHRITTE_DE.md)
- [RoonAIViewer-Benutzerhandbuch](docs/ROONAI_VIEWER_DE.md)
- [Datenschutz und Sicherheit](docs/DATENSCHUTZ_UND_SICHERHEIT_DE.md)
- [Häufige Fragen](docs/FAQ_DE.md)
- [Versionshinweise](docs/VERSIONSHINWEISE_DE.md)
- [English documentation](README.md)

## Verfügbarkeit

Dieses Informations-Repository enthält keine Installationsdateien und keinen Quellcode. Roon AI Playlist und RoonAIViewer werden getrennt bereitgestellt.
