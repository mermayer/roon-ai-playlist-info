# Datenschutz und Sicherheit

## Grundprinzip

Roon AI Playlist ist für den lokalen Betrieb im privaten Netzwerk ausgelegt. Zonenstatus, Wrapped-Verlauf, Hörbuchdaten, Einstellungen, Protokolle sowie gespeicherte Cover und Interpretenbilder werden auf dem App-System verwaltet.

## Externe Verbindungen

Netzwerkzugriffe zu externen Diensten entstehen nur, wenn die jeweilige Funktion aktiviert und verwendet wird. Dazu können gehören:

- ein gewählter KI-Anbieter für Playlist-Vorschläge
- Google Antigravity bei Auswahl dieses KI-Weges; die lokale CLI übermittelt den Playlistauftrag im angemeldeten Konto an Googles Dienst
- TIDAL für Suche, Albumaktionen, Hörbuchmetadaten und abonnierte Browserwiedergabe
- Last.fm und Deezer für Musik- und Bildinformationen
- fanart.tv und TheAudioDB für Interpretenbilder
- MusicBrainz und Cover Art Archive für Albumdaten und Cover
- Audible für optionale Hörbuchinformationen
- vom Benutzer konfigurierte lokale oder externe HTTP-Ziele für Netzwerk-Trigger

Welche Suchbegriffe oder Metadaten an einen Anbieter gesendet werden, hängt von der verwendeten Funktion ab. Für optionale Dienste gelten zusätzlich deren eigene Datenschutzbestimmungen.

## Zugangsdaten

API-Schlüssel, Tokens und Anmeldedaten werden in der lokalen App-Konfiguration gespeichert. App-Sicherungen können diese Zugangsdaten enthalten und sollten daher wie Passwörter geschützt aufbewahrt werden.

Die Antigravity-Anmeldung wird von der offiziellen CLI auf dem App-System verwaltet und nicht als KI-API-Key in Roon AI Playlist gespeichert. Die App übermittelt den Playlistwunsch und erhält die erzeugte Titelliste; das Google-Passwort erhält sie nicht. Es gelten Googles Datenschutzbedingungen, Modellverfügbarkeit und Kontokontingente. Kostenpflichtige G1-/AI-Credits sind standardmäßig blockiert und die App löst keinen Credit-Kauf aus.

Im RoonAIViewer wird der Server-Token mit Windows DPAPI an das aktuelle Windows-Benutzerkonto gebunden gespeichert.

## Zugriff im Heimnetz

- Netzwerkzugriff nur in einem vertrauenswürdigen privaten Netzwerk aktivieren.
- Für Browser und RoonAIViewer einen API-Token konfigurieren.
- Nur den tatsächlich benötigten Port in der Firewall freigeben.
- Die App nicht direkt aus dem Internet erreichbar machen.
- Externe HTTPS- oder HTTP-Befehle der Netzwerk-Trigger sorgfältig prüfen.

Vollständige App und Nur Server + Konfiguration verwenden dieselben lokalen Daten und Netzwerkendpunkte. Der Servermodus veröffentlicht keinen zusätzlichen Dienst und kopiert keine Daten zum Viewer; er verzichtet lediglich auf das dauerhaft geladene lokale Playerfenster. Das Schließen seines bei Bedarf geöffneten Konfigurationsfensters beendet den geschützten App-Dienst nicht.

## Lokale Bilder und Hörhistorie

Cover, Interpretenbilder und Providerantworten können lokal zwischengespeichert werden. Wrapped führt eine lokale Hörhistorie, sofern diese Funktion aktiviert ist. Die Wartungsfunktionen ermöglichen die Korrektur und Löschung entsprechender Einträge.

Die virtuelle TIDAL-Hörbuchbibliothek speichert Albumverweise, Kapitel, Fortschritt und Lesezeichen lokal; sie kopiert das abonnierte Audio nicht in die Bibliothek. Direktes Anhören und Schnellaufnahme verwenden den offiziellen TIDAL-Browserplayer in einem getrennt verwalteten lokalen Chrome-Profil. Der eng begrenzte Begleiter koordiniert diesen Player und seinen gewählten Audioausgang, liest jedoch keine TIDAL-Zugangsdaten, Lizenzschlüssel oder geschützten Streamdaten aus. Erfasstes PCM, Geschwindigkeits-/Pitchverarbeitung, temporäre Mastersegmente und erzeugte Kapiteldateien verbleiben auf dem App-System.

## Sicherungen

Eine App-Sicherung dient der Wiederherstellung von Einstellungen und lokalen Daten. Da sie persönliche Hörhistorien und Zugangsdaten enthalten kann:

- Sicherungen nur auf vertrauenswürdigen Datenträgern speichern,
- nicht öffentlich hochladen,
- vor der Weitergabe verschlüsseln oder sensible Bestandteile entfernen,
- alte Sicherungen sicher löschen, wenn sie nicht mehr benötigt werden.

## Unabhängigkeit

Roon AI Playlist ist ein unabhängiges Projekt. Die Nutzung externer Dienste erfordert gegebenenfalls eigene Konten und unterliegt den Bedingungen des jeweiligen Anbieters.
