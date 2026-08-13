# Roon AI Playlist

**Eine lokale Roon-Erweiterung für intelligente Playlisten, bessere Live-Radio-Metadaten, visuelle Mehrzonensteuerung, Hörbuchfunktionen, persönliche Hörstatistiken, Bildverwaltung und Hausautomationsaktionen.**

[English version – default](README.md)

> Roon AI Playlist ist ein unabhängiges Projekt und steht in keiner Verbindung zu Roon Labs, TIDAL, Last.fm, Deezer, fanart.tv, Audible oder den unterstützten KI-Anbietern.

## Aktuelle Versionen

- Informations- und Dokumentationsausgabe: **1.0.3**
- Roon AI Playlist: **1.0.466**
- RoonAIViewer: **1.0.3**

## Was ist Roon AI Playlist?

Roon AI Playlist richtet sich an Menschen, die Roon bereits verwenden und mehr Kontrolle über Musikentdeckung, Darstellung, Hörhistorie, Live Radio, Hörbücher und angeschlossene Geräte wünschen.

**Roon AI Playlist soll weder die Roon-Oberfläche noch irgendeine Kernfunktion von Roon ersetzen.** Roon bleibt für Musikbibliothek, Streaming, RAAT, DSP, Zonen, Warteschlangen und Audiowiedergabe zuständig. Diese Begleitanwendung wurde ausschließlich dafür geschaffen, außerhalb von Roon nützliche, dort fehlende Arbeitsabläufe zu ermöglichen – so weit es die Roon-Extension-APIs zulassen. Sie arbeitet mit dem vorhandenen Roon-System und gibt Wiedergabeaktionen an Roon zurück.

Die Anwendung läuft lokal und lässt sich auf vier Arten bedienen:

- als vollständige Windows-App auf dem Serverrechner,
- im wählbaren Modus **Nur Server + Konfiguration** ohne dauerhaft geladene Player-Oberfläche,
- über einen normalen Browser im privaten Netzwerk,
- über den schlanken Windows-Client **RoonAIViewer** auf einem anderen Rechner oder Display.

## Eigener Servermodus für die entfernte Bedienung

Der Windows-Installer kann jetzt entweder die vollständige App oder **Nur Server + Konfiguration** einrichten. Der Servermodus ist für einen Rechner gedacht, auf dem Roon AI Playlist dauerhaft läuft, während die eigentliche Bedienung über RoonAIViewer oder einen Browser auf einem anderen Gerät im Heimnetz erfolgt.

Im Servermodus bleiben der zentrale App-Dienst, die Roon-Verbindung, Netzwerk-Trigger, Wrapped-Aufzeichnung, Medienverarbeitung, Playlist-Werkzeuge, geplante Aufgaben und die Hörbuchaufnahme vollständig verfügbar. Die große lokale Player-Oberfläche wird jedoch nicht dauerhaft im Speicher gehalten. Die Konfiguration lässt sich weiterhin lokal über das Symbol im Windows-Infobereich öffnen; beim Schließen wird auch dieses Fenster wieder freigegeben. Der Betriebsmodus kann später in der Konfiguration geändert und mit einem App-Neustart übernommen werden.

Damit kann die Anwendung als zentraler Roon-Begleitdienst laufen, ohne auf Fernsteuerung oder Hintergrundfunktionen zu verzichten. Auch eine Hörbuchaufnahme lässt sich weiterhin über RoonAIViewer auf einem anderen System starten und überwachen, sofern Aufnahmezone und Ausgabeordner auf dem Serverrechner vorhanden sind.

## Kostenlose hochwertige KI-Playlisten mit Google Antigravity

Roon AI Playlist kann Playlisten jetzt vollautomatisch über die offizielle **Google Antigravity CLI** erzeugen. Dieser Weg benötigt keinen KI-API-Key, keinen manuellen Kopier-/Einfügeschritt und kein separates nutzungsabhängig abgerechnetes API-Konto. Nach einer einmaligen Google-Anmeldung auf dem Windows-System der App übergibt Roon AI Playlist den Musikwunsch im Hintergrund an die CLI und erhält die strukturierte Titelliste direkt zurück.

