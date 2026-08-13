# Erste Schritte

## Voraussetzungen

- Windows 10 oder Windows 11, 64 Bit
- ein erreichbarer Roon Core im selben lokalen Netzwerk
- die Berechtigung, Erweiterungen in Roon zu autorisieren
- optionale Zugangsdaten nur für die Dienste, die tatsächlich verwendet werden sollen
- für kostenlose automatische KI-Playlisten: Google Antigravity CLI auf demselben Windows-System und ein Google-Konto für die einmalige Anmeldung

## Erster Start

Der Windows-Installer bietet zunächst zwei Betriebsarten an:

- **Vollständige App:** zentraler App-Dienst und vollständige lokale Player-Oberfläche.
- **Nur Server + Konfiguration:** zentraler App-Dienst ohne dauerhaft geladenen lokalen Player; vorgesehen für die Bedienung über Browser oder RoonAIViewer.

Beide Modi stellen dieselben Roon-, Wrapped-, Automations-, Medien- und Hörbuchaufnahmefunktionen bereit. Im Modus Nur Server + Konfiguration wird die lokale Konfiguration bei Bedarf über das Symbol im Windows-Infobereich geöffnet.

Beim ersten Start führt ein Assistent durch die wichtigsten Einstellungen:

1. vorhandene App-Sicherung wiederherstellen oder eine neue Einrichtung beginnen
2. Roon Core suchen und die Erweiterung in **Roon > Einstellungen > Erweiterungen** autorisieren
3. lokalen Zugriff oder sicheren Zugriff aus dem Heimnetz festlegen
4. gewünschte Zusatzdienste aktivieren oder überspringen
5. Wiedergabezone auswählen und Verbindung prüfen
6. Konfiguration speichern

Der Einrichtungsassistent kann später erneut über die Konfiguration geöffnet werden.

## Empfohlene Reihenfolge nach der Einrichtung

1. Im Player prüfen, ob alle gewünschten Roon-Zonen erscheinen.
2. Eine normale Wiedergabe starten und Cover, Metadaten und Warteschlange kontrollieren.
3. Gewünschte Live-Radio-Sender in Roon Tools laden und deren Metadatenmodus festlegen.
4. Wrapped aktivieren und den gewünschten Auswertungszeitraum wählen.
5. Optional Hörbücher synchronisieren und analysieren.
6. Optional Interpretenbild-Anbieter sortieren und externe Dienste verbinden.
7. Für kostenlose automatische KI-Playlisten unter **Konfiguration > AI** **Antigravity** wählen, **Anmeldung öffnen** abschließen, **CLI prüfen**, ein Modell wählen und speichern.
8. Eine erste App-Sicherung erstellen.

Antigravity benötigt keinen KI-API-Key. Nach der Einrichtung überträgt die lokale CLI Playlistwunsch und Ergebnis automatisch. Es gelten Googles jeweils aktueller kostenloser Tarif, die Modellverfügbarkeit und die Nutzungskontingente; die App kauft niemals Credits.

## Zugriff aus dem Heimnetz

Für Browser oder RoonAIViewer muss der App-Dienst Verbindungen aus dem lokalen Netzwerk annehmen. Der verwendete Port muss auf dem Serverrechner in der Firewall erreichbar sein. Für diesen Betrieb sollte ein API-Token eingerichtet und nur in einem vertrauenswürdigen privaten Netzwerk verwendet werden.

Für diese Anordnung eignet sich der Modus Nur Server + Konfiguration besonders gut: Dienst und Hintergrundfunktionen bleiben aktiv, ohne ein dauerhaftes lokales Playerfenster zu laden. Der Betriebsmodus kann später unter **Konfiguration > Basis** geändert werden; nach dem Speichern startet die Desktop-App neu.

## Updates

Vor einem Update sollte eine aktuelle Sicherung erstellt werden. Nach der Installation bleiben die vorhandenen Einstellungen und lokalen Daten normalerweise erhalten. Nach dem ersten Start der neuen Version sollten Roon-Verbindung, Playeransicht und Wartungsstatus kurz geprüft werden.

Die ausführliche Bedienung aller App-Bereiche steht im [vollständigen Benutzerhandbuch](BENUTZERHANDBUCH_DE.md).
