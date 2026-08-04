# Roon AI Playlist – Benutzerhandbuch

[English version](USER_GUIDE.md) · [Zurück zur Übersicht](../README_DE.md)

Dokumentationsstand: Roon AI Playlist **1.0.458**, RoonAIViewer **1.0.3**.

## Inhaltsübersicht

1. [Aufgabe der App](#1-aufgabe-der-app)
2. [Voraussetzungen](#2-voraussetzungen)
3. [Installation und erster Start](#3-installation-und-erster-start)
4. [Navigation und Bedienoberflächen](#4-navigation-und-bedienoberflächen)
5. [Player und Zonen](#5-player-und-zonen)
6. [Playlisten erzeugen](#6-playlisten-erzeugen)
7. [Live Radio](#7-live-radio)
8. [TIDAL-Werkzeuge](#8-tidal-werkzeuge)
9. [Hörbücher](#9-hörbücher)
10. [Roon Wrapped](#10-roon-wrapped)
11. [Cover und Interpretenbilder](#11-cover-und-interpretenbilder)
12. [Roon Tools](#12-roon-tools)
13. [Remote-Slots](#13-remote-slots)
14. [Netzwerk-Trigger](#14-netzwerk-trigger)
15. [Fernbedienungs-Proxy](#15-fernbedienungs-proxy)
16. [Browser und RoonAIViewer](#16-browser-und-roonaiviewer)
17. [Konfiguration](#17-konfiguration)
18. [Sicherung und Wiederherstellung](#18-sicherung-und-wiederherstellung)
19. [Speicher und Wartung](#19-speicher-und-wartung)
20. [Sicherheit und Datenschutz](#20-sicherheit-und-datenschutz)
21. [Fehlerbehebung](#21-fehlerbehebung)
22. [Empfohlener Einrichtungsablauf](#22-empfohlener-einrichtungsablauf)

## 1. Aufgabe der App

Roon AI Playlist ergänzt ein vorhandenes Roon-System. Sie ist kein Ersatz für die Roon-Oberfläche oder Roons eigene Funktionen. Roon bleibt für Musikbibliothek, Streaming, RAAT, DSP, Zonen, Warteschlangen und Audiowiedergabe verantwortlich. Die App wurde geschaffen, um außerhalb von Roon zusätzliche, dort fehlende Arbeitsabläufe bereitzustellen – innerhalb der Möglichkeiten und Grenzen der Roon-Extension-APIs:

- intelligente und externe Playlist-Erzeugung,
- visuelle Mehrzonensteuerung,
- bessere Live-Radio-Metadaten und Bilder,
- Hörbuchfortschritt und Lesezeichen,
- persönliche Wrapped-Auswertungen,
- Cover- und Interpretenbildpflege,
- TIDAL-Schnellaktionen,
- Remote-Slots und Netzwerk-Trigger,
- Browser- und Viewer-Bedienung.

Die App ersetzt keine Roon-Bibliothek und greift nicht in die Audioverarbeitung ein. Wiedergabeaktionen werden an Roon übergeben.

## 2. Voraussetzungen

Für den normalen Betrieb werden benötigt:

- Windows 10 oder Windows 11, 64 Bit,
- ein laufender und im lokalen Netzwerk erreichbarer Roon Core,
- die Möglichkeit, die App unter **Roon > Einstellungen > Erweiterungen** zu autorisieren,
- eine Roon-Zone für die Wiedergabe.

Optional können folgende Dienste ergänzt werden:

- Ollama, OpenRouter, OpenAI, Gemini oder Claude für KI-Playlisten,
- TIDAL für direkte Suche und Playlistenaktionen,
- Last.fm und Deezer für Musiksuche und Metadaten,
- fanart.tv und TheAudioDB für Interpretenbilder,
- MusicBrainz und Cover Art Archive für Albumdaten und Cover,
- Audible für Hörbuchinformationen.

Nicht benötigte Dienste können deaktiviert bleiben. Der Player, Roon Tools, Hörbücher und große Teile von Wrapped funktionieren auch ohne KI-Anbieter.

## 3. Installation und erster Start

### Installation

1. Den separat bereitgestellten Windows-Installer öffnen.
2. Installation abschließen und Roon AI Playlist starten.
3. Beim ersten Start den Einrichtungsassistenten durchlaufen.

### Roon autorisieren

1. Warten, bis die App den Roon Core im Netzwerk gefunden hat.
2. In Roon **Einstellungen > Erweiterungen** öffnen.
3. **AI Playlist Generator** autorisieren.
4. Nur bei Verwendung der Hörbuchaufnahme zusätzlich **Roon AI Hoerbuchaufnahme** autorisieren.

Die normale Roon-Anbindung benötigt keinen manuell erstellten Roon-API-Schlüssel.

### Einrichtungsassistent

Der Assistent führt durch folgende Entscheidungen:

1. vorhandene App-Sicherung wiederherstellen oder frisch beginnen,
2. Roon-Verbindung herstellen,
3. lokalen oder LAN-Zugriff festlegen,
4. Sprache und grundlegende Oberfläche wählen,
5. KI- und Zusatzdienste aktivieren oder überspringen,
6. Zugangsdaten prüfen,
7. Konfiguration speichern.

Der Assistent kann später über **Konfiguration > Einrichtungsassistent** erneut geöffnet werden.

### Nach dem ersten Start prüfen

- Wird der Roon Core als verbunden angezeigt?
- Erscheinen die gewünschten Zonen im Player?
- Reagiert eine Zone auf Play/Pause?
- Werden Cover und Warteschlange angezeigt?
- Ist bei LAN-Zugriff ein API-Token gesetzt?
- Wurde eine erste Sicherung erstellt?

## 4. Navigation und Bedienoberflächen

Die Hauptnavigation besteht aus:

- **Player:** Zonenübersicht, Wiedergabe und Detailansichten.
- **Playlist:** KI-, Last.fm-, Tag- und Wrapped-Playlisten.
- **Hörbücher:** Bibliothek, Analyse, Fortschritt, Kapitel und Lesezeichen.
- **Wrapped:** persönliche Hörstatistik, Show, Story und Datenqualität.
- **Roon Tools:** Live-Radio-Sender, Roon-Playlisten, Queue und Schnellaktionen.
- **Konfiguration:** Dienste, Oberfläche, Wrapped, Remote, Wartung und Sicherungen.

### Vollständige Windows-App

Die vollständige App enthält die Bedienoberfläche und den zentralen App-Dienst. Wird das Fenster geschlossen, kann die App im Windows-Infobereich weiterlaufen. Das Tray-Menü öffnet App oder Browser, startet oder stoppt den Dienst, lädt neu oder beendet die Anwendung vollständig.

### Browseransicht

Die Browseransicht eignet sich für Tablets, Wanddisplays oder andere Rechner im privaten Netzwerk. Sie verwendet dieselben Zustände wie der normale Player, verzichtet aber in der Zonenansicht auf unnötige Fensterbestandteile.

### RoonAIViewer

RoonAIViewer ist ein separater Windows-Client für einen entfernten App-Dienst. Er wird in [Abschnitt 16](#16-browser-und-roonaiviewer) zusammengefasst und besitzt ein eigenes [ausführliches Handbuch](ROONAI_VIEWER_DE.md).

## 5. Player und Zonen

![Übersicht des Mehrzonen-Players](../assets/screenshots/new_zone_view.png)

### Zonenübersicht

Die Zonenübersicht ist unter **Konfiguration > UI** einstellbar. Normale Playeransicht und große Browseransicht besitzen getrennte Auswahlen: Es lässt sich festlegen, welche gefundenen Roon-Zonen sichtbar sind, in welcher Reihenfolge sie erscheinen und ob die Darstellung automatisch, ein- oder zweispaltig erfolgt. Das Ausblenden einer Zone entfernt sie nur aus dieser Ansicht; die Zone wird dadurch in Roon weder deaktiviert noch umbenannt.

Jede Zonenkarte kann folgende Informationen enthalten:

- Zonenname,
- Zustand wie Playing, Paused, Stopped oder Loading,
- Titel, Interpret und Album,
- Albumcover oder passendes Ersatzbild,
- Fortschritt und Titeldauer,
- kommende Titel,
- verbleibende Titelanzahl und Restzeit,
- Transportsteuerung.

Die App verwendet die vorhandene Roon-Zonenüberwachung. Mehrere Browser oder Viewer erzeugen keine eigene zusätzliche Roon-Verbindung.

### Zonen-Detailansicht

![Zonen-Detailansicht mit Warteschlange und Interpretenbild](../assets/screenshots/player.png)

Durch Öffnen einer Zone erscheint eine größere Darstellung. Je nach Wiedergabetyp zeigt sie:

- großes Album- oder Titelcover,
- Künstlerporträt und Künstlerhintergrund,
- aktuelle Metadaten,
- Fortschrittsbalken,
- Warteschlange,
- Wiedergabesteuerung,
- optionale TIDAL- und Netzwerkaktionen.

Bei einer normalen Queue stehen der aktuelle und kommende Titel im Mittelpunkt. Im Roon-Radio-Modus erhält die Künstlerdarstellung mehr Platz, solange Roon keine echte Folge-Queue meldet.

### Bedienelemente

Abhängig vom Inhalt können erscheinen:

- Zurück oder vorheriger Titel,
- Play/Pause,
- nächster Titel,
- zehn Sekunden zurück oder vor bei geeigneten Inhalten,
- `T+` zum Speichern in der zonenbezogenen TIDAL-Zielplaylist,
- **AUS** für Zonen mit einem konfigurierten Netzwerk-Trigger.

Bei reinen Musikansichten werden Sprungtasten ausgeblendet, wenn sie keinen sinnvollen Nutzen haben. Live Radio besitzt ebenfalls eine angepasste Steuerung.

### Queue und Restzeit

Die App zeigt eine Vorschau der kommenden Titel, ihre Dauer sowie die Gesamtzahl und Restzeit der noch ausstehenden Titel. Kurz verzögerte Queue-Daten werden kontrolliert nachgeladen, ohne ständig neue Abfragen zu starten.

### Bilder und Quellenzeichen

Kleine Buchstaben am Bild können die Quelle kennzeichnen, beispielsweise Roon oder fanart.tv. Cover, Künstlerporträt und breiter Hintergrund werden getrennt behandelt, damit nicht dasselbe Bild für jede Fläche verwendet werden muss.

Bei Künstlergruppen oder Duos sucht die App zuerst den vollständigen gemeinsamen Namen. Einzelne Beteiligte werden erst geprüft, wenn für die gemeinsame Identität kein geeigneter Treffer vorhanden ist.

### Roon Radio, Spotify und Hörbücher

- **Roon Radio:** angepasste Darstellung, bis eine normale Warteschlange vorliegt.
- **Spotify- oder externe Streams:** Stream-Metadaten und Cover werden bevorzugt; nicht passende Dauer- oder Sprungelemente werden ausgeblendet.
- **Hörbücher:** Kapitel, Position, Lesezeichen und Fortsetzen stehen im Vordergrund.

![Spotify-Wiedergabe in einer eigenen Zonenansicht](../assets/screenshots/spotify_pl.png)

Die Spotify-Darstellung ist eine Ansicht für Wiedergabe, die über Roon eintrifft, und kein eigener Spotify-Client. Die App durchsucht kein Spotify-Konto und übernimmt nicht die Spotify-Wiedergabe. Liefert der Stream verwertbare Angaben zu Interpret, Titel, Album und Cover, trennt der Player Albumcover, Künstlerporträt und Hintergrund. Qualifizierte Hörsitzungen werden in Wrapped als Spotify gekennzeichnet und lassen sich dort unabhängig filtern.

## 6. Playlisten erzeugen

![Mit Roon abgeglichene KI-Playlist](../assets/screenshots/playlist.png)

### Verfügbare Quellen

- **KI-Playlist:** freier Musikwunsch mit zusätzlichen Filtern.
- **Last.fm:** Vorschläge aus Tags und Stimmungen.
- **Taglisten:** gepflegte Kategorien für verschiedene Playlistquellen.
- **Wrapped Top 20:** persönliche Favoriten aus dem lokalen Wrapped-Verlauf.

### KI-Playlist erstellen

1. **Playlist** öffnen.
2. KI-Playlist als Quelle wählen.
3. Musikwunsch beschreiben, beispielsweise Stil, Anlass oder gewünschte Mischung.
4. Optional Jahrzehnte, Genres, Stimmung, Energie und Sprache eingrenzen.
5. Zielzone und gewünschte Titelanzahl wählen.
6. Playlist erzeugen.

Die freie Beschreibung darf leer bleiben, wenn die strukturierten Filter den Wunsch bereits vollständig ausdrücken. Stimmung und Energie, Jahrzehnt, Genre und Interpreten-Sprache werden mit dem aktuellen Anbieter und Modell kombiniert. Die Fußzeile nennt das erzeugende Modell und die verwendete Roon-Abgleichsstrategie.

Das Ergebnis ist eine bearbeitbare Arbeitsliste und keine undurchsichtige Ein-Klick-Aktion. Einzelne Kandidaten lassen sich probeweise starten, anhängen, ersetzen oder entfernen, bevor das Gesamtergebnis an Roon übergeben wird. Providerkennzeichnung, Jahr und Energielabel helfen dabei, eine unpassende Ausgabe oder einen Ausreißer zu erkennen.

### Last.fm-Tag-Playlist erstellen

![Last.fm-Tags und die daraus entstandene Roon-geprüfte Playlist](../assets/screenshots/lastfm.png)

1. **Last.fm-Playlist** als Quelle wählen.
2. Einen oder mehrere Jahrzehnt-/Jahr-, Sprach-, Genre-, Stil- oder Atmosphäre-Tags markieren.
3. Roon-Zone und Titelanzahl auswählen.
4. **Last.fm Top-Titel laden** verwenden.

Last.fm liefert populäre Kandidaten zur gewählten Tagkombination; anschließend führt die App den normalen Roon-Abgleich aus. Die Ergebnisüberschrift bewahrt die gewählten Tags, während die Fußzeile gefundene und fehlende Kandidaten trennt. **Alle zurücksetzen** löscht die Auswahl; eine zuvor gespeicherte Playlist kann geladen werden, ohne die Last.fm-Anfrage zu wiederholen.

### Roon-Abgleich verstehen

Die Vorschläge werden nicht ungeprüft abgespielt. Die App sucht jeden Kandidaten in der tatsächlichen Roon-Bibliothek und zeigt:

- sicher gefundene Titel,
- unsichere oder alternative Treffer,
- nicht gefundene Kandidaten,
- mögliche Ersatztracks.

Erst danach kann die Liste abgespielt, zur Queue hinzugefügt oder gespeichert werden. Externe IDs werden nicht blind als Roon-Bibliothekseinträge behandelt.

### Ergebnis verwenden

Je nach Ansicht stehen zur Verfügung:

- sofort in der gewählten Zone abspielen,
- zur vorhandenen Queue hinzufügen,
- Reihenfolge mischen,
- als M3U speichern,
- eine gespeicherte Liste laden und erneut prüfen.

### Taglisten verwalten

Die auswählbaren Kategorien für Last.fm-, KI- und Deezer-basierte Quellen können unter **Konfiguration > Dienste** bearbeitet und geprüft werden. Änderungen sollten vor dem Speichern validiert werden. Diese gepflegten Tags bestimmen die auswählbaren Schaltflächen der Playlist-Ansicht, sodass eine Installation ihr Vokabular ohne Änderung der App anpassen kann.

## 7. Live Radio

![Aufbereitete Live-Radio-Metadaten mit Cover und Interpretenbildern](../assets/screenshots/radio_new.png)

### Warum eine zusätzliche Aufbereitung nötig ist

Roon erhält Live-Radio-Metadaten aus dem Stream. Manche Sender liefern vollständige Felder, andere nur einen Text, vertauschte Namen, fehlerhafte Zeichen oder Werbeeinträge. Die App versucht daraus einen belastbaren Musiktitel zu bilden.

### Such- und Anzeigekette

Je nach vorhandenen Angaben werden verwendet:

1. ausdrückliche Roon-Albuminformationen,
2. TIDAL und bereits gespeicherte sichere Treffer,
3. MusicBrainz und Cover Art Archive,
4. Last.fm,
5. Deezer als weiterer Fallback.

Die App kann Artist, Titel und Album korrigieren, wenn ein sicherer Treffer vorliegt. Unpassende Compilations, Best-of-, Soundtrack-, Live- oder Remaster-Ergebnisse werden abgewertet, wenn sie nicht zu den vorhandenen Hinweisen passen.

### Nicht-Musik-Inhalte

Typische Jingles, Werbung, Nachrichten, Wetter, Intros, Outros, Senderkennungen und technische Automationsnamen werden möglichst vor der Providersuche erkannt. Dadurch entstehen weniger falsche Cover und weniger unerwünschte Wrapped-Einträge.

### Zeichensatzreparatur

Beschädigte Umlaute, Apostrophe und ähnliche Zeichen werden vor der Suche normalisiert. Die sichtbare Anzeige verwendet nach Möglichkeit ebenfalls die reparierte Schreibweise.

### Metadatenmodi pro Sender

Der Modus wird unter **Roon Tools** am jeweiligen Sender gespeichert:

- **Normal (`N`):** vollständige Suche und Anzeige; qualifizierte Musik wird regulär in Wrapped übernommen.
- **Vorsichtig (`V`):** exakt dieselbe Suche, Anzeige, Cover-, Interpretenbild- und `T+`-Funktion wie Normal. Nur Wrapped unterscheidet sich: Ohne verwertbaren Treffer erfolgt keine Aufnahme.
- **Aus (`A`):** keine externe Suche und keine Wrapped-Aufnahme; angezeigt werden die vom Sender beziehungsweise von Roon gelieferten Werte.

Das Moduszeichen erscheint neben dem Sendernamen in Zonenkarte und Detailansicht.

### `T+` bei Live Radio

In Normal und Vorsichtig kann ein erkannter Titel über `T+` in die für diese Zone konfigurierte TIDAL-Zielplaylist übernommen werden. Im Modus Aus steht die externe Aktion nicht zur Verfügung.

### Was tun bei einem falschen Treffer?

- Den Titelwechsel abwarten, um einen veralteten Zwischenstand auszuschließen.
- Prüfen, welchen Metadatenmodus der Sender verwendet.
- Im Fehlerprotokoll nach einem Provider- oder Zeichensatzfehler suchen.
- Einen später in Wrapped gespeicherten Eintrag über **Offene Cover verwalten** korrigieren.

## 8. TIDAL-Werkzeuge

Nach erfolgreicher TIDAL-Verbindung kann die App:

- Titel, Alben und Interpreten suchen,
- Beziehungen zwischen Titel, Album und Künstler auflösen,
- TIDAL-Mixe übernehmen,
- Ausschlussfilter für Mixe speichern,
- pro Roon-Zone eine TIDAL-Zielplaylist festlegen,
- laufende oder erkannte Radio-Titel über `T+` hinzufügen.

### Persönliche Mixe und Radios

![Persönliche TIDAL-Mixe, Entdeckungen, Titelradio und Interpretenradio](../assets/screenshots/personal_radio.png)

Die Ansicht **Mixe** liest die Empfehlungen des verbundenen TIDAL-Kontos und stellt sie gemeinsam dar. Je nach Konto gehören dazu My Daily Discovery, nummerierte My Mixes, My New Arrivals, eigene Mixe, Titelradio und Interpretenradio. Jeder Eintrag nennt seinen Typ und eine kurze Beschreibung oder prägende Interpreten.

Die Werkzeugleiste bietet:

- eine Roon-Zielzone,
- einen Textfilter für die sichtbaren Mixe,
- Kachel- und Listendarstellung,
- Auswahl aller aktuell sichtbaren Einträge,
- optionalen Ausschluss von Videos, Interpretenradio oder Titelradio,
- manuelle Aktualisierung und Synchronisierung,
- eine optionale tägliche Synchronisationszeit samt Status des letzten Laufs.

**Mix starten** ersetzt die Wiedergabe in der gewählten Roon-Zone. **Mix anhängen** ergänzt die bestehende Queue. Werden Einträge markiert und über **Auswahl speichern** übernommen, entstehen daraus normale TIDAL-Playlisten; spätere Synchronisierungen aktualisieren diese gespeicherten Kopien, statt unkontrolliert neue Duplikate anzulegen.

### TIDAL-Playlisten

![TIDAL-Playlisten suchen, prüfen, starten oder anhängen](../assets/screenshots/tidal_pl.png)

Die Ansicht **Playlisten** durchsucht redaktionelle TIDAL-Playlisten und die Playlisten des verbundenen Kontos. Freier Suchtext lässt sich mit Jahrzehnt-, Genre-, Stimmungs- und Themenfiltern kombinieren. Der Quellenfilter unterstützt alle Treffer, nur TIDAL oder nur Benutzerplaylisten. Karten kennzeichnen Herkunft und Titelanzahl. Vor der Wiedergabe kann eine Vorschau die ersten Titel nennen, was bei allgemeinen Namen wie „Party“ oder „Klassik“ besonders hilfreich ist.

Vor **PL starten** oder **PL anhängen** wird die Roon-Zone gewählt. Starten ersetzt die aktuelle Queue; Anhängen erhält und ergänzt sie. Dieser Ablauf steuert die Wiedergabe in Roon – der TIDAL-Eintrag wird weiterhin an Roon übergeben und nicht ungeprüft als lokales Roon-Bibliotheksobjekt behandelt.

### Zielplaylist einrichten

1. TIDAL in **Konfiguration > Dienste** aktivieren und verbinden.
2. Die verfügbaren Playlisten laden.
3. Für die gewünschte Roon-Zone eine Zielplaylist auswählen.
4. Einstellungen speichern.

Der `T+`-Button erscheint nur dort, wo eine sinnvolle TIDAL-Aktion möglich ist.

### Fehlersituationen

- Ein leerer Treffer bedeutet nicht automatisch einen Verbindungsfehler.
- Abgelaufene Anmeldung erneut verbinden.
- Bei Providerfehlern Verbindung und Dienstestatus prüfen.
- Ein TIDAL-Treffer ist nicht automatisch derselbe Bibliothekseintrag in Roon; die App führt deshalb getrennte Abgleiche durch.

## 9. Hörbücher

![Hörbuchplayer mit Kapiteln und Lesezeichen](../assets/screenshots/audiobooks.png)

### Katalogsuche mit Audible und DNB

![Filterbarer Hörbuchkatalog von Audible und DNB](../assets/screenshots/audible.png)

Die Registerkarte **Hörbuchsuche** dient der Entdeckung, bevor ein Titel zur lokalen Hörbuchbibliothek gehört. Als Katalogquelle stehen aktuelle Audible.de-Veröffentlichungen und der Katalog der Deutschen Nationalbibliothek zur Verfügung. Titel, Autor, Suchwort, Genre, Erscheinungsjahre und Sortierung grenzen die Treffer ein. Je nach Quelle zeigen die Karten Autor, Sprecher, Reihe, Laufzeit, Jahr, Genres, Bewertung und eine Hörprobe.

**Details** öffnet die verfügbaren Kataloginformationen. **Audible.de** führt zur Quellseite. **TIDAL** übergibt Titel und Autor an die nachfolgend beschriebene getrennte Albensuche; die App unterstellt nicht, dass jedes Katalogergebnis auch bei TIDAL verfügbar ist.

### Hörbuch bei TIDAL finden

![Geprüfte TIDAL-Albumkandidaten für ein Hörbuch](../assets/screenshots/tidal_search.png)

Der TIDAL-Dialog sucht Albumkandidaten und löst anschließend deren Interpretenbeziehung getrennt auf. Es bleiben nur Alben übrig, deren TIDAL-Interpret zum gesuchten Autor passt. Jeder Kandidat zeigt Cover, Interpret, Jahr, Laufzeit und Titelanzahl, damit Ausgaben und Bände vor **Zu meinen Alben hinzufügen** unterschieden werden können. Kein Treffer ist ein gültiges Verfügbarkeitsergebnis und wird anders dargestellt als Anmelde-, Timeout- oder Providerfehler.

Die Übernahme erzeugt den Hörbucheintrag der App; sie kauft keine Inhalte und importiert keine Audiodateien. Die Wiedergabeverfügbarkeit bleibt von TIDAL und Roon abhängig.

### Bibliothek synchronisieren

1. **Hörbücher** öffnen.
2. **Hörbücher synchronisieren** wählen.
3. Warten, bis alle entsprechenden Roon-Alben geladen wurden.
4. **Hörbücher analysieren** ausführen, um Kapitel und Dauer vollständig zu erfassen.

Die Analyse verwendet vollständige Seitennavigation und ist auch für Bücher mit mehreren hundert Kapiteln vorgesehen.

### Bibliotheksansicht

Zur Verfügung stehen:

- Listen- und Kachelansicht,
- Sortierung nach Titel, Autor, Fortschritt oder Aktualisierung,
- Cover, Autor, Kapitelzahl und Gesamtdauer,
- aktuelle Hörposition und Restzeit,
- Fortsetzen und Neustart.

### Hörbuchplayer

Die Detailansicht zeigt:

- großes Cover,
- Titel und Autor,
- Wiedergabezone,
- aktuelle Position,
- Kapitelliste,
- Kapitelnummern und Dauer,
- automatische und manuelle Lesezeichen,
- Transport- und Sprungsteuerung.

### Fortschritt und Lesezeichen

Der Fortschritt ist an das Hörbuch gebunden, nicht an eine einzige Zone. Wird ein bekanntes Buch in einer überwachten Roon-Zone wiedergegeben, kann dieselbe Buchposition fortgeschrieben werden.

- **Automatisches Lesezeichen:** wird durch die laufende Wiedergabe aktualisiert.
- **Manuelles Lesezeichen:** hält eine bewusst gespeicherte Position fest und kann wieder gelöscht werden.
- **Fortsetzen:** startet an der gespeicherten Position.
- **Von Anfang:** startet das Buch neu.

Erkannte Hörbücher werden nicht als normale Musik in Wrapped übernommen und lösen keine nächtlichen Musik-Interpretenbildsuchen aus.

### Optionale Hörbuchaufnahme

Die Aufnahme ist für bereits synchronisierte und analysierte Hörbücher vorgesehen.

Vor dem ersten Start:

1. unter **Konfiguration > Basis > Hörbuchaufnahme** Zielordner und exklusive Aufnahmezone wählen,
2. **System prüfen** ausführen,
3. alle gemeldeten Voraussetzungen erfüllen,
4. die zusätzliche Roon-Erweiterung **Roon AI Hoerbuchaufnahme** autorisieren.

Der Systemcheck prüft unter anderem Audiowerkzeuge, Eingabegerät, Roon-Zone, Schreibzugriff und freien Speicherplatz.

Während der Aufnahme:

- ist die konfigurierte Zone exklusiv reserviert,
- entstehen zunächst fortlaufende Mastersegmente,
- werden beobachtete Kapitelwechsel protokolliert,
- kann **Nach diesem Kapitel pausieren** vorgemerkt und wieder aufgehoben werden,
- beginnt Fortsetzen mit dem nächsten Kapitel in einem neuen Segment.

Nach der Aufnahme werden nummerierte MP3-Kapitel mit Titel, Autor, Album, Tracknummer und eingebettetem Cover erzeugt. Bei einem echten Fehler bleiben vorhandene Mastersegmente als Rettungsdateien erhalten.

## 10. Roon Wrapped

![Persönliche Wrapped-Show](../assets/screenshots/wrapped.png)

### Was wird erfasst?

Wrapped speichert qualifizierte lokale Hörsitzungen aus:

- normaler Roon-Musikwiedergabe,
- Live Radio im passenden Sendermodus,
- erkannten Spotify- oder externen Musikstreams.

Kurze Fehlstarts werden aus Hörzeit und Top-Listen herausgehalten, können aber für Skip- und Qualitätswerte berücksichtigt werden. Hörbücher und gefilterte Nicht-Musik-Inhalte werden ausgeschlossen.

### Ansichten

- **Dashboard:** Kernwerte, Top-Listen, Tageszeiten, Quellen und letzte Sitzungen.
- **Show:** kompakte visuelle Zusammenfassung mit Covermosaik und Höhepunkten.
- **Story:** nacheinander ablaufende Kapitelkarten mit Navigation und Autoplay.
- **Status:** Tracking-Zeitraum, Datenqualität, Coverabdeckung und fehlende Daten.
- **Gehörte Titel:** filterbare Liste der historischen Wiedergaben.

### Titelgenaue Hörhistorie

![Wrapped Tracks mit Datums- und Quellenfiltern](../assets/screenshots/tracks.png)

Die Ansicht **Tracks** legt die einzelnen Wiedergaben hinter den Zusammenfassungen offen. Jede Zeile enthält Cover, Titel, Interpret, Album, Zeitpunkt, Quelle, gegebenenfalls Sender und gewertete Hörzeit. Die Zeitraumwahl kann einen einzelnen Tag oder einen größeren Wrapped-Zeitraum anzeigen; der Quellenfilter isoliert normale Roon-Wiedergabe, Live Radio oder Spotify.

Ein Klick auf eine Zeile öffnet die Zonenauswahl. Die App sucht den historischen Titel in Roon und übergibt den aufgelösten Treffer an die gewählte Zone. Die Ansicht hilft außerdem, Einträge mit korrekturbedürftigem Interpret, Album oder Cover zu finden, weil ursprüngliche Quelle und Hörzeit sichtbar bleiben.

### Zeiträume

- aktuelles Jahr,
- aktuelles Quartal,
- aktueller Monat,
- letzte 30 Tage,
- letzte 90 Tage,
- gesamter Bestand,
- benutzerdefinierter Zeitraum.

### Historische Titel erneut abspielen

Ein Klick auf einen Titel oder Top-Track öffnet eine Zonenauswahl. Die App sucht den Titel in Roon und startet ihn in der gewünschten Zone. Findet Roon dabei bessere Daten, können fehlende Album- oder Coverinformationen ergänzt werden.

### Exporte

Je nach Oberfläche können folgende Exporte erstellt werden:

- PNG-Karte,
- PDF-Bericht,
- CSV-Daten.

PDF ist für die vollständige Windows-App vorgesehen. Browser und Viewer verwenden vor allem PNG, CSV und die Bildschirmansichten.

### Wrapped-Daten vervollständigen

Unter **Konfiguration > Wrapped > Datenverwaltung** führt **Wrapped-Daten vervollständigen** drei Schritte aus:

1. fehlende Alben ermitteln,
2. fehlende Cover suchen,
3. externe Bilder lokal speichern.

Alle offenen Gruppen werden bearbeitet, bis kein weiterer Fortschritt möglich ist. **Automatisch vervollständigen** startet denselben Ablauf sofort und prüft anschließend alle fünf Minuten auf neue Lücken. **Lauf stoppen** beendet den aktuellen Vorgang.

### Offene Cover verwalten

Unter **Erweiterte Aktionen > Offene Cover verwalten** erscheinen weiterhin ungelöste Titel gruppiert. Für eine Gruppe können:

- Interpret, Titel und Album korrigiert,
- die korrigierten Werte gespeichert und sofort neu gesucht,
- die Suche ohne Änderung wiederholt,
- die betroffenen Wrapped-Wiedergaben nach Bestätigung gelöscht werden.

Vor dem Löschen zeigt die App die genaue Zahl der betroffenen Wiedergaben. Eine zusätzliche Prüfung verhindert, dass eine zwischenzeitlich geänderte Gruppe versehentlich gelöscht wird.

## 11. Cover und Interpretenbilder

### Anbieterreihenfolge

Unter **Konfiguration > Wrapped > Interpretenbilder verwalten** können folgende Anbieter sortiert oder deaktiviert werden:

- fanart.tv,
- TIDAL,
- Roon,
- Last.fm,
- Deezer,
- TheAudioDB.

Der erste brauchbare Treffer der gewählten Reihenfolge gewinnt. Manuell festgelegte Bilder behalten Vorrang.

### Bildaktionen

- vorhandene lokale Treffer ansehen,
- ein Bild für einen Künstler festlegen,
- einen Treffer nur für diesen Künstler ablehnen,
- eine Ablehnung zurücknehmen,
- externe Neusuche für einen Künstler starten,
- eigenes JPEG-, PNG- oder WebP-Bild hinterlegen.

### Porträt und Hintergrund

Die App unterscheidet normale Künstlerbilder und breite Hintergründe. Bei Live Radio kann deshalb oben ein Porträt und unten ein separates Fanart-Banner erscheinen. Fehlt ein geeigneter Hintergrund, kann auf ein normales Künstlerbild zurückgefallen werden.

### Mehrfachinterpreten

Namen wie Duos, Bands oder gemeinsame Credits werden zuerst vollständig gesucht. Nur wenn die Einheit kein brauchbares Bild liefert, werden einzelne Beteiligte geprüft. Eine geteilte Darstellung wird nur verwendet, wenn die Einzelergebnisse sinnvoll vollständig sind.

## 12. Roon Tools

Roon Tools bündelt schnelle Roon-Aktionen:

- Live-Radio-Sender laden und starten,
- Metadatenmodus pro Sender wählen,
- Roon-Playlisten laden und starten,
- Playzone auswählen,
- Playlist-Sortierung wählen,
- Queue der gewählten Zone anzeigen,
- konfigurierte Remote-Slots auslösen.

Die Queue-Karte in Roon Tools ist eine kompakte Warteschlangenansicht und nicht identisch mit der vollständigen Zonen-Detailansicht.

### Playlist-Sortierung

Roon-Playlisten können alphabetisch, nach Titelanzahl oder in der in Roon sichtbaren Reihenfolge angezeigt werden. Die zuletzt gewählte Sortierung wird gespeichert.

## 13. Remote-Slots

![Konfiguration von zehn IR- und WLAN-Remote-Slots](../assets/screenshots/remote_v2.png)

Unter **Konfiguration > Remote** können bis zu zehn Schnellaktionen angelegt werden. Ein Slot besitzt:

- eine Nummer,
- ein sichtbares Label,
- eine Zielzone,
- eine Aktion.

Mögliche Aktionen sind beispielsweise:

- Live-Radio-Sender starten,
- Roon-Playlist starten,
- Wiedergabe einer Zone starten oder umschalten.

Jeder Slot kann in der Konfiguration getestet werden. Aktive Slots erscheinen an den vorgesehenen Stellen der Oberfläche und können auch von kompatiblen lokalen Fernbedienungslösungen ausgelöst werden.

Die Einstellung **Toggle** eignet sich, wenn eine Hardwaretaste beispielsweise abwechselnd Play und Pause auslösen soll. **Ziele laden** holt die zur gewählten Aktion passenden Sender oder Playlisten aus Roon. Die sichtbare Beschriftung ist vom Roon-Zielnamen unabhängig; dadurch kann ein kurzer, hardwaregerechter Name verwendet werden, ohne Zone oder Playlist in Roon umzubenennen. Deaktivierte Slots behalten ihre Konfiguration, reagieren aber nicht.

Kompatible ESP32-, IR/WLAN- oder Hausautomationscontroller können einen geschützten lokalen Endpunkt für die jeweilige Slotnummer aufrufen. API-Token und Sicherheit des lokalen Netzes bleiben Aufgabe der Installation; diese Endpunkte sollten nicht direkt ins Internet gestellt werden.

## 14. Netzwerk-Trigger

Netzwerk-Trigger verbinden den Roon-Wiedergabestatus mit externen Geräten.

![Zwei unabhängige Netzwerk-Trigger mit Live-Status und Countdown](../assets/screenshots/remote_trigger_2.png)

### Typische Anwendungen

- Verstärker beim Wiedergabestart einschalten,
- aktive Lautsprecher oder Steckdosen zeitverzögert ausschalten,
- IR- oder Hausautomationsbridge ansteuern,
- mehrere Geräte einer Zone gemeinsam verwalten.

### Trigger einrichten

1. **Konfiguration > Remote > Netzwerk-Trigger** öffnen.
2. Trigger hinzufügen und verständlich benennen.
3. Eine oder mehrere Roon-Zonen zuordnen.
4. EIN- und/oder AUS-Adresse eintragen; mindestens eine Richtung ist erforderlich.
5. Ausschaltverzögerung wählen, wenn ein AUS-Befehl vorhanden ist.
6. Konfiguration validieren.
7. EIN und AUS getrennt testen.
8. Einstellungen speichern und Status beobachten.

### Zulässige Varianten

- **EIN und AUS:** vollständige automatische Steuerung.
- **Nur EIN:** beim Start einschalten; kein Ausschalt-Timer.
- **Nur AUS:** beim Wiedergabestart für den nächsten Pause-/Stopp-Vorgang vormerken, aber keinen EIN-Befehl senden.

### Scheduler-Verhalten

- Beginnt oder lädt mindestens eine zugeordnete Zone, wird ein geplanter AUS-Vorgang abgebrochen und gegebenenfalls EIN gesendet.
- Sind alle zugeordneten Zonen pausiert oder gestoppt, startet die Ausschaltverzögerung.
- Beginnt die Wiedergabe erneut, wird der Timer abgebrochen.
- Fehlt eine zugeordnete Zone oder ist ihr Zustand unsicher, wird aus Sicherheitsgründen nicht ausgeschaltet.
- Beim Ablauf wird AUS einmal gesendet, sofern alle Zonen weiterhin inaktiv sind.

### Manueller AUS-Schalter

Zonen mit einem aktiven Trigger und AUS-Befehl erhalten in allen Zonenansichten einen manuellen AUS-Schalter. Er:

1. stoppt die Roon-Zone,
2. beendet zugehörige Ausschalt-Timer,
3. sendet die AUS-Befehle der zugeordneten Trigger sofort.

Bei einem gemeinsamen Trigger warnt die Oberfläche, wenn eine andere zugeordnete Zone noch aktiv ist. Die manuelle Aktion darf den nächsten echten Wiedergabestart nicht blockieren.

Das Statusfeld dient nicht nur der Einrichtung: Es meldet zusammengefassten Zonenzustand, aktuellen Triggerausgang, verbleibenden Timer, Ergebnis des letzten Befehls und Antwortzeit. Dadurch lässt sich ein echter automatischer Übergang von einem erfolgreichen Einzeltest unterscheiden. Mehrere Trigger werden unabhängig verarbeitet; ein nicht erreichbarer HTTP-Endpunkt verändert nicht den Zustand eines anderen Triggers.

## 15. Fernbedienungs-Proxy

![Konfiguration und Live-Status des RoPieee-Dummy-Zonen-Proxys](../assets/screenshots/ropieee_remote.png)

Der optionale Dummy-Zonen-Proxy kann Play, Pause, Next und Previous einer Bluetooth- oder ähnlichen Fernbedienung an die zuletzt aktive Musik- oder Hörbuchzone weiterleiten.

Benötigt werden:

- eine eigene Roon-Dummy-Zone,
- eine festgelegte Musikzone,
- eine festgelegte Hörbuchzone,
- die bereitgestellten langen Markertracks in definierter Reihenfolge.

Die App unterscheidet absichtliche Markerbewegungen von natürlichem Titelende und Rückkopplungen. Zielzone, Marker, letzter Befehl und Bestätigungszeit werden in der Konfiguration angezeigt. Lautstärke und Mute werden nicht weitergeleitet.

Vor der Verwendung sollte die Konfiguration validiert und die Dummy-Zone synchronisiert werden.

### RoPieee-Ablauf

RoPieee wird so eingestellt, dass es ausschließlich die eigene Dummy-Zone steuert. Auf RoPieee wird keine zusätzliche Komponente installiert. Der Dummy-Ausgang sollte stumm sein; seine Queue enthält die mitgelieferten langen Titel **Remote Marker A**, **Remote Marker B** und **Remote Marker C** in genau dieser Reihenfolge. Die App aktiviert für diese Queue Wiederholung und deaktiviert Shuffle sowie Roon Radio.

- Ein Play- oder Pause-Wechsel der Dummy-Zone wird als Play beziehungsweise Pause weitergeleitet.
- Eine absichtliche Markerbewegung wird als Next oder Previous interpretiert.
- Natürliches Markerende und von der App selbst ausgelöste Änderungen werden unterdrückt, damit keine Steuerschleife entsteht.
- Ziel ist die zuletzt aktive konfigurierte Musik- oder Hörbuchzone; vor der ersten Aktivität gilt ein Standardziel, und das letzte Ziel kann optional einen Neustart überstehen.

Das Live-Feld zeigt Bereitschaft, aktives Ziel, Dummy-Zustand, letzten weitergeleiteten Befehl, Markerprüfung und Bestätigungszeit. **Dummy synchronisieren** stellt erwartete Queue und Zustand nach Konfigurationsänderungen wieder her. Lautstärke und Mute gehören bewusst nicht zum implementierten Proxy.

## 16. Browser und RoonAIViewer

### Browserzugriff

Für den Zugriff von einem anderen Gerät:

1. LAN-Zugriff in der App aktivieren,
2. einen API-Token konfigurieren,
3. den verwendeten Port in der Firewall des Serverrechners freigeben,
4. Serveradresse und Port im Browser öffnen.

Der Zugriff ist für ein vertrauenswürdiges privates Netzwerk gedacht und sollte nicht direkt ins Internet freigegeben werden.

### RoonAIViewer

RoonAIViewer zeigt dieselbe Oberfläche in einem eigenen Windows-Fenster. Der Viewer:

- startet keinen eigenen App-Dienst,
- stellt keine direkte Roon-Verbindung her,
- besitzt Tray-Betrieb und Autostart,
- speichert einen Zoom von 90 bis 130 Prozent,
- prüft Serveradresse und Token nativ,
- schützt den Token mit Windows DPAPI,
- kann eine fälschliche Offline-Anzeige automatisch neu laden.

Die komplette Einrichtung, Bedienung, Fehlerbehebung und Deinstallation steht im [RoonAIViewer-Handbuch](ROONAI_VIEWER_DE.md).

## 17. Konfiguration

Die Konfiguration besteht aus den Registerkarten **Basis**, **UI**, **AI**, **Dienste**, **Wrapped**, **Remote**, **Wartung** und **Speichern & Logs**. Die Statuskarten oberhalb der Registerkarten zeigen, ob App-Paket, Roon, gewählter KI-Anbieter, optionale Dienste und Datenspeicher bereit sind. Grau bedeutet dabei häufig bewusst deaktiviert oder nicht ausgewählt und nicht automatisch einen Fehler.

Die meisten Servereinstellungen werden erst mit **Änderungen speichern** übernommen. Client-Verbindung, TIDAL-Autorisierung, einzelne Wrapped-Wartungsaktionen und einige Remote-Tests besitzen eigene Schaltflächen und werden unabhängig ausgeführt. **Neu laden** verwirft noch nicht gespeicherte Formänderungen. **Defaults laden** lädt Standardwerte nur in das Formular; dauerhaft werden sie erst nach dem Speichern.

Zugangsdaten werden lokal gespeichert. Da App-Backups API-Schlüssel, Tokens und persönliche Daten enthalten können, müssen sie wie Passwörter behandelt werden.

### Basis: Client-Verbindung

- **Modus – Lokaler Server:** Die Oberfläche verwendet den App-Dienst, der sie ausgeliefert hat. Das ist die normale Einstellung einer vollständigen Windows-Installation.
- **Modus – Entfernter Server:** Die Oberfläche sendet ihre API-Aufrufe an die eingetragene Installation auf einem anderen Rechner.
- **Server-Adresse:** Basisadresse einschließlich `http://` oder `https://` und Port, aber ohne `/api`. Sie wird nur im entfernten Modus verwendet.
- **API-Token für diesen Client:** Muss dem `server.apiToken` des Zielservers entsprechen. Es ist weder ein TIDAL- noch ein KI-Schlüssel und wird nur im lokalen Profil dieses Clients gespeichert.
- **Client-Einstellungen speichern:** Speichert diese drei Werte getrennt von der Serverkonfiguration.
- **Verbindung testen:** Prüft Erreichbarkeit und Token, ohne die übrige App-Konfiguration zu verändern.

Für RoonAIViewer werden Server und Token im nativen Viewer-Verbindungsdialog verwaltet; Einzelheiten stehen im [RoonAIViewer-Handbuch](ROONAI_VIEWER_DE.md).

### Basis: Desktop-Start

- **Mit Windows starten:** Startet nach der Windows-Anmeldung die Electron-App und damit den lokalen App-Dienst.
- **Beim Start minimiert im Tray starten:** Öffnet zunächst kein sichtbares Hauptfenster. Die Oberfläche kann über das Tray-Symbol aufgerufen werden.

Beide Optionen gelten nur für die vollständige Windows-App. Ein Browser und RoonAIViewer besitzen eigene Startmechanismen.

### Basis: Bild- und Cover-Speicher

- **Speicherordner:** Gemeinsamer Ort für Roon-/TIDAL-/Hörbuch-Covercache, lokale Interpretenbilder und Wrapped-Cover. Leer verwendet den App-Datenordner.
- **Belegter Speicher / Objekte / Aufschlüsselung:** Zeigen Umfang und Verteilung des aktuellen Bildbestands.
- **Inhalte verschieben:** Kopiert und prüft den vorhandenen Bestand, bevor auf den neuen Ordner umgeschaltet wird. Die übrigen App-Daten werden nicht verschoben.
- **Größe neu berechnen:** Liest Belegung und Objektzahl neu ein, ohne Dateien zu verändern.

Der neue Ordner muss dauerhaft erreichbar und beschreibbar sein. Der geprüfte Ablauf und Fehlerfälle sind in [Kapitel 19](#19-speicher-und-wartung) beschrieben.

### Basis: Hörbuchaufnahme

- **Audio-Ausgabeordner:** Absoluter, beschreibbarer Pfad auf dem Windows-Rechner des App-Servers. Im Browser wird der Serverpfad eingetragen, nicht ein Ordner des Browsergeräts.
- **Aufnahmezone:** Exklusive lokale Roon-Zone auf demselben Windows-Rechner. Nur deren Audiosignal wird aufgenommen.
- **Ausgabeformat:** Fest vorgegebenes MP3-Format mit 192 kbit/s CBR.

Vor der ersten Aufnahme muss der Systemcheck aus [Kapitel 9](#9-hörbücher) erfolgreich sein.

### Basis: Server, Roon und Protokolle

- **`server.host`:** Netzwerkadresse, an die der Webserver gebunden wird. `127.0.0.1` erlaubt nur lokalen Zugriff; eine LAN-Bindung sollte nur mit API-Token in einem vertrauenswürdigen Netz verwendet werden.
- **`server.port`:** HTTP-Port des App-Dienstes. Nach einer Änderung müssen Browser- und Viewer-Adressen angepasst werden; die App kann neu starten.
- **`server.apiToken`:** Optionaler Schutz für Steuer- und Schreibzugriffe. Ein gesetzter Token muss in Browsern und Viewern identisch hinterlegt werden.
- **`music.service`:** Bevorzugt beim Roon-Suchen und Queueing Treffer aus TIDAL oder Qobuz. Dies aktiviert keine direkte Qobuz-App-Integration.
- **`roon.matching.mode`:** `strict` akzeptiert nur sehr genaue Treffer; `relaxed` toleriert stärkere Abweichungen und kann dadurch mehr, aber auch ungenauere Treffer liefern.
- **`roon.matching.strategy`:** `smart` verwendet mehrstufige Titel-, Alias- und `feat.`-Fallbacks; `strict` verzichtet bewusst auf aggressive Fallbacks. Für den Alltag ist `smart` gewöhnlich die robustere Strategie.
- **`playlists.directory`:** Ablageordner für gespeicherte M3U-Playlisten. Leer verwendet den automatisch ermittelten Musikordner.
- **`roon.configFile`:** Pfad zur Pairing-/Zustandsdatei der Roon-Integration. Diese Expertenoption sollte nur bei einer gezielten Wiederherstellung oder nach entsprechender Diagnose verändert werden.
- **`logs.generationLogRetentionDays`:** Automatische Aufbewahrung des Generierungslogs in Tagen; `0` deaktiviert die zeitbasierte Aufbewahrung.
- **Roon-NowPlaying-Rohlog:** Schreibt detaillierte unverarbeitete Now-Playing-Daten in ein Diagnoseprotokoll. Nur zur Fehlersuche aktivieren, da Datei und enthaltene Hörinformationen wachsen können.

### UI: Sprache, Standardzone und Playlistdarstellung

- **`ui.language`:** Schaltet die App-Oberfläche zwischen Deutsch und Englisch um.
- **`ui.defaultPlayZoneId`:** Zone, die nach dem App-Start in Playlisten-, TIDAL- und Werkzeugansichten vorausgewählt wird. Leer nimmt die erste verfügbare Zone.
- **Freitext intern auf Englisch für KI:** Formuliert einen deutsch eingegebenen freien Playlistwunsch intern als englische Arbeitsanweisung. Die sichtbare Oberfläche und strukturierte Filter bleiben unverändert.
- **Gefundenen Roon/TIDAL-Titel anzeigen:** Zeigt in der Ergebnisliste die Schreibweise des tatsächlich aufgelösten Treffers statt ausschließlich des ursprünglichen Vorschlags.
- **Trefferqualität anzeigen:** Blendet die Bewertung des Roon-Abgleichs ein. Die Grenzen **High** und **Medium** bestimmen, ab welchem Score ein Treffer sicher, mittel oder unsicher dargestellt wird; High muss oberhalb von Medium liegen.
- **Unsichere Treffer gezielt ersetzen:** Aktiviert die Aktion, nur als unsicher bewertete Kandidaten erneut zu suchen, ohne sichere Einträge anzutasten.

### UI: Wiederholungsfilter und Modellvergleich

- **Playlist-Historie zur Wiederholungsvermeidung:** Prüft neue Vorschläge gegen kürzlich erzeugte Playlisten.
- **Lookback-Playlisten:** Anzahl zurückliegender Playlisten, die in diese Prüfung eingehen.
- **Maximale Wiederholungen:** Ab welcher Häufigkeit ein Titel als zu oft verwendet gilt. Strengere Werte erhöhen die Abwechslung, können aber bei kleinen Bibliotheken die Trefferquote senken.
- **Modellvergleich aktivieren:** Blendet auf der Playlist-Seite den Bake-off für mehrere Ollama-Modelle ein.
- **Modelle (CSV):** Kommagetrennte Ollama-Modellnamen, die mit demselben Wunsch verglichen werden.
- **Metrik:** `foundRate` bevorzugt die höchste Roon-Trefferquote, `duration` die kürzeste Laufzeit und `balanced` gewichtet beides.

### UI: Player- und Browserdarstellung

- **Queue-Vorschau:** Legt fest, ob drei bis acht kommende Titel pro Zonenkarte gezeigt werden.
- **Browser-Zonen-Zoom / Detail-Zoom:** Skalieren die gesamte reduzierte Browserübersicht beziehungsweise eine daraus geöffnete Detailansicht von 70 bis 160 Prozent.
- **Browser-Zonentext / Detailtext:** Skalieren nur die Schrift der beiden Browseransichten. Damit lassen sich Bilder und Texte unabhängig an ein Display anpassen.
- **Cover-Hintergrundbereich:** Begrenzt den unscharfen Coverhintergrund auf den Coverbereich oder erweitert ihn über Detailseiten und Trackliste.
- **Tracklisten-Helligkeit:** Regelt die Helligkeit dieses Hintergrunds hinter der rechten Trackliste.
- **Player-Zonenansicht:** Für jede gefundene Roon-Zone lassen sich Sichtbarkeit, Reihenfolge und zonenbezogene TIDAL-Zielplaylist festlegen. Das Layout kann ein-, zweispaltig oder automatisch sein. **TIDAL-Playlisten laden** aktualisiert die wählbaren Ziele für `T+`.
- **Browser-Zonenansicht:** Besitzt eine eigene Sichtbarkeit, Reihenfolge und Spaltenwahl. Änderungen betreffen nur die reduzierte Browseransicht und verändern keine Roon-Zone.

### AI: Allgemeine Steuerung

- **KI-Playlist-Erzeugung aktivieren:** Schaltet ausschließlich die KI-Quelle ein oder aus. Player, Last.fm-/Deezer-/Wrapped-Playlisten, TIDAL, Hörbücher und Roon Tools bleiben verfügbar.
- **`ai.mode`:** Wählt Ollama, OpenRouter, OpenAI, Gemini oder Claude. Nur die Einstellungen des gewählten Anbieters werden für neue KI-Playlisten verwendet.
- **Request-Timeout:** Maximale Wartezeit je KI-HTTP-Anfrage. Ein größerer Wert hilft langsamen Modellen, verlängert aber die Wartezeit bei echten Ausfällen.
- **Cloud-Ultra-Sparmodus:** Versucht Cloud-Generierung mit einem einzigen Request und ohne Nachfüllen. Das reduziert Kosten und Anfragen, kann aber weniger Titel als gewünscht liefern.
- **Deutsche Referenzliste:** Nutzt bei deutschen Vocals oder Schlager eine lokale JSON-Liste als Titelbasis. Pfad bestimmt die Datei; **Max Hints** begrenzt die je Prompt übergebenen Einträge; **Diversity Lookback** meidet zuletzt verwendete Referenztitel.
- **Mindest-Trefferquote:** Ab welcher in Roon gefundenen Quote eine Liste als ausreichend gilt.
- **Fehlende Titel automatisch ersetzen / maximale Durchläufe:** Steuern, ob und wie oft fehlende Kandidaten automatisch nachgebessert werden.

### AI: Gemeinsame Provideroptionen

Je nach Anbieter werden die Felder **URL**, **API-Key**, **Modell-Preset**, **freies Modell** und weitere Laufzeitoptionen angeboten; nicht jeder Provider besitzt oder unterstützt jede der folgenden Einstellungen. Ein freier Modellname überschreibt das Preset. API-Schlüssel werden lokal gespeichert und in App-Backups aufgenommen.

- **Temperature:** Niedrigere Werte liefern stabilere, weniger variable Antworten; höhere Werte erhöhen die Variation. `auto` lässt die App beziehungsweise den Anbieter einen geeigneten Wert wählen. Nicht jedes Reasoning-Modell akzeptiert eine Temperature.
- **Reasoning/Think:** Steuert bei kompatiblen Modellen den Denkaufwand. Nicht unterstützte Modelle ignorieren den Wert oder können ihn ablehnen.
- **Quality Mode:** Arbeitet konservativer und gegebenenfalls mit zusätzlichen Prüfungen, benötigt aber mehr Zeit.
- **Fast Mode:** Reduziert Retries und Wartezeiten; schneller, aber mit weniger Reserve bei kurzzeitigen Providerproblemen.
- **Sparmodus:** Verwendet möglichst nur einen Request und füllt fehlende Titel nicht nach.

### AI: Ollama

- **URL:** Ollama-Endpunkt aus Sicht des App-Servers. Läuft Ollama auf einem anderen Rechner, muss dessen LAN-Adresse statt `localhost` eingetragen sein.
- **Verbindung testen:** Prüft den Endpunkt unabhängig von einer Playlistgenerierung.
- **Preset / freies Modell:** Wählt ein installiertes Modell. Der freie Name überschreibt das Preset.
- **Think, Temperature, Quality, Spar- und Fast Mode:** Steuern Denkaufwand, Variation und Geschwindigkeits-/Qualitätskompromiss des lokalen Modells.

### AI: OpenRouter

- **URL / API-Key / Modell:** Verbinden den OpenRouter-Endpunkt und wählen eine Modell-ID im Format `Anbieter/Modell`.
- **Eigene Modellliste:** **Eigenes Modell übernehmen** fügt den freien Eintrag gezielt zum Dropdown hinzu. Einzelne eigene Einträge oder die gesamte eigene Liste lassen sich löschen; eingebaute Presets bleiben erhalten. Dauerhaft wird die Änderung erst mit **Änderungen speichern**.
- **Reasoning, Temperature, Quality und Fast Mode:** Gelten nur, wenn das gewählte Modell die jeweilige Option unterstützt.
- **Max Retries, Retry Delay, Max Retry Delay, Inter-Batch Delay:** Begrenzen Wiederholungen und Wartezeiten bei Rate-Limits oder vorübergehenden Fehlern. Sehr kleine Werte reagieren schneller, erhöhen aber die Gefahr unnötiger Abbrüche; sehr große Werte verlängern einen Lauf deutlich.

### AI: OpenAI und Gemini

Beide Bereiche besitzen **URL**, **API-Key**, Modell-Preset, freies Modell, Reasoning-Stufe, Temperature und Fast Mode. Das freie Modell überschreibt das Preset. Reasoning und Temperature dürfen nur in einer Kombination verwendet werden, die das gewählte Modell unterstützt; bei Unsicherheit `auto` beziehungsweise eine leere Reasoning-Stufe verwenden.

### AI: Claude

- **URL / API-Key / Modell:** Wählen Anthropic-Endpunkt und Claude-Modell.
- **Max Tokens:** Obergrenze der generierten Antwort. Ein zu kleiner Wert kann eine Titelliste abschneiden.
- **Temperature:** Variabilität der Antwort, soweit vom Modell unterstützt.
- **Anthropic-Version:** API-Versionsheader. Nur ändern, wenn die verwendete Anthropic-Schnittstelle dies verlangt.
- **Thinking aktivieren / Budget Tokens:** Reserviert bei unterstützten Modellen ein eigenes Denkbudget; das Budget erhöht Laufzeit und Verbrauch.
- **Fast Mode:** Verwendet eine kürzere Retry-/Delay-Strategie.

### Dienste: TIDAL

- **Direkte TIDAL-Integration aktivieren:** Blendet die eigenen TIDAL-Bereiche ein und erlaubt Suche, Mix-/Playlist-Synchronisierung, Hörbuchsuche und `T+`. Ein TIDAL-Konto innerhalb von Roon bleibt von diesem Schalter unberührt.
- **Client-ID / Client-Secret:** OAuth-Clientdaten der App. Sie werden lokal und im App-Backup gespeichert.
- **Verbinden / TIDAL autorisieren:** Startet die Gerätefreigabe, zeigt den Code und öffnet die TIDAL-Bestätigungsseite.
- **Trennen:** Entfernt die gespeicherte App-Anmeldung und leert die lokale Mixauswahl; das TIDAL-Konto in Roon wird nicht getrennt.

### Dienste: Last.fm

- **Mood-Hinweise aktivieren:** Ergänzt gefundene Titel über Last.fm-Tags und kann die Last.fm-Playlistquelle beziehungsweise Stimmungszuordnung bereitstellen.
- **API-Key:** Ohne Schlüssel bleiben Last.fm-Abfragen und der zugehörige Umschalter deaktiviert.
- **Tag-Liste neu einlesen / editieren:** Lädt die gespeicherte Liste erneut oder öffnet den Editor für die auf der Playlist-Seite angebotenen Last.fm-Tags. Änderungen sollten validiert werden.

### Dienste: Deezer

- **Deezer aktivieren:** Nutzt die schlüssellose API als zusätzliche Quelle für Cover, Interpretenbilder und Releasedaten.
- **Bei Cover-Nachfüllung bevorzugen:** Setzt Deezer vor Last.fm in den entsprechenden Coverablauf. Die allgemeine Interpretenbildreihenfolge wird weiterhin separat unter Wrapped verwaltet.
- **Timeout:** Maximale Wartezeit je Anfrage. Höhere Werte tolerieren langsame Antworten, niedrigere brechen früher ab.
- **Tag-Liste neu einlesen / editieren:** Verwaltet die Chips der Deezer-Playlistquelle.

### Dienste: fanart.tv und AI-Tagliste

- **fanart.tv aktivieren:** Schaltet hochwertige Künstlerporträts und Hintergründe frei.
- **Project API Key:** Erforderlicher Schlüssel. **Personal API Key** ist optional und ersetzt den Project Key nicht.
- **Timeout:** Gemeinsame maximale Wartezeit für fanart.tv- und notwendige MusicBrainz-Abfragen.
- **AI-Tag-Liste:** Steuert die Genre-Chips der KI-Playlistquelle. Der zweite Wert jeder Editorzeile wird in den KI-Prompt übernommen.

Weitere automatische Quellen wie MusicBrainz/Cover Art Archive und TheAudioDB besitzen in dieser Version keine eigenen allgemeinen Dienstefelder; ihre Nutzung ergibt sich aus dem jeweiligen Metadaten- oder Bildablauf.

### Wrapped: Zählregeln

- **Polling-Intervall:** Abstand der lokalen Statusprüfung. Kürzer reagiert schneller, erzeugt aber mehr Last; der zulässige Bereich liegt zwischen einer und 30 Sekunden.
- **Pause-Timeout:** Nach dieser ununterbrochenen Pausenzeit wird eine Hörsitzung geschlossen.
- **Mindesthörzeit:** Fallback für Titel ohne bekannte Dauer, besonders Live Radio.
- **Mindesthöranteil:** Prozentualer Anteil bei bekannter Titellänge, ab dem ein Play regulär gezählt wird.
- **Short Track Seconds / Short Track Min Ratio:** Vorhandene Legacy-Felder früherer Kurztrackregeln. Sie haben in der aktuellen Zähllogik keine Wirkung und sollten normalerweise unverändert bleiben.
- **Replay Window:** Zeitfenster, innerhalb dessen eine erneute Wiedergabe als Replay ausgewertet wird.
- **Max Stored Sessions:** Obergrenze des lokalen Verlaufs. Wird sie überschritten, können die ältesten Sitzungen entfernt werden.

Änderungen dieser Regeln wirken auf neue beziehungsweise noch offene Sitzungen. Historische Ergebnisse werden dadurch nicht automatisch neu berechnet.

### Wrapped: Interpretenbilder

- **Suchreihenfolge der Bildanbieter:** Aktivierte Anbieter werden von oben nach unten geprüft; der erste brauchbare Treffer gewinnt. Einzelne Anbieter können deaktiviert und mit Pfeilen verschoben werden. Manuell festgelegte Bilder haben Vorrang.
- **Gespeicherte Bilder suchen:** Durchsucht zunächst nur lokale Zuordnungen eines Interpreten.
- **Bei „Neu suchen“ auch Roon einmalig abfragen:** Erlaubt für die gezielte Neusuche zusätzlich eine Roon-Abfrage.
- **Bildaktionen:** Gefundene Bilder lassen sich festlegen, interpretenbezogen ablehnen, wieder zulassen oder durch JPEG, PNG beziehungsweise WebP zwischen 10 KB und 3 MB ersetzen.

Die komplette Bedienlogik steht in [Kapitel 11](#11-cover-und-interpretenbilder).

### Wrapped: Datenverwaltung

- **Wrapped-Daten vervollständigen:** Führt fehlende Alben, fehlende Cover und lokale Bildkopien in dieser Reihenfolge vollständig aus.
- **Automatisch vervollständigen:** Startet denselben Ablauf sofort und prüft danach alle fünf Minuten auf neue Lücken.
- **Lauf stoppen:** Beendet den aktiven Schritt nach der gerade laufenden Provideranfrage.
- **Unbekannte Alben ermitteln / Cover nachfüllen / Externe Cover lokalisieren:** Starten die drei Phasen einzeln für Diagnose oder gezielte Wartung.
- **Artistbilder fanart.tv:** Bewertet vorhandene Wrapped-Künstlerbilder vorsichtig gegen fanart.tv neu.
- **Roon-Bildcache füllen:** Übernimmt bekannte Roon-Bildschlüssel gedrosselt in den lokalen Cache. Limit bestimmt die Bilder pro Durchlauf, Auto-Pause den Abstand automatischer Batches. **Auto-Roon-Bildcache starten** setzt diese Batches mit den festgelegten Pausen fort und lässt sich wieder stoppen.
- **Externe Cover pro Schritt:** Begrenzt die Batchgröße auf 25, 50 oder 100 Bilder.
- **Cover-Suche zurücksetzen:** Setzt nur den gespeicherten Fortschritt der Nachfüllung zurück und ermöglicht eine erneute Prüfung.
- **Skips bereinigen:** Entfernt historische Skip-Markierungen aus Test- beziehungsweise Altbeständen.
- **Wrapped-Daten löschen:** Löscht den vollständigen Wrapped-Bestand unwiderruflich. Vorher ein Backup erstellen.
- **Offene Cover verwalten:** Gruppiert ungelöste Titel und erlaubt Metadatenkorrektur, gezielte Neusuche oder bestätigte Löschung der betroffenen Wiedergaben.

Fortschrittsbalken und Zähler unterscheiden geprüfte Titel, Treffer und noch offene Kandidaten. Ausführliche sichere Abläufe stehen in [Kapitel 10](#10-roon-wrapped).

### Remote

Der Bereich enthält drei voneinander unabhängige Systeme:

- **Roon-Dummy-Zonen-Proxy:** Aktivierung, Musik-, Hörbuch- und Dummy-Zone, Standardziel und Speicherung des letzten Ziels. **Konfiguration prüfen**, **Status aktualisieren** und **Dummy synchronisieren** kontrollieren Markerqueue, aktives Ziel, letzten Befehl und Latenz. Siehe [Kapitel 15](#15-fernbedienungs-proxy).
- **Netzwerk-Trigger:** Jeder Trigger besitzt Aktivierung, Namen, eine oder mehrere Zonen, optionalen EIN- und/oder AUS-HTTP-GET-Befehl und gegebenenfalls eine Ausschaltverzögerung. Konfiguration, beide Richtungen und Live-Status werden pro Trigger geprüft; nicht mehr benötigte Trigger lassen sich einzeln löschen. Siehe [Kapitel 14](#14-netzwerk-trigger).
- **IR/WLAN-Slots:** Bis zu zehn Slots mit Aktivierung, optionalem Toggle, sichtbarem Label, Aktion, Zone und abhängig von der Aktion einem Sender- oder Playlistziel. **Ziele laden** aktualisiert Roon-Ziele; **Test** prüft den Slot. Siehe [Kapitel 13](#13-remote-slots).

### Wartung: automatische Backups

- **Automatische Backups aktivieren:** Schaltet die zeitgesteuerte schlanke Sicherung ein.
- **Backupordner:** Zielordner; leer verwendet den Backup-Unterordner der App-Daten.
- **Prüfintervall in Stunden:** Wie häufig kontrolliert wird, ob eine Sicherung nötig ist.
- **Maximales Alter in Stunden:** Spätestens nach diesem Zeitraum wird ein neues Auto-Backup erzeugt.
- **Aufbewahrungsversionen:** Zahl der Auto-Backups, die erhalten bleiben.

Ein Auto-Backup bleibt bewusst kleiner als ein Vollbackup. Inhalt, Schutz und Wiederherstellung sind in [Kapitel 18](#18-sicherung-und-wiederherstellung) beschrieben.

### Wartung: Prüfungen, Export und Import

- **Daten prüfen:** Prüft Paket, zentrale Datenbestände, SQLite-/JSON-Konsistenz und ausgewählte Speicherzustände.
- **Healthcheck:** Prüft unter anderem Roon-Verbindung, Dienste, Medienprozess, Speicher und Konfiguration und zeigt jeden Check mit Status und Details.
- **Backup exportieren:** Erstellt eine normale Sicherung zum Herunterladen.
- **Vollbackup exportieren:** Nimmt zusätzlich Datenbank, Metadaten sowie Bild-/Covercache auf und kann deutlich größer werden.
- **Vollbackup im Backupordner erstellen:** Schreibt dieselbe umfassende Sicherung direkt in den konfigurierten Serverordner.
- **Backup importieren:** Prüft ein ZIP- oder kompatibles älteres JSON-Backup vor der Übernahme. Laufende Medienwartung und Hörbuchaufnahme vorher beenden.
- **API-Token testen:** Prüft den aktuell verwendeten Zugriffsschutz.
- **Gespeicherten Token löschen:** Entfernt nur den lokal gespeicherten Client-Token; der Servertoken selbst bleibt bestehen.

Während eine Sicherung läuft, sind weitere Backupaktionen gesperrt. Der sichtbare Fortschritt nennt Arbeitsschritt, Datenquelle, Zähler und Laufzeit.

### Speichern & Logs

- **Änderungen speichern:** Validiert und speichert die Serverkonfiguration. Host- oder Portänderungen können den App-Dienst neu starten.
- **Neu laden:** Lädt den gespeicherten Zustand erneut und verwirft ungespeicherte Formularänderungen.
- **Defaults laden:** Füllt das Formular mit Standardwerten; erst Speichern übernimmt sie dauerhaft. Vor größeren Rücksetzungen ein Backup anlegen.
- **Log öffnen / sofort löschen:** Öffnet beziehungsweise leert das KI-Generierungslog. Die automatische Aufbewahrung wird unter Basis eingestellt.
- **Provider- und Statusfilter:** Begrenzen die sichtbare Generierungsstatistik; **CSV exportieren** speichert diese Auswertung.
- **Fehlerprotokoll:** Bündelt UI-, API-, Netzwerk-, Provider- und Serverfehler mit Zeit, Bereich, Details und Häufigkeit. Aktualisieren liest neu ein; Löschen entfernt den vorhandenen Fehlerbestand.

Das Fehlerprotokoll ist eine Diagnosehilfe. Einzelne Netzwerk- oder Providerfehler können vorübergehend sein; wiederholte Fehler zusammen mit Zeitpunkt und zuvor verwendeter Funktion sind für die Ursachenanalyse aussagekräftiger.

## 18. Sicherung und Wiederherstellung

### Was eine App-Sicherung enthält

Je nach Sicherungsart können enthalten sein:

- App-Konfiguration,
- Zugangsdaten und Tokens,
- Wrapped-Daten,
- Hörbuchbestand und Fortschritt,
- Remote-Slots und Netzwerk-Trigger,
- Metadaten- und Bildzuordnungen,
- SQLite-Datenbank und portabler Snapshot.

Sicherungen sind vertraulich zu behandeln.

### Manuelle Sicherung

1. **Konfiguration > Wartung** öffnen.
2. Backup-Export starten.
3. Ziel auswählen.
4. Fortschritt und Abschlussmeldung abwarten.
5. Sicherungsdatei an einem geschützten Ort aufbewahren.

Während eine Sicherung läuft, sind weitere Backup-Aktionen gesperrt.

### Wiederherstellung

1. Wenn möglich vorher den aktuellen Stand separat sichern.
2. Keine laufende Medienpflege oder Hörbuchaufnahme aktiv lassen.
3. Wiederherstellung öffnen und Sicherungsdatei wählen.
4. Prüfung der Datei abwarten.
5. Wiederherstellung bestätigen.
6. Nach dem Neustart Roon-Verbindung, Dienste, Zonen und Wartungsstatus prüfen.

Vor jedem App-Update wird eine aktuelle Sicherung empfohlen.

## 19. Speicher und Wartung

### Bild- und Cover-Speicher verschieben

Unter **Konfiguration > Basis > Bild- und Cover-Speicher** werden aktiver Ordner, Größe und Objektanzahl angezeigt.

1. neuen Ordner wählen oder absoluten Pfad eintragen,
2. **Inhalte verschieben** starten,
3. Bestätigung abwarten.

Die App kopiert und prüft die Dateien, bevor sie auf den neuen Speicherort umschaltet. Bei einer Kollision oder einem Prüffehler bleibt der bisherige Bestand erhalten.

### Medienverarbeitung

Providerabfragen, Bilddownloads, Bildprüfung, Hashing und Cache-Arbeiten werden getrennt überwacht. Umfangreiche Coverpflege soll deshalb Player, Roon-Verbindung, Weboberfläche und Netzwerk-Trigger nicht unterbrechen.

### Healthcheck

Der Healthcheck prüft unter anderem:

- Roon-Verbindung,
- zentrale Datenspeicher,
- Medienverarbeitung,
- Cache- und Speicherzustand,
- ausgewählte Konfigurationsfehler.

### Fehlerprotokoll

Das kombinierte Fehlerprotokoll enthält Zeit, Quelle, Bereich, Meldung, Details und Anzahl. Wiederholte identische Fehler können zusammengefasst werden. Für eine Diagnose sind Zeitpunkt, aktive Wiedergabe und die unmittelbar vorher verwendete Funktion besonders wichtig.

## 20. Sicherheit und Datenschutz

- Die App nur in einem vertrauenswürdigen privaten Netzwerk betreiben.
- Für Browser und Viewer einen API-Token verwenden.
- Keine direkte Freigabe des App-Dienstes ins Internet einrichten.
- API-Schlüssel und Tokens nicht in Screenshots oder öffentlichen Dokumenten zeigen.
- Sicherungen wie Passwörter behandeln, da sie Zugangsdaten und Hörhistorien enthalten können.
- Nur benötigte externe Dienste aktivieren.
- Netzwerk-Trigger-Adressen sorgfältig prüfen, weil sie reale Geräte steuern können.

Wrapped, Hörbuchdaten und Bildcaches werden lokal verwaltet. Externe Anfragen entstehen nur durch aktivierte Funktionen und unterliegen zusätzlich den Regeln des jeweiligen Anbieters.

## 21. Fehlerbehebung

### Roon ist nicht verbunden

- Läuft der Roon Core?
- Ist **AI Playlist Generator** unter Roon-Erweiterungen autorisiert?
- Befinden sich beide Systeme im selben Netzwerk?
- Blockiert eine Firewall die Erkennung?
- App-Dienst über das Tray-Menü neu starten.

### Eine Zone fehlt

- Zone in Roon aktivieren und benennen.
- Prüfen, ob sie zu einer anderen Zonengruppe gehört.
- Roon-Verbindung neu aufbauen.
- Danach die Konfiguration der betroffenen Remote- oder Triggerfunktion aktualisieren.

### Queue-Anzahl ist sichtbar, aber Titel fehlen

- Kurz auf das Queue-Update warten.
- Prüfen, ob tatsächlich ein weiterer Titel existiert.
- Nach einem Roon-Core-Neustart die App-Verbindung neu herstellen.

### KI-Playlist wird nicht erzeugt

- Ist KI in der Konfiguration aktiviert?
- Anbieter, Modell und Zugangsdaten prüfen.
- Verbindungstest ausführen.
- Bei Ollama auf einem anderen Rechner dessen LAN-Adresse statt `localhost` verwenden.

### TIDAL-Suche oder `T+` funktioniert nicht

- TIDAL-Verbindung und Anmeldung prüfen.
- Zielplaylist für die Zone kontrollieren.
- Sicherstellen, dass der aktuelle Inhalt als Musiktitel erkannt wurde.
- Providerfehler im Log prüfen.

### Live Radio zeigt keine Ergänzungen

- Sendermodus prüfen: `A` deaktiviert externe Anreicherung.
- Prüfen, ob Interpret und Titel überhaupt als Musik erkennbar sind.
- Bei `V` bleibt die Anzeige wie bei Normal; nur Wrapped ist vorsichtiger.
- Bei einem Jingle oder Werbesegment ist eine fehlende Suche beabsichtigt.

### Live Radio zeigt einen falschen Treffer

- Rohangaben des Senders und den aktuellen Titelwechsel prüfen.
- Auf beschädigte Zeichen oder vertauschte Felder achten.
- Providerfehler beziehungsweise besten Kandidaten im Log ansehen.
- Falls der Eintrag in Wrapped liegt, Metadaten unter **Offene Cover verwalten** korrigieren und neu suchen.

### Interpretenbild fehlt

- Anbieterreihenfolge prüfen.
- Sicherstellen, dass mindestens ein Anbieter aktiv ist.
- Namen zuerst als vollständige Künstleridentität suchen lassen.
- Gezielte Neusuche starten.
- Falls nötig ein eigenes Bild festlegen.

### Wrapped enthält einen Titel nicht

- Prüfen, ob Wrapped aktiviert ist.
- War die Wiedergabe lang genug, um als qualifiziert zu gelten?
- Handelt es sich um ein Hörbuch, Jingle oder anderes gefiltertes Segment?
- Bei Live Radio den Sendermodus prüfen.
- Im vorsichtigen Modus ist ohne verwertbaren Treffer keine Aufnahme vorgesehen.

### Wrapped-Cover bleibt offen

- **Wrapped-Daten vervollständigen** ausführen.
- Danach **Offene Cover verwalten** öffnen.
- Schreibweise von Interpret, Titel und Album korrigieren.
- Gezielte Neusuche starten oder eigenes Bild verwenden.

### Hörbuchkapitel sind unvollständig

- Hörbuch erneut synchronisieren.
- Analyse erneut ausführen.
- Prüfen, ob Roon das Buch als zusammenhängendes Album darstellt.
- Browse- oder Verbindungsfehler im Wartungslog prüfen.

### Hörbuchaufnahme startet nicht

- **System prüfen** erneut ausführen.
- Exklusive Zone, Eingabegerät, Zielordner und Speicherplatz prüfen.
- Zusätzliche Roon-Erweiterung autorisieren.
- Sicherstellen, dass das Buch synchronisiert und vollständig analysiert wurde.

### Netzwerk-Trigger reagiert nur auf Test

- Ist der Trigger aktiviert und der richtigen Zone zugeordnet?
- Wurde seit der letzten manuellen AUS-Aktion ein echter neuer Wiedergabestart erkannt?
- Zustand Playing/Loading in der Triggerkarte prüfen.
- Bei Gruppen kontrollieren, ob eine andere Zone noch aktiv ist.
- EIN- und AUS-Konfiguration sowie Schedulerstatus prüfen.

### Browser oder Viewer meldet offline

- Serveradresse und Port prüfen.
- API-Token kontrollieren.
- Firewall und Netzwerkverbindung prüfen.
- Im Viewer **Verbindung einrichten** und **Verbindung testen** verwenden.
- Danach vollständig neu laden.

## 22. Empfohlener Einrichtungsablauf

Für eine neue Installation hat sich folgende Reihenfolge bewährt:

1. Roon verbinden und Zonen im Player prüfen.
2. Sprache und UI-Zoom einstellen.
3. API-Token und sicheren LAN-Zugriff konfigurieren, falls Browser oder Viewer genutzt werden.
4. Nur benötigte externe Dienste aktivieren und einzeln testen.
5. TIDAL-Zielplaylisten pro Zone festlegen.
6. Live-Radio-Sender laden und deren Modi auswählen.
7. Wrapped aktivieren und gewünschte Regeln festlegen.
8. Interpretenbild-Anbieter sortieren.
9. Hörbücher synchronisieren und analysieren.
10. Remote-Slots und Netzwerk-Trigger einzeln einrichten und testen.
11. Bildspeicher festlegen.
12. Healthcheck ausführen.
13. Erste vollständige Sicherung erstellen.

Damit ist die Kernfunktion geprüft, bevor automatische Datenpflege, Hörbuchaufnahme oder externe Gerätesteuerung dauerhaft aktiviert werden.
