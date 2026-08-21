# Funktionen über Roon hinaus

[English version](FEATURES_BEYOND_ROON.md) · [Zurück zur Übersicht](../README_DE.md)

Stand: Roon AI Playlist `1.0.549`, 21. August 2026.

Diese Übersicht nennt Funktionen, die **Roon AI Playlist** zusätzlich zu den Bordmitteln des originalen Roon bereitstellt. Sie beschreibt keinen Ersatz für die Roon-Oberfläche oder irgendeine Roon-Funktion. Die Begleitanwendung soll ausschließlich außerhalb von Roon nützliche, dort fehlende Arbeitsabläufe ermöglichen – so weit es die Roon-Extension-APIs zulassen. Verglichen wird mit Roon ohne weitere Extensions, Skripte oder Hausautomationssysteme. Roons Kernfunktionen wie RAAT-Wiedergabe, DSP, normale Zonensteuerung, Zonengruppierung, Bibliotheksverwaltung, Roon Radio, klassische Playlisten, TIDAL-Wiedergabe, History, Albumcover, Sleep Timer, Roon Display und Roon-Datenbankbackups werden nicht als App-Vorteil gezählt.

## 1. KI- und externe Playlist-Erzeugung

![KI-Playlist-Filter und gegen Roon geprüftes Ergebnis](../assets/screenshots/playlist.png)

- Playlisten aus freien natürlichsprachlichen Wünschen erzeugen.
- Ollama, OpenRouter, OpenAI, Gemini, Claude, die geführte ChatGPT-Work-Übergabe oder die vollautomatische Google Antigravity CLI wählen.
- Aktuelle hochwertige Antigravity-Modelle ohne KI-API-Key oder nutzungsabhängiges API-Konto verwenden; es gelten Googles kostenloser Tarif und dessen Kontingente.
- Gemini-Denktiefen aus einer echten Auswahlliste wählen, kontospezifische Modelle über `agy models` laden oder eine zukünftige Modell-ID frei eintragen.
- Prompts mit Genre, Jahrzehnt, Stimmung und Sprache kombinieren.
- Mehrere lokale KI-Modelle im Model-Bake-off vergleichen.
- Vorschläge aus Last.fm-, Deezer- und gepflegten Taglisten erzeugen.
- Eigene gruppierte Taglisten bearbeiten und validieren.
- Kandidaten gegen die tatsächliche Roon-Bibliothek prüfen und Trefferqualität anzeigen.
- Ersatztracks für fehlende oder unsichere Kandidaten ermitteln.
- Eine konkrete Aufnahme aus `Wrapped > Titel` zum festen Ausgangstitel einer normalen, vollständig bearbeitbaren KI-Playlist machen.
- Diese Aufnahme ohne Last.fm nach engem Genre/Subgenre, tatsächlich gesungener Sprache, Stil, Instrumentierung/Klangbild, Epoche/Produktion, Gesangscharakter und Energie profilieren.
- Das sichtbare Profil verbindlich anwenden und bei automatischen Anbietern jeden Vorschlag vor der Anzeige unabhängig prüfen.
- Den Ausgangstitel genau einmal vorne halten und das endliche Ergebnis anschließend prüfen, ersetzen, umsortieren, speichern, einreihen oder in einer gewählten Roon-Zone wiedergeben.
- Wrapped Top 20 als Playlistquelle verwenden.
- Ergebnisse als M3U speichern, laden und prüfen.

Die KI-Erzeugung bleibt eine Vorschlagsstufe: Gewähltes Modell, strukturierte Filter und optionaler Freitext liefern Kandidaten, während die App jeden Roon-Treffer vor der Wiedergabe sichtbar macht. Einzelne Einträge lassen sich probeweise starten, ersetzen, entfernen oder anhängen; das vollständige geprüfte Ergebnis kann eine Zonen-Queue starten oder erweitern. Im Antigravity-Modus läuft dieser gesamte Weg nach der einmaligen Google-Anmeldung automatisch: Es müssen weder Prompts kopiert noch API-Keys hinterlegt werden. Die App kauft keine Credits und blockiert bereits aktivierte kostenpflichtige G1-/AI-Credits, solange der Benutzer sie nicht ausdrücklich erlaubt.

![Last.fm-Tagauswahl und abgeglichene Top-Titel](../assets/screenshots/lastfm.png)

Last.fm-Playlisten verwenden gepflegte Jahrzehnt-, Sprach-, Genre-, Stil- und Atmosphäre-Tags und benötigen keinen KI-Prompt. Mehrere Tags lassen sich kombinieren; die populären Kandidaten durchlaufen anschließend exakt denselben sichtbaren Roon-Abgleich und Bearbeitungsablauf.

