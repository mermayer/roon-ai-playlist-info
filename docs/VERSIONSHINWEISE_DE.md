# Versionshinweise

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

## Roon AI Playlist 1.0.458

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
