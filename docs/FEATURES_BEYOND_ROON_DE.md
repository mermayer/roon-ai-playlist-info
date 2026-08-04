# Funktionen über Roon hinaus

[English version](FEATURES_BEYOND_ROON.md) · [Zurück zur Übersicht](../README_DE.md)

Stand: Roon AI Playlist `1.0.458`, 3. August 2026.

Diese Übersicht nennt Funktionen, die **Roon AI Playlist** zusätzlich zu den Bordmitteln des originalen Roon bereitstellt. Verglichen wird mit Roon ohne weitere Extensions, Skripte oder Hausautomationssysteme. Roons Kernfunktionen wie RAAT-Wiedergabe, DSP, normale Zonensteuerung, Zonengruppierung, Bibliotheksverwaltung, Roon Radio, klassische Playlisten, TIDAL-Wiedergabe, History, Albumcover, Sleep Timer, Roon Display und Roon-Datenbankbackups werden nicht als App-Vorteil gezählt.

## 1. KI- und externe Playlist-Erzeugung

- Playlisten aus freien natürlichsprachlichen Wünschen erzeugen.
- Ollama, OpenRouter, OpenAI, Gemini oder Claude als KI-Anbieter wählen.
- Prompts mit Genre, Jahrzehnt, Stimmung und Sprache kombinieren.
- Mehrere lokale KI-Modelle im Model-Bake-off vergleichen.
- Vorschläge aus Last.fm-, Deezer- und gepflegten Taglisten erzeugen.
- Eigene gruppierte Taglisten bearbeiten und validieren.
- Kandidaten gegen die tatsächliche Roon-Bibliothek prüfen und Trefferqualität anzeigen.
- Ersatztracks für fehlende oder unsichere Kandidaten ermitteln.
- Wrapped Top 20 als Playlistquelle verwenden.
- Ergebnisse als M3U speichern, laden und prüfen.

