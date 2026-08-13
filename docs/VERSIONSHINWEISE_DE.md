# Versionshinweise

## Informations- und Dokumentationsausgabe 1.0.3 — 13. August 2026

- die neue Installer-Auswahl zwischen Vollständige App und Nur Server + Konfiguration dokumentieren
- die vorgesehene Anordnung mit dauerhaft laufendem Server und RoonAIViewer oder Browser auf einem anderen System erklären
- beschreiben, dass der Servermodus kein vollständiges lokales Playerfenster dauerhaft lädt und die lokale Konfiguration nur bei Bedarf öffnet
- bestätigen, dass beide Modi dieselbe Konfiguration, Roon-Verbindung, SQLite-Daten, Caches, Hintergrund-Worker und Sicherungen verwenden
- bestätigen, dass Roon-Steuerung, Wrapped, Medienverarbeitung, Netzwerk-Trigger, Remote-Slots, geplante Abläufe und Hörbuchaufnahme im Servermodus weiterlaufen
- den späteren Wechsel des Desktop-Betriebsmodus mit anschließendem kontrolliertem App-Neustart erklären
- den dokumentierten App-Stand auf 1.0.466 aktualisieren

## Informations- und Dokumentationsausgabe 1.0.2 — 6. August 2026

- die kostenlose vollautomatische KI-Playlist-Erzeugung mit Google Antigravity CLI an exponierter Stelle in der öffentlichen Übersicht darstellen
- dokumentieren, dass nach der Einrichtung weder KI-API-Key, nutzungsabhängiges API-Konto noch manueller Kopier-/Einfügeschritt erforderlich sind
- Installation auf dem App-System, einmalige Google-Anmeldung, **CLI prüfen**, echte Modellauswahl, kontospezifische `agy models`-Einträge, Denktiefen und zukünftige freie Modell-IDs erklären
- den derzeitigen kostenlosen Zugang zu hochwertigen Gemini-Modellen beschreiben und gleichzeitig Modellverfügbarkeit sowie Kontingente klar als Google-Leistung kennzeichnen
- die automatische Übergabe in den unveränderten Roon-Abgleich, die Ersatzlogik, Ergebnisprüfung und Wiedergabebestätigung erläutern
- festhalten, dass die App keine Credits kauft und vorhandene kostenpflichtige G1-/AI-Credits standardmäßig blockiert
- den dokumentierten App-Stand auf 1.0.463 aktualisieren

## Informations- und Dokumentationsausgabe 1.0.1 — 4. August 2026

- erklären, wie die eigenständige native macOS-App SpotBridge 1.0.0 lokale Spotify-Wiedergabe an Roon Audio Input übergibt
- AAC und verlustfrei codiertes Ogg-FLAC für den Bridge-Transport, übermittelte Metadaten und Cover sowie die optionale Transportkoordination zwischen Spotify und Roon dokumentieren
- die Aufgaben von SpotBridge bei der Audioaufnahme klar von Darstellung und Wrapped-Funktionen in Roon AI Playlist abgrenzen
- einen klaren Rechtehinweis für die eigene Dokumentation ergänzen und Marken, Cover, Bilder sowie andere eingebettete Fremdinhalte davon ausnehmen
- deutsche und englische Änderungsprotokolle für öffentliche Informationsausgaben einführen

## Informations- und Dokumentationsausgabe 1.0.0 — 4. August 2026

Dies ist die erste öffentliche Informationsausgabe zu Roon AI Playlist. Sie enthält weder einen Installer noch Quellcode.

- englische Standard-Startseite und vollständige deutschsprachige Entsprechung
- umfangreiche Übersicht darüber, wie Roon AI Playlist das originale Roon ergänzt
- vollständige Benutzerhandbücher in Deutsch und Englisch
- feldgenaue Referenz aller aktuellen Konfigurationsbereiche
- eigenes RoonAIViewer-Handbuch
- Dokumente zu ersten Schritten, Datenschutz, Sicherheit, häufigen Fragen und App-Überblick
- Screenshots und Erklärungen zu Mehrzonenplayer, KI- und Last.fm-Playlisten, Live Radio, Spotify, TIDAL-Mixen und -Playlisten, Hörbuchsuche, Wrapped, Netzwerk-Triggern, Remote-Slots und RoPieee-Proxy
- klare Produktabgrenzung: Die App ergänzt Roon außerhalb seiner Oberfläche innerhalb der Möglichkeiten der Roon-Extension-APIs und ersetzt Roon nicht

