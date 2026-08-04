# Häufige Fragen

## Ersetzt Roon AI Playlist die Roon-Oberfläche oder den Roon Core?

Nein. Die App ergänzt Roon bewusst, statt dessen Oberfläche, Bibliotheksverwaltung, Wiedergabe-Engine, RAAT, DSP, Queues oder normale Steuerung nachzubauen. Sie benötigt einen erreichbaren Roon Core und stellt außerhalb von Roon nur die zusätzlichen Arbeitsabläufe bereit, die sich über die Roon-Extension-APIs ermöglichen lassen.

## Muss ich einen KI-Anbieter verwenden?

Nein. Die KI-Playlistfunktion kann deaktiviert werden. Player, Live Radio, Hörbücher, Wrapped, Roon Tools und andere nicht KI-abhängige Funktionen bleiben verfügbar.

## Kann die App ohne TIDAL verwendet werden?

Ja. TIDAL erweitert Suche, Live-Radio-Erkennung und Playlistenaktionen, ist aber nicht für alle App-Bereiche erforderlich. Je nach Funktion stehen weitere Quellen oder lokale Roon-Daten zur Verfügung.

## Wie gelangt Spotify-Wiedergabe zu Roon AI Playlist?

Über Roon. Die eigenständige native macOS-App SpotBridge kann den lokalen Spotify-Prozess mit einem CoreAudio Process Tap aufnehmen und als AAC oder verlustfrei codiertes Ogg-FLAC an Roon Audio Input senden. SpotBridge übermittelt außerdem Interpret, Titel, Album und Cover und kann Transportereignisse koordinieren. Nachdem der Stream in einer ausgewählten Roon-Zone erscheint, kann Roon AI Playlist ihn darstellen und eine qualifizierte Wrapped-Sitzung erfassen. Roon AI Playlist selbst nimmt kein Spotify-Audio auf und meldet sich nicht bei Spotify an.

Ogg-FLAC erhält das aufgenommene Signal auf dem Weg zu Roon; aus der ursprünglichen Spotify-Quelle wird dadurch kein höherwertiges Audiosignal.

## Warum können Live-Radio-Daten von Roon abweichen?

Radiosender liefern sehr unterschiedliche und teilweise unvollständige Metadaten. Die App versucht Interpret, Titel, Album und Cover über mehrere Quellen zu ergänzen und kann dadurch einen anderen geeigneten Albumtreffer als Roon anzeigen.

## Was bedeuten N, V und A neben einem Radiosender?

- `N` – Normal: Anreicherung und reguläre Wrapped-Aufnahme
- `V` – Vorsichtig: gleiche Anzeige und Suche, aber keine Wrapped-Aufnahme ohne verwertbaren Treffer
- `A` – Aus: keine externe Anreicherung und keine Wrapped-Aufnahme

## Werden Jingles und Werbung in Wrapped gespeichert?

Typische Jingles, Intros, Outros, Nachrichten, Werbung, Senderkennungen und technische Automationsnamen werden möglichst vor der Musikrecherche erkannt und verworfen. Bei mehrdeutigen echten Musikangaben hängt das Ergebnis vom gewählten Sendermodus und den verfügbaren Treffern ab.

## Warum fehlt ein Cover oder Interpretenbild?

Ein Anbieter kann keine Bilder besitzen, die Schreibweise kann abweichen oder ein Treffer kann zu unsicher sein. In der Wrapped- und Interpretenbildverwaltung lassen sich Metadaten korrigieren, Anbieter priorisieren, Treffer neu suchen, Bilder festlegen oder eigene Bilder hinterlegen.

## Wie werden Duos und Gruppen behandelt?

Ein gemeinsamer Name wie „John Travolta & Olivia Newton-John“ wird zuerst als vollständige Einheit gesucht. Erst wenn dafür kein geeigneter Gesamttreffer vorhanden ist, kann die App einzelne Beteiligte prüfen.

## Wo werden Wrapped-Daten gespeichert?

Wrapped-Daten werden lokal auf dem App-System gespeichert. Sie werden nicht vom RoonAIViewer dupliziert.

## Kann ich die App auf einem anderen Rechner bedienen?

Ja. Im Heimnetz kann die Oberfläche in einem Browser oder mit RoonAIViewer geöffnet werden. Dafür muss der App-Dienst Netzwerkzugriff erlauben und sollte mit einem API-Token geschützt sein.

## Ist RoonAIViewer ein zweiter Server?

Nein. Der Viewer zeigt nur die Oberfläche des vorhandenen App-Systems. Er startet keinen App-Dienst, verbindet sich nicht direkt mit Roon und speichert keine eigene Hörhistorie.

## Was geschieht beim Schließen des Viewers?

Das Fenster wird in den Windows-Infobereich ausgeblendet. Erst **Beenden** im Tray-Menü schließt den Viewer vollständig. Der entfernte App-Dienst bleibt in beiden Fällen aktiv.

## Enthält dieses öffentliche Angebot einen Installer?

Nein. Installationsdateien und Quellcode werden nicht öffentlich bereitgestellt.