Roon Radio bleibt die bequeme Wahl für eine mühelose, fortlaufende Entdeckungswiedergabe. Der Wrapped-Ausgangstitel dient stattdessen der bewussten Kuratierung: Exakte Aufnahme und Vorgaben sind sichtbar, Genre und Gesangssprache gelten schon vor der Wiedergabe verbindlich und die endliche Liste lässt sich prüfen, bearbeiten, speichern und reproduzieren. Roon besitzt mit Valence und Roon Radio eine eigene Empfehlungslogik und verwaltet normale Playlisten, bietet aber keinen solchen vorab geprüften Multi-KI-Playlistablauf. Siehe [Roon Valence](https://help.roonlabs.com/portal/en/kb/articles/valence) und [Roon Playlists](https://help.roonlabs.com/portal/en/kb/articles/playlists).

## 2. Direkte TIDAL-Werkzeuge

![Browser für persönliche TIDAL-Mixe und Radios](../assets/screenshots/personal_radio.png)

- TIDAL direkt über API V2 durchsuchen.
- Künstler-, Titel- und Albumbeziehungen getrennt auflösen.
- TIDAL-Mixe mit eigenen Ausschlussfiltern übernehmen.
- Pro Roon-Zone eine feste TIDAL-Zielplaylist konfigurieren.
- Den laufenden Titel mit `T+` direkt dieser Zielplaylist hinzufügen.
- Identifizierte Live-Radio-Titel in TIDAL speichern.
- Mix-Suchtext und Ausschlussfilter dauerhaft im App-Profil speichern.

Persönliche Entdeckung beschränkt sich nicht auf eine Textsuche. My Daily Discovery, nummerierte My Mixes, New Arrivals, Titelradio und Interpretenradio lassen sich gemeinsam prüfen, in einer ausgewählten Roon-Zone starten oder anhängen und gezielt in beständige TIDAL-Playlisten synchronisieren. Videos und Radiokategorien können von dieser Synchronisierung ausgeschlossen werden.

![Browser für redaktionelle und eigene TIDAL-Playlisten](../assets/screenshots/tidal_pl.png)

Die Playlist-Ansicht kombiniert Freitext mit Jahrzehnt-, Genre-, Stimmungs-, Themen- und Herkunftsfiltern. Eine Vorschau zeigt die ersten Titel, bevor eine Playlist die Roon-Queue ersetzt oder erweitert.

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

![Hörbuchkatalog von Audible und DNB](../assets/screenshots/audible.png)

- Roon-Alben als Hörbücher synchronisieren und auch bei mehreren hundert Kapiteln vollständig analysieren.
- Kapitelanzahl, Gesamtdauer und lokalen Hörfortschritt verwalten.
- Hörbücher fortsetzen, neu starten oder kapitelweise abspielen.
- Manuelle und automatische, zonenunabhängige Lesezeichen speichern.
- Audible-Metadaten und Cover ergänzen.
- Hörbücher und Autoren zuverlässig von Wrapped und Musik-Interpretenbildsuchen ausschließen.
- TIDAL-Hörbücher eigenständig nach Titel oder Interpret suchen, Cover und Albumdaten aufbereiten und bis zu 200 Treffer einschließlich **Älteste zuerst** sortieren.
- TIDAL-Titel ohne Audioimport in einer getrennten virtuellen Merkliste verwalten.
- Ein TIDAL-Hörbuch über Roon Audio Input oder einen gewählten Windows-/USB-Bluetooth-Ausgang wiedergeben.
- Geschwindigkeit von 1,00× bis 2,00× und Pitch von 0,50 bis 1,50 unabhängig in 0,05-Schritten einstellen.
- Auf Sprache abgestimmte Rubber-Band-Tonhöhenverarbeitung sowie AVRCP Play/Pause kompatibler Bluetooth-Hörer bei Windows-Ausgabe verwenden.
- TIDAL-Kapitel, Hörfortschritt, Autolesezeichen und benannte manuelle Lesezeichen verwalten.
- Ein bekanntes Hörbuch automatisch in einer exklusiven lokalen Roon-Aufnahmezone starten.
- Die TIDAL-Schnellaufnahme direkt aus einem Suchtreffer starten und bevorzugt ein geprüftes 4×-Profil mit 2×-Fallback verwenden.
- Eine vollständige Aufnahmestatusseite mit Kapitel, Laufzeit, Restzeit, Profil, Ziel, Pause, Fortsetzen und Abbruch anzeigen.
- Weitere TIDAL-Wiedergabe der App und im verwalteten Chrome während einer laufenden Aufnahme sperren.
- Vorher FFmpeg, FFprobe, `libmp3lame`, VB-CABLE, Roon-Zone, Zielordner und Speicherplatz prüfen.
- Das Buch in einem separaten überwachten Prozess als durchgehende Mastersegmente aufnehmen.
- Beobachtete Roon-Kapitelwechsel anschließend in nummerierte MP3-Kapitel mit 192 kbit/s CBR aufteilen.
- Titel, Autor, Album, Tracknummer und Frontcover in die Kapiteldateien schreiben.
- Eine Pause am Ende des aktuellen Kapitels vormerken, zurücknehmen und beim nächsten Kapitel fortsetzen.
- Aufnahme- und Verarbeitungfortschritt, Restzeit, Prozesszustand und Fehler anzeigen.
- Mastersegmente bei einem Fehler als sichtbare Rettungsdateien erhalten.

Der Entdeckungskatalog lässt sich nach Autor, Titel, Suchwort, Genre, Jahr und Quelle filtern und kann Sprecher, Laufzeit, Bewertung, Hörprobe sowie Quellverweise zeigen. Ein Katalogtreffer kann anschließend eine eigene TIDAL-Suche öffnen, statt seine Verfügbarkeit dort vorauszusetzen. Die Titelsuche folgt zusätzlich plausiblen Serieninterpreten; auch nach einem leeren ersten Ergebnis bleibt die Interpretensuche verfügbar.

![Aufbereitete TIDAL-Hörbuchtreffer](../assets/screenshots/tidal_audiobook_search.png)

TIDAL-Albumkandidaten erscheinen mit Cover, Interpret, Jahr, Laufzeit und Kapitelzahl. **Album hinzufügen**, **Später anhören** und **Schnellaufnahme** bleiben getrennte Aktionen. Beim direkten Anhören verwaltet die virtuelle Bibliothek den Hörbuchzustand, während das Originalaudio bei TIDAL verbleibt.

![Direkte TIDAL-Hörbuchwiedergabe](../assets/screenshots/tidal_audiobook.png)

Play/Pause direkt in der App ist der verlässliche Pausenweg. Roon Previous/Next kann Kapitel wechseln; nach dem Stoppen eines Live-Audio-Input-Stroms entfernen einzelne Roon-Clients jedoch ihre fortsetzbare Play-Aktion. Diese clientabhängige Einschränkung wird deshalb nicht als vollständige Roon-Transportsteuerung beworben.

## 6. Roon Wrapped

![Filterbare titelgenaue Wrapped-Historie](../assets/screenshots/tracks.png)

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

Die Tracks-Ansicht hält die Auswertung überprüfbar: Zu jeder gezählten Wiedergabe bleiben Titel, Interpret, Album, Zeitpunkt, Quelle, Sender, Cover und effektive Hörzeit sichtbar. Datums- und Quellenfilter können Roon, Live Radio oder Spotify isolieren; ein historischer Eintrag lässt sich auflösen und erneut in einer gewählten Roon-Zone starten.

Roon speichert Wiedergabeverlauf und Play Counts, bietet aber nicht diese eigenständige Story-, Export- und Reparaturumgebung. Siehe [In Roon-Backups gespeicherte Daten](https://help.roonlabs.com/portal/en/kb/articles/what-is-a-backup-in-roon).

## 7. Externe Geräte- und Hausautomationssteuerung

![Unabhängige Netzwerk-Trigger mit Live-Status und Ausschalt-Timern](../assets/screenshots/remote_trigger_2.png)

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

![Zehn konfigurierbare IR- und WLAN-Aktionsslots](../assets/screenshots/remote_v2.png)

- Bis zu zehn Schnellzugriffsslots für Live Radio, Roon-Playlisten und Zonenaktionen konfigurieren.
- Slots in der App oder über eine geschützte HTTP-API durch ESP32-, IR- oder andere lokale Controller auslösen.
- Eine Dummy-Roon-Zone als Bluetooth-Fernbedienungsproxy verwenden.
- Play, Pause, Next und Previous an die zuletzt aktive Musik- oder Hörbuchzone weiterleiten.
- Markerbewegungen, natürliches Titelende und Rückkopplungen unterscheiden.
- Zielzone, Marker, letzten Befehl und Bestätigungsverzögerung anzeigen.

Die zehn nummerierten Slots und der Dummy-Zonen-Proxy lösen unterschiedliche Aufgaben. Slots stellen eindeutige Aktionen in der Oberfläche oder an einem geschützten lokalen HTTP-Endpunkt bereit. Der Proxy übersetzt die Transportereignisse einer ferngesteuerten stummen Roon-Zone in Aktionen für die zuletzt aktive konfigurierte Musik- oder Hörbuchzone.

![Konfiguration und Status des RoPieee-Dummy-Zonen-Proxys](../assets/screenshots/ropieee_remote.png)

Damit kann eine mit RoPieee verbundene Bluetooth-Fernbedienung zwischen zwei wechselnden Zielen verwendet werden, ohne eigene Software auf RoPieee zu installieren. Drei Markertitel codieren die Navigation; Prüfung, Rückkopplungsunterdrückung, Zielspeicherung und gemessene Bestätigung übernimmt die Begleitanwendung. Lautstärke und Mute gehören nicht zu diesem Proxy.

## 9. Player, Browser und Viewer

![Übersicht des Mehrzonen-Players](../assets/screenshots/new_zone_view.png)

- Konfigurieren, welche Roon-Zonen sichtbar sind, ihre Reihenfolge und Spaltendarstellung bestimmen und die ausgewählten Zonen gleichzeitig mit Cover, Zustand, Fortschritt, Transport und Queue anzeigen.
- Bis zu sechs kommende Titel sowie Restanzahl und Restzeit direkt pro Zone anzeigen.
- Eigene Darstellungen für normale Musik, Roon Radio, Live Radio, Spotify und Hörbücher verwenden.
- Cover, Künstlerprofilbild und Künstlerhintergrund getrennt präsentieren.
- Eine vollständige Bedienoberfläche in einem normalen LAN-Browser bereitstellen.
- Den schlanken Windows-Viewer mit WebView2, Tray, Autostart, Zoom und per DPAPI geschütztem Token einsetzen.
- Den zentralen App-Dienst bei entfernter Bedienung im Modus Nur Server + Konfiguration installieren und sämtliche Hintergrundfunktionen ohne dauerhaft geladenes lokales Playerfenster bereitstellen.

Der Betriebsmodus ist während der Windows-Installation wählbar und kann später in der Konfiguration geändert werden. Im Servermodus bleiben Roon-Steuerung, Wrapped-Aufzeichnung, Netzwerk-Trigger, Medienverarbeitung, geplante Aufgaben und Hörbuchaufnahme verfügbar. Das lokale Konfigurationsfenster wird nur bei Bedarf geöffnet und nach dem Schließen freigegeben, während Browser und RoonAIViewer weiterhin die vollständige Oberfläche erhalten.

![Spotify-Wiedergabe in der eigenen Zonendarstellung](../assets/screenshots/spotify_pl.png)

Spotify und andere externe Wiedergaben werden nur dargestellt, wenn sie die App über Roon erreichen. Die Begleitanwendung wird nicht selbst zum Spotify-Client; sie passt die Anzeige an die gelieferten Streamdaten an und erfasst qualifizierte Spotify-Sitzungen als eigene Wrapped-Quelle.

Die eigenständige native macOS-App SpotBridge kann diesen Weg für lokale Spotify-Wiedergabe bereitstellen. Sie nimmt den Spotify-Prozess über einen CoreAudio Process Tap auf, übergibt das erfasste Signal als AAC oder verlustfrei codiertes Ogg-FLAC an Roon Audio Input, übermittelt Interpret, Titel, Album und Cover und kann Transportereignisse von Spotify und Roon koordinieren. Roon AI Playlist beginnt seine Arbeit erst, nachdem Roon den Stream bereitstellt; SpotBridge ist nicht in diese App eingebettet.

`Spotify unter macOS → SpotBridge → Roon Audio Input → Roon-Zone → Roon AI Playlist`

Roons Web Display zeigt Now Playing und Liedtexte im Browser, ist aber keine vollständige Browser-Fernbedienung mit diesen App-Werkzeugen. Siehe [Roon Displays](https://help.roonlabs.com/portal/en/kb/articles/displays).

## 10. Wartung und Transparenz

- Kombinierte Client-, Server- und Providerfehler anzeigen und als CSV exportieren.
- Verbindung und Konfiguration der einzelnen Dienste gezielt prüfen.
- App-Paket, SQLite-/JSON-Konsistenz, Caches und Speicherstatus prüfen.
- App-Konfiguration, Tokens, Wrapped, Hörbücher, Trigger und Metadaten gemeinsam sichern und wiederherstellen.
- Bild- und Coverspeicher verifiziert auf ein anderes Laufwerk verschieben.
- Ereignisschleifenverzögerung, Serverlaufzeit, Workerzustand, Auftragszahlen, Fehler und Neustarts diagnostizieren.
- Providerabfragen, Downloads, Hashing und Bildspeicherung in einem separaten überwachten Medienprozess ausführen.
- Den zentralen Windows-Dienst ohne dauerhaften Renderer betreiben, wenn die Anzeige über einen entfernten Browser oder RoonAIViewer erfolgt.

## Abgrenzung

Die App ersetzt Roon nicht. Roon bleibt für seine Bibliothek, Streaming-Integrationen, RAAT, DSP, Zonen, Queue und normalen Roon-Transport zuständig. Roon AI Playlist nutzt die Roon-Extension-APIs und ergänzt darauf aufbauend die oben beschriebenen Workflows; nur der ausdrücklich dokumentierte TIDAL-Hörbuchmodus verarbeitet offizielle Browserwiedergabe für Roon Audio Input oder einen Windows-Ausgang.