Google stellt im kostenlosen Individual-/Standard-Tarif derzeit moderne Modelle wie **Gemini 3.6 Flash, Gemini 3.5 Flash und Gemini 3.1 Pro** bereit – abhängig von Googles aktueller Modellverfügbarkeit und den jeweiligen Nutzungskontingenten. Roon AI Playlist bietet dafür eine echte Modellauswahl mit Denktiefen, kann kontospezifische Einträge aus `agy models` ergänzen und behält ein freies Feld für zukünftige Modell-IDs. **Gemini 3.1 Pro (High)** bleibt die praktisch bewährte Voreinstellung für qualitätsorientierte Playlisten.

Die erzeugte Liste durchläuft weiterhin den normalen Roon-Ablauf der App: Jeder Vorschlag wird gegen die tatsächliche Roon-Bibliothek geprüft, offene Titel können ersetzt werden und die Wiedergabe beginnt erst nach Bestätigung. Die App kauft niemals Credits und blockiert bereits aktivierte kostenpflichtige Antigravity-G1-/AI-Credits standardmäßig. Aktuelle Angaben stehen in Googles [Antigravity-Modellübersicht](https://antigravity.google/docs/models) und auf der Seite [Antigravity-Tarife und Kontingente](https://antigravity.google/pricing).

## Was ergänzt die App zu Roon?

### Intelligente Playlist-Erzeugung

- Musikwünsche frei in natürlicher Sprache beschreiben.
- Ollama, OpenRouter, OpenAI, Gemini, Claude, die geführte ChatGPT-Work-Übergabe oder die vollautomatische Google Antigravity CLI wählen.
- Wünsche mit Genre, Jahrzehnt, Stimmung, Energie und Sprache kombinieren.
- Playlisten aus Last.fm, Deezer, gepflegten Taglisten oder Wrapped-Favoriten erzeugen.
- Jeden Vorschlag vor der Wiedergabe mit der tatsächlichen Roon-Bibliothek abgleichen.
- Treffer, unsichere Ergebnisse, fehlende Titel und mögliche Alternativen anzeigen.
- Ergebnis in einer gewählten Roon-Zone starten oder als M3U speichern.

#### KI-Playlisten mit sichtbarem Roon-Abgleich

Die KI-Quelle verbindet eine optionale freie Beschreibung mit Stimmung und Energie, Jahrzehnt, Genre, Interpreten-Sprache, Zielzone und Titelanzahl. Das gewählte lokale, Cloud-, ChatGPT-Work- oder Antigravity-Modell schlägt die Musik vor, doch diese Vorschläge werden nicht ungeprüft abgespielt. Jeder Eintrag wird zuerst gegen Roon aufgelöst. Die Ergebnisansicht zeigt Titel, Interpret, Energie, Jahr, Providerverfügbarkeit, gefundene und fehlende Anzahl sowie einzelne Ersetzen-/Entfernen-Aktionen. Eine geprüfte Liste kann die Queue der gewählten Zone ersetzen, angehängt, gemischt oder für später gespeichert werden.

![KI-Playlist-Erzeugung mit Filtern und gegen Roon geprüften Treffern](assets/screenshots/playlist.png)

#### Last.fm-Playlisten ohne KI-Prompt

Die Last.fm-Quelle bietet eine nachvollziehbare Alternative auf Basis gepflegter Jahrzehnt-, Sprach-, Genre-, Stil- und Atmosphäre-Tags. Mehrere Tags lassen sich kombinieren, Titelanzahl und Zielzone werden direkt gewählt und die erzeugten Kandidaten durchlaufen denselben Roon-Abgleich und dieselbe Ergebnisprüfung wie KI-Vorschläge. Die fertige Liste kann abgespielt, angehängt, gemischt, bearbeitet oder gespeichert werden; die gewählten Tags bleiben in der Ergebnisüberschrift sichtbar, sodass ihre Herkunft erkennbar ist.

![Mit Tags erzeugte und für Roon geprüfte Last.fm-Playlist](assets/screenshots/lastfm.png)

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

- Festlegen, welche Roon-Zonen sichtbar sind, ihre Reihenfolge bestimmen und die ausgewählten Zonen gemeinsam in einem Dashboard darstellen.
- Cover, Wiedergabestatus, Fortschritt, Transportsteuerung und Warteschlange anzeigen.
- Kommende Titel, verbleibende Titelanzahl und gesamte Restzeit anzeigen.
- Eigene Ansichten für normale Musik, Roon Radio, Live Radio, Spotify-Streams und Hörbücher verwenden.
- Albumcover, Künstlerporträt und Künstlerhintergrund getrennt darstellen.
- Browser- und Viewer-Anzeigen bei kurzen Roon-Neuverbindungen stabil halten.
- Den aktuellen Titel direkt einer zonenbezogenen TIDAL-Zielplaylist hinzufügen.

![Zonendetail mit Warteschlange und Interpretenbild](assets/screenshots/player.png)

#### Spotify und externe Wiedergabe in Roon

Spielt Roon einen Spotify- oder anderen externen Stream, wechselt die Zonenansicht zu einer Darstellung, die zu den tatsächlich gelieferten Metadaten passt. Albumcover, Künstlerporträt, breites Künstlerbild, Titel, Interpret und Album bleiben getrennte Bildelemente; Dauer- und Suchlaufsteuerung werden ausgeblendet, wenn sie irreführend wären. Qualifizierte Spotify-Wiedergaben lassen sich in Wrapped als eigene Quelle erkennen. Die App meldet sich nicht bei Spotify an und ersetzt keinen Spotify-Client – sie stellt die Wiedergabe dar und erfasst sie, wenn sie über Roon bei ihr ankommt.

![Spotify-Wiedergabe mit Cover und Interpretenbildern](assets/screenshots/spotify_pl.png)

#### So gelangt Spotify zu Roon: SpotBridge

SpotBridge 1.0.0 ist eine eigenständige native macOS-Menüleisten-App, die lokale Spotify-Wiedergabe mit Roon Audio Input verbindet. Sie nimmt das Audiosignal des lokalen Spotify-Prozesses über einen CoreAudio Process Tap auf und überträgt das erfasste Signal als AAC oder verlustfrei codiertes Ogg-FLAC an eine gewählte Roon-Zone.

`Spotify unter macOS → CoreAudio Process Tap → SpotBridge → Roon Audio Input → gewählte Roon-Zone`

SpotBridge übermittelt Interpret, Titel, Album und Cover und kann Transportereignisse von Spotify und Roon automatisch aufeinander abstimmen. Sobald der entstehende Stream in Roon verfügbar ist, kann Roon AI Playlist seine Metadaten und Bilder darstellen und eine qualifizierte Hörsitzung in Wrapped erfassen. SpotBridge bleibt dabei eine unabhängige Begleitanwendung: Roon AI Playlist selbst nimmt weder Spotify-Audio auf noch meldet es sich bei Spotify an.

Ogg-FLAC erhält das aufgenommene Signal auf dem Übertragungsweg von SpotBridge zu Roon verlustfrei; die Qualität der ursprünglichen Spotify-Quelle wird dadurch nicht verbessert.

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

#### Hörbücher entdecken, bevor sie in der Roon-Bibliothek liegen

Die Hörbuchsuche ist eine eigenständige Katalogansicht für aktuelle deutschsprachige Veröffentlichungen. Sie kann Audible.de oder den Katalog der Deutschen Nationalbibliothek durchsuchen, nach Titel, Autor, Suchwort, Genre und Jahr filtern und nach verschiedenen Kriterien sortieren. Angezeigt werden je nach Quelle unter anderem Sprecher, Laufzeit, Genres, Bewertung und eine Hörprobenaktion. Ein Ergebnis lässt sich bei seiner Originalquelle öffnen oder an die TIDAL-Suche übergeben.

![Hörbuchentdeckung über den Audible-Katalog](assets/screenshots/audible.png)

Die anschließende TIDAL-Hörbuchsuche sucht passende Alben und prüft die Interpretenbeziehung des Albums unabhängig. Vor der Übernahme in die persönliche Hörbuchliste zeigt sie Cover, Autor beziehungsweise Interpret, Jahr, Laufzeit und Titelanzahl. Dadurch lässt sich auch ein echtes „bei TIDAL nicht verfügbar“ von einer gestörten Providerverbindung unterscheiden.

![TIDAL-Albensuche zu einem ausgewählten Hörbuch](assets/screenshots/tidal_search.png)

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

#### Hörhistorie bis zum einzelnen Titel

Die Ansicht **Tracks** ist die nachvollziehbare Datengrundlage hinter den visuellen Zusammenfassungen. Sie zeigt jede gezählte Wiedergabe mit Cover, Titel, Interpret, Album, Zeitpunkt, Quelle, gegebenenfalls Sender und tatsächlich gewerteter Hörzeit. Die Liste kann nach Zeitraum und Quelle – Roon, Live Radio oder Spotify – gefiltert werden; ein historischer Titel lässt sich erneut an eine ausgewählte Roon-Zone senden. Unvollständige oder falsche historische Metadaten bleiben hier sichtbar, statt in einer aggregierten Grafik zu verschwinden.

![Filterbare Wrapped-Titelhistorie](assets/screenshots/tracks.png)

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
- My Daily Discovery, nummerierte My Mixes, New Arrivals, Titelradio, Interpretenradio und weitere persönliche Radioeinträge des verbundenen TIDAL-Kontos ermitteln.
- Einen Mix in der ausgewählten Roon-Zone starten oder an die laufende Queue anhängen.
- Ausgewählte Mixe und persönliche Radios manuell oder per täglicher Synchronisierung als TIDAL-Playlisten speichern.
- Video-, Interpretenradio- oder Titelradio-Einträge bei Bedarf ausschließen.
- Pro Roon-Zone eine feste TIDAL-Zielplaylist konfigurieren.
- Den laufenden Titel oder einen erkannten Live-Radio-Titel über `T+` hinzufügen.
- Mix-Suchtext und Filter im lokalen App-Profil speichern.

#### Persönliche Mixe und Radios

Der Mix-Browser fasst die persönlichen TIDAL-Empfehlungen, die sonst auf mehrere TIDAL-Oberflächen verteilt sind, in einer filterbaren Übersicht zusammen. Jede Karte nennt Typ und prägende Interpreten. Die Zielzone wird einmal ausgewählt; **Mix starten** ersetzt die Wiedergabe, während **Mix anhängen** die laufende Queue beibehält und ergänzt. Ausgewählte Einträge können als normale TIDAL-Playlisten dauerhaft gespeichert werden. Der Synchronisationsstatus zeigt den letzten Lauf und die Zahl erfolgreicher Aktualisierungen.

![TIDAL-Browser für persönliche Mixe und Radios](assets/screenshots/personal_radio.png)

#### TIDAL-Playlist-Browser

Der Playlist-Browser durchsucht sowohl redaktionelle TIDAL-Playlisten als auch die Playlisten des verbundenen Benutzers. Jahrzehnt-, Genre-, Stimmungs- und Themenfilter lassen sich mit freiem Suchtext verbinden; der Quellenfilter kann die Treffer auf TIDAL- oder Benutzerplaylisten begrenzen. Die Karten zeigen Herkunft und Titelanzahl, eine Vorschau nennt vor dem Start die ersten Titel und jeder Treffer kann die Wiedergabe in Roon beginnen oder an die ausgewählte Zone angehängt werden.

![Direkte TIDAL-Playlist-Suche und Wiedergabe in Roon](assets/screenshots/tidal_pl.png)

### Fernbedienung und externe Geräte

- Bis zu zehn Schnellzugriffe für Live-Radio-Sender, Roon-Playlisten und Zonenaktionen konfigurieren.
- Mehrere unabhängige Netzwerk-Trigger für eine oder mehrere Roon-Zonen definieren.
- Getrennte HTTP- oder HTTPS-Befehle beim Wiedergabestart und nach Wiedergabeende senden.
- Verstärker, Steckdosen, IR-Bridges oder Hausautomationsgeräte steuern.
- Ausschalten nach Pause oder Stopp planen und bei erneuter Wiedergabe automatisch abbrechen.
- Mit einem manuellen AUS-Schalter die Zone stoppen, den Scheduler beenden und zugeordnete Geräte sofort ausschalten.
- Optional eine eigene Roon-Dummy-Zone als Bluetooth-Fernbedienungsproxy für Play, Pause, Next und Previous verwenden.

#### Zehn konfigurierbare Remote-Slots

Jeder Slot besitzt Aktivierung, Beschriftung, Aktion, Roon-Zone und – falls erforderlich – einen Sender oder eine Playlist als Ziel. Für Aktionen wie Play/Pause kann ein Toggle-Verhalten aktiviert werden. Ziele werden aus dem verbundenen Roon-System geladen; jeder Slot lässt sich testen, bevor er in der Oberfläche oder über den geschützten lokalen HTTP-Endpunkt eines ESP32, einer IR-Bridge oder eines ähnlichen Controllers verwendet wird.

![Zehn konfigurierbare IR- und WLAN-Remote-Slots](assets/screenshots/remote_v2.png)

#### Unabhängige Netzwerk-Trigger

Ein Netzwerk-Trigger überwacht eine oder mehrere Zonen und besitzt einen eigenen optionalen EIN-Befehl, optionalen AUS-Befehl und eine Ausschaltverzögerung. Der Live-Status zeigt Zonengruppe, Ausgangszustand, Countdown, letzten Befehl, Antwortzeit und Prüfergebnis. Mehrere Trigger können dieselbe Zone überwachen – etwa getrennt für Verstärker und Display –, ohne ihre Befehle aneinander zu koppeln. Tests werden ausdrücklich ausgelöst; die Sicherheitslogik hält AUS zurück, solange eine zugeordnete Zone aktiv, nicht vorhanden oder ihr Zustand unsicher ist.

![Unabhängige Netzwerk-Trigger mit Status und Scheduler](assets/screenshots/remote_trigger_2.png)

#### RoPieee-Fernbedienungsbrücke

RoPieee leitet Fernbedienungsereignisse normalerweise an eine fest gewählte Roon-Zone. Der optionale Proxy lässt RoPieee stattdessen eine eigene stumme Dummy-Zone steuern. Drei mitgelieferte Markertitel codieren Previous und Next, während der Transportzustand der Dummy-Zone Play und Pause abbildet. Roon AI Playlist leitet diese Aktionen an die zuletzt aktive konfigurierte Musik- oder Hörbuchzone weiter, kann das Ziel über App-Neustarts hinweg merken, unterdrückt Rückkopplungen und zeigt Markerprüfung sowie gemessene Bestätigungszeit. Auf RoPieee wird nichts installiert; Lautstärke und Mute werden bewusst nicht weitergeleitet.

![Konfiguration und Status des RoPieee-Dummy-Zonen-Proxys](assets/screenshots/ropieee_remote.png)

### Wartung und Stabilität

- Vollständige App-Sicherungen erstellen und wiederherstellen.
- Wrapped-Sitzungen primär in SQLite und zusätzlich als portablen Sicherungsstand speichern.
- Den Bildspeicher geprüft auf ein anderes lokales Laufwerk verschieben.
- Dienstestatus, Speicher, Caches, Providerfehler und Roon-Verbindung kontrollieren.
- Umfangreiche Metadatenabfragen, Bilddownloads, Prüfung, Hashing und Cache-Arbeiten getrennt ausführen, damit Player, Weboberfläche, Roon-Verbindung und Netzwerk-Trigger ansprechbar bleiben.
- Für ausschließlich entfernt bediente Systeme eine ressourcenschonende Installation **Nur Server + Konfiguration** ohne dauerhaft geladene lokale Player-Oberfläche wählen.

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

Die KI-Playlistfunktion ist optional und kann deaktiviert werden. Anbieter mit API-Key bleiben unterstützt; zusätzlich bietet Google Antigravity CLI einen vollautomatischen API-Key-freien Weg und ChatGPT Work eine geführte API-Key-freie Übergabe. Zu den optionalen Integrationen gehören TIDAL, Last.fm, Deezer, fanart.tv, MusicBrainz/Cover Art Archive, TheAudioDB, Audible und der gewählte KI-Dienst.

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
- [Änderungsprotokoll](CHANGELOG_DE.md)
- [Versionshinweise](docs/VERSIONSHINWEISE_DE.md)
- [Rechte und Inhalte Dritter](RIGHTS.md#deutsch)
- [English documentation](README.md)

## Verfügbarkeit

Dieses Informations-Repository enthält keine Installationsdateien und keinen Quellcode. Roon AI Playlist und RoonAIViewer werden getrennt bereitgestellt.

© 2026 mermayer. Alle Rechte vorbehalten. Einzelheiten zu dieser Dokumentation und zu den in Screenshots gezeigten Inhalten stehen unter [Rechte und Inhalte Dritter](RIGHTS.md#deutsch).