## Roon AI Playlist 1.0.466

Zu den neu dokumentierten App-Funktionen gehören:

- im Windows-Installer wählbarer Betriebsmodus Vollständige App oder Nur Server + Konfiguration
- ressourcenschonender Dauerbetrieb ohne dauerhaft geladenes lokales Playerfenster
- lokale Konfiguration bei Bedarf über den Windows-Infobereich öffnen und nach dem Schließen wieder freigeben
- späterer Wechsel des Betriebsmodus über die Konfiguration mit kontrolliertem App-Neustart
- unveränderter Zugriff auf die vollständige Oberfläche über Browser und RoonAIViewer
- unveränderte serverseitige Funktionen für Roon, Wrapped, Automation, Medien-Worker und Hörbuchaufnahme

Die für App-Version 1.0.463 dokumentierten Antigravity-Funktionen bleiben Bestandteil der aktuellen App:

- vollautomatische Playlist-Erzeugung über Google Antigravity CLI auf demselben Windows-System
- API-Key-freier Betrieb nach einmaliger Anmeldung mit einem Google-Konto
- auswählbare Denktiefen für Gemini 3.6 Flash, Gemini 3.5 Flash und Gemini 3.1 Pro sowie kontospezifische und freie zukünftige Modelle
- Gemini 3.1 Pro (High) als praktisch bewährte qualitätsorientierte Voreinstellung
- Diagnose von CLI, Anmeldung, Kontingent und Modell über **CLI prüfen**
- automatische strukturierte Ergebnisübergabe an die vorhandene Roon-Suche und Ersatzlogik
- Schutz vor unbeabsichtigter Verwendung bereits aktivierter kostenpflichtiger Antigravity-Credits

Der für 1.0.458 dokumentierte Funktionsumfang bleibt ebenfalls Bestandteil der aktuellen App:

### Bereits mit 1.0.458 dokumentierte Funktionen

Der dokumentierte Funktionsstand umfasst unter anderem:

- stabilere Medienverarbeitung bei umfangreichen Cover- und Interpretenbildsuchen
- getrennte Verarbeitung von Medienaufgaben, damit Player, Roon-Verbindung und Netzwerk-Trigger erreichbar bleiben
- konfigurierbare Reihenfolge der Interpretenbild-Anbieter
- verbesserte gemeinsame Suche nach Duos und Künstlergruppen
- Live-Radio-Modi Normal, Vorsichtig und Aus mit identischer Suche in Normal und Vorsichtig
- verbesserte Live-Radio-Erkennung, Zeichensatzreparatur und Filterung von Nicht-Musik-Inhalten
- Verwaltung weiterhin offener Wrapped-Cover mit Korrektur, Neusuche und Löschung
- gemeinsamer Ablauf zur Vervollständigung von Wrapped-Alben und -Covern
- SQLite als primärer Wrapped-Speicher mit portablem Sicherungsstand
- automatische und manuelle Sicherungen mit sichtbarem Fortschritt
- Hörbuchfortschritt, Lesezeichen und optionale kapitelweise Aufnahme
- Netzwerk-Trigger mit manuellem AUS-Schalter und sicherem Scheduler-Verhalten
- ausführliche Zustands- und Wartungsanzeigen

## RoonAIViewer 1.0.3

- eigener Windows-Client für eine entfernte Roon-AI-Playlist-Installation
- Verbindungstest vor dem Speichern
- verschlüsselte Token-Speicherung für das aktuelle Windows-Benutzerkonto
- dauerhaft gespeicherter Zoom von 90 bis 130 Prozent
- optionaler Windows-Autostart und minimierter Start im Infobereich
- echtes Neuladen über Tray-Menü, `F5` und `Strg+R`
- automatische Wiederherstellung einer fälschlich als offline angezeigten Seite nach erfolgreicher Serverprüfung
- saubere Deinstallation mit optionaler Entfernung von Einstellungen und Browserprofil