Roon besitzt mit Valence und Roon Radio eine eigene Empfehlungslogik und verwaltet normale Playlisten, bietet aber keine frei formulierbare Multi-KI-Playlistgenerierung mit wählbarem KI-Anbieter. Siehe [Roon Valence](https://help.roonlabs.com/portal/en/kb/articles/valence) und [Roon Playlists](https://help.roonlabs.com/portal/en/kb/articles/playlists).

## 2. Direkte TIDAL-Werkzeuge

- TIDAL direkt über API V2 durchsuchen.
- Künstler-, Titel- und Albumbeziehungen getrennt auflösen.
- TIDAL-Mixe mit eigenen Ausschlussfiltern übernehmen.
- Pro Roon-Zone eine feste TIDAL-Zielplaylist konfigurieren.
- Den laufenden Titel mit `T+` direkt dieser Zielplaylist hinzufügen.
- Identifizierte Live-Radio-Titel in TIDAL speichern.
- Mix-Suchtext und Ausschlussfilter dauerhaft im App-Profil speichern.

Roons TIDAL-Ansicht ist laut Roon kein direkter Durchgriff auf den jeweils aktuellen TIDAL-Client, sondern verwendet eine regelmäßig erzeugte Roon-Datenbank. Siehe [TIDAL in Roon](https://help.roonlabs.com/portal/en/kb/articles/tidal).

## 3. Live-Radio-Metadaten und Cover

- Vertauschte Sender-, Künstler-, Titel- und Albumfelder erkennen und kanonisieren.
- Beschädigte Umlaute, Apostrophe und andere Zeichen reparieren.
- Fehlende Albumangaben anhand von Künstler und Titel ermitteln.
- Metadaten und Cover über TIDAL V2, gespeicherte Treffer, MusicBrainz/Cover Art Archive, Last.fm und Deezer ergänzen.
- Eindeutige Roon-Alben priorisieren und unpassende Compilation-, Best-of-, Soundtrack-, Live- oder Remaster-Treffer abwerten.
- Fehlerhafte Senderangaben durch sicher gefundene Künstler- und Titelnamen korrigieren.
- Jingles, Werbung, Nachrichten, Intros, Outros, Senderkennungen und technische Automationsnamen vor der Providersuche erkennen.
- Trackcover vom Roon-Senderlogo unterscheiden und lokal sichern.
- Pro Sender den Modus `Normal`, `Vorsichtig` oder `Aus` dauerhaft speichern und als `N`, `V` oder `A` anzeigen.
- Im vorsichtigen Modus unsichere Ergebnisse nur aus Wrapped ausschließen, ohne Suche und Anzeige einzuschränken.

Roon dokumentiert, dass es bei Live Radio grundsätzlich nur Metadaten verwenden kann, die im Audiostream enthalten sind. Siehe [Live Radio in Roon](https://help.roonlabs.com/portal/en/kb/articles/live-radio).

## 4. Cover- und Interpretenbildverwaltung

- Die Suchreihenfolge von fanart.tv, TIDAL, Roon, Last.fm, Deezer und TheAudioDB frei konfigurieren.
- Einzelne Anbieter ausschließlich für Interpretenbilder deaktivieren.
- Profilbilder und breite Künstlerhintergründe getrennt verwalten.
- Bilder lokal spiegeln, per Inhalts-Hash deduplizieren und ihre Quelle anzeigen.
- Mehrfachinterpreten zuerst als gemeinsame Identität suchen und erst ohne Gesamttreffer auf einzelne Beteiligte zurückfallen.
- Mehrere Künstlerbilder als koordinierte Slideshow anzeigen.
- Treffer interpretenbezogen ablehnen, bevorzugte Bilder festlegen oder eigene Bilder hochladen.
- Eine gezielte Neusuche für einen Künstler starten.
- Fehlende Wrapped-Alben und Cover automatisch nachfüllen und externe Bilder lokal speichern.
- Offene Cover gruppiert verwalten, Metadaten korrigieren, einzeln neu suchen oder bestätigte Wrapped-Wiedergaben sicher löschen.

Roon kann Bibliotheksalben identifizieren und eigene Albumcover übernehmen, besitzt aber keine frei sortierbare externe Providerkette und keinen vergleichbaren Wrapped-Reparaturablauf. Siehe [Albumidentifikation](https://help.roonlabs.com/portal/en/kb/articles/identifying-albums) und [Albumcover ändern](https://help.roonlabs.com/portal/en/kb/articles/faq-how-do-i-change-the-cover-art-of-an-album).

## 5. Hörbuchverwaltung und Aufnahme

- Roon-Alben als Hörbücher synchronisieren und auch bei mehreren hundert Kapiteln vollständig analysieren.
- Kapitelanzahl, Gesamtdauer und lokalen Hörfortschritt verwalten.
- Hörbücher fortsetzen, neu starten oder kapitelweise abspielen.
- Manuelle und automatische, zonenunabhängige Lesezeichen speichern.
- Audible-Metadaten und Cover ergänzen.
- Hörbücher und Autoren zuverlässig von Wrapped und Musik-Interpretenbildsuchen ausschließen.
- Ein bekanntes Hörbuch automatisch in einer exklusiven lokalen Roon-Aufnahmezone starten.
- Vorher FFmpeg, FFprobe, `libmp3lame`, VB-CABLE, Roon-Zone, Zielordner und Speicherplatz prüfen.
- Das Buch in einem separaten überwachten Prozess als durchgehende Mastersegmente aufnehmen.
- Beobachtete Roon-Kapitelwechsel anschließend in nummerierte MP3-Kapitel mit 192 kbit/s CBR aufteilen.
- Titel, Autor, Album, Tracknummer und Frontcover in die Kapiteldateien schreiben.
- Eine Pause am Ende des aktuellen Kapitels vormerken, zurücknehmen und beim nächsten Kapitel fortsetzen.
- Aufnahme- und Verarbeitungfortschritt, Restzeit, Prozesszustand und Fehler anzeigen.
- Mastersegmente bei einem Fehler als sichtbare Rettungsdateien erhalten.

## 6. Roon Wrapped

- Qualifizierte Hörsitzungen aus Roon, Live Radio und Spotify-Streams lokal aufzeichnen.
- Fehlstarts, Skips und Replays unterscheiden.
- Hörzeit nach Tageszeit und Quelle sowie Top-Titel, -Interpreten und -Alben auswerten.
- Dashboard, Show, Covermosaik und automatisch ablaufende Story darstellen.
- Jahr, Quartal, Monat, Rolling 30/90, Gesamt oder freie Zeiträume filtern.
- Historische Titel aus der Auswertung direkt in einer gewählten Roon-Zone starten.
- Datenqualität, Coverabdeckung und fehlende Metadaten sichtbar machen.
- Ergebnisse als PNG, PDF und CSV exportieren und eine Exporthistorie führen.
- Historische Metadaten, Alben und Cover automatisch vervollständigen.
- Wrapped-Sessions primär in SQLite und zusätzlich als portablen JSON-Snapshot sichern.

Roon speichert Wiedergabeverlauf und Play Counts, bietet aber nicht diese eigenständige Story-, Export- und Reparaturumgebung. Siehe [In Roon-Backups gespeicherte Daten](https://help.roonlabs.com/portal/en/kb/articles/what-is-a-backup-in-roon).

## 7. Externe Geräte- und Hausautomationssteuerung

- Mehrere unabhängige Netzwerk-Trigger mit jeweils einer oder mehreren Roon-Zonen konfigurieren.
- Frei definierbare HTTP- oder HTTPS-Befehle für `EIN` und `AUS` senden.
- Trigger nur mit EIN, nur mit AUS oder mit beiden Richtungen betreiben.
- Externe Verstärker, Steckdosen, IR-Bridges oder Hausautomationsaktoren beim Wiedergabestart einschalten.
- Nach Pause oder Stopp einen Ausschalt-Timer von 15 Minuten bis acht Stunden starten.
- Den Timer bei erneuter Wiedergabe abbrechen und bei fehlenden Zonen sicher keinen AUS-Befehl senden.
- Countdown, Zustand, letzten Befehl, Laufzeit und Erfolg anzeigen und beide Richtungen separat testen.
- Einen laufenden Scheduler mit dem manuellen AUS-Button überschreiben, die Roon-Zone stoppen und alle zugeordneten Geräte sofort ausschalten.

Roons Sleep Timer beendet beziehungsweise blendet lediglich die Wiedergabe der Zone aus und sendet keine frei definierbaren Netzwerkbefehle. Siehe [Roon Sleep Timer](https://help.roonlabs.com/portal/en/kb/articles/sleep-timer).

## 8. Externe Fernbedienungen und Remote-Slots

- Bis zu zehn Schnellzugriffsslots für Live Radio, Roon-Playlisten und Zonenaktionen konfigurieren.
- Slots in der App oder über eine geschützte HTTP-API durch ESP32-, IR- oder andere lokale Controller auslösen.
- Eine Dummy-Roon-Zone als Bluetooth-Fernbedienungsproxy verwenden.
- Play, Pause, Next und Previous an die zuletzt aktive Musik- oder Hörbuchzone weiterleiten.
- Markerbewegungen, natürliches Titelende und Rückkopplungen unterscheiden.
- Zielzone, Marker, letzten Befehl und Bestätigungsverzögerung anzeigen.

## 9. Player, Browser und Viewer

![Übersicht des Mehrzonen-Players](../assets/screenshots/new_zone_view.png)

- Alle relevanten Roon-Zonen gleichzeitig als Dashboard mit Cover, Zustand, Fortschritt, Transport und Queue darstellen.
- Bis zu sechs kommende Titel sowie Restanzahl und Restzeit direkt pro Zone anzeigen.
- Eigene Darstellungen für normale Musik, Roon Radio, Live Radio, Spotify und Hörbücher verwenden.
- Cover, Künstlerprofilbild und Künstlerhintergrund getrennt präsentieren.
- Eine vollständige Bedienoberfläche in einem normalen LAN-Browser bereitstellen.
- Den schlanken Windows-Viewer mit WebView2, Tray, Autostart, Zoom und per DPAPI geschütztem Token einsetzen.

Roons Web Display zeigt Now Playing und Liedtexte im Browser, ist aber keine vollständige Browser-Fernbedienung mit diesen App-Werkzeugen. Siehe [Roon Displays](https://help.roonlabs.com/portal/en/kb/articles/displays).

## 10. Wartung und Transparenz

- Kombinierte Client-, Server- und Providerfehler anzeigen und als CSV exportieren.
- Verbindung und Konfiguration der einzelnen Dienste gezielt prüfen.
- App-Paket, SQLite-/JSON-Konsistenz, Caches und Speicherstatus prüfen.
- App-Konfiguration, Tokens, Wrapped, Hörbücher, Trigger und Metadaten gemeinsam sichern und wiederherstellen.
- Bild- und Coverspeicher verifiziert auf ein anderes Laufwerk verschieben.
- Ereignisschleifenverzögerung, Serverlaufzeit, Workerzustand, Auftragszahlen, Fehler und Neustarts diagnostizieren.
- Providerabfragen, Downloads, Hashing und Bildspeicherung in einem separaten überwachten Medienprozess ausführen.

## Abgrenzung

Die App ersetzt Roon nicht. Roon bleibt für Musikbibliothek, Streaming, Audioausgabe, RAAT, DSP, Zonen, Queue und Transport zuständig. Roon AI Playlist nutzt die Roon-Extension-APIs und ergänzt darauf aufbauend die oben beschriebenen Workflows.
