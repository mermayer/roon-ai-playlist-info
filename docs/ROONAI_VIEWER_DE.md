# RoonAIViewer – Benutzerhandbuch

## Was ist RoonAIViewer?

RoonAIViewer ist ein schlanker Windows-Client für eine Roon-AI-Playlist-Installation auf einem anderen Rechner. Er zeigt die vollständige Weboberfläche in einem eigenen Windows-Fenster an und eignet sich besonders für einen zweiten PC, ein Windows-Tablet oder ein festes Musikdisplay.

Der Viewer betreibt keinen eigenen App-Dienst und verbindet sich nicht selbst mit der Roon API. Deshalb entsteht durch ihn keine zusätzliche Roon-Zonenabfrage. Wiedergabe, Metadaten, Wrapped und alle Aktionen werden weiterhin vom zentralen Roon-AI-Playlist-System bereitgestellt.

## Wann ist der Viewer sinnvoll?

RoonAIViewer ist besonders geeignet, wenn:

- Roon AI Playlist dauerhaft auf einem anderen Computer läuft,
- die Oberfläche auf einem Windows-Gerät wie eine eigenständige App verwendet werden soll,
- ein Browser mit Adressleiste und Tabs unerwünscht ist,
- das Fenster nach dem Schließen im Infobereich verfügbar bleiben soll,
- Zoom und Verbindung dauerhaft gespeichert werden sollen,
- die Oberfläche automatisch mit Windows starten soll.

Für eine gelegentliche Nutzung ohne Installation genügt weiterhin ein normaler Browser.

## Unterschiede zur vollständigen App, zum Servermodus und zum Browser

| Eigenschaft | Vollständige Windows-App | Nur Server + Konfiguration | Browser | RoonAIViewer |
|---|---:|---:|---:|---:|
| enthält den zentralen App-Dienst | ja | ja | nein | nein |
| Verbindung direkt zur Roon API | über den App-Dienst | über den App-Dienst | nein | nein |
| vollständiges lokales Playerfenster | ja | nein | Browserfenster | ja |
| lokale Konfiguration | ja | bei Bedarf über Infobereich | nein | nein |
| Zugriff auf entfernten App-Dienst | möglich | nicht zutreffend | ja | ja |
| Tray-Betrieb | ja | ja | nein | ja |
| Windows-Autostart | ja | ja | browserabhängig | ja |
| dauerhaft gespeicherter Zoom | ja | nur Konfigurationsfenster | browserabhängig | ja, 90–130 % |
| geschützte lokale Token-Speicherung | ja | ja | browserabhängig | ja |

## Voraussetzungen

- Windows 10 oder Windows 11, 64 Bit
- .NET Framework 4.8
- Microsoft Edge WebView2 Evergreen Runtime
- Netzwerkzugriff auf den Rechner, auf dem Roon AI Playlist läuft
- Serveradresse einschließlich Port
- API-Token, sofern am Server aktiviert

WebView2 ist unter Windows 11 normalerweise vorhanden und auf vielen Windows-10-Systemen bereits installiert. Fehlt die Laufzeit, kann sie während der Viewer-Installation nachinstalliert werden; dafür ist einmalig eine Internetverbindung erforderlich.

## Vorbereitung des Serverrechners

Bevor der Viewer eingerichtet wird:

1. Roon AI Playlist auf dem Serverrechner starten.
2. Für ein dauerhaft entfernt bedientes System bei der App-Installation oder später unter **Konfiguration > Basis** den Modus **Nur Server + Konfiguration** wählen.
3. Sicherstellen, dass die App Verbindungen aus dem lokalen Netzwerk annimmt.
4. Den verwendeten Port in der Firewall des Serverrechners freigeben.
5. Für den Netzwerkzugriff ein API-Token konfigurieren.
6. Servername oder lokale IP-Adresse und Port notieren.

Der Server sollte nur in einem vertrauenswürdigen privaten Netzwerk erreichbar sein. Eine direkte Freigabe ins Internet ist nicht vorgesehen.
Nur Server + Konfiguration ist optional, verhindert aber, dass auf dem Serverrechner zusätzlich eine vollständige Player-Oberfläche geladen bleibt. Viewer-Funktionen und die serverseitige Hörbuchaufnahme werden dadurch nicht eingeschränkt.

## Installation

1. Den separat bereitgestellten RoonAIViewer-Installer starten.
2. Bei Bedarf den Installationsordner ändern.
3. Installation abschließen.
4. RoonAIViewer über Desktop oder Startmenü öffnen.

RoonAIViewer wird in **Windows > Installierte Apps** eingetragen.

## Erste Verbindung

Beim ersten Start öffnet sich die Verbindungseinrichtung:

1. Serveradresse eingeben, beispielsweise `http://roon-server:3000` oder eine lokale IP-Adresse mit Port.
2. Das am Server konfigurierte API-Token eintragen. Ohne Tokenschutz bleibt das Feld leer.
3. **Verbindung testen** wählen.
4. Den gewünschten Oberflächen-Zoom zwischen 90 und 130 Prozent einstellen.
5. Optional **Mit Windows starten** aktivieren.
6. Optional festlegen, dass der Viewer beim Windows-Start minimiert im Infobereich beginnt.
7. Einstellungen speichern.

Nach erfolgreicher Prüfung öffnet der Viewer die vom Server bereitgestellte Oberfläche.

## Tägliche Bedienung

- Ein Linksklick auf das Viewer-Symbol im Windows-Infobereich öffnet oder aktiviert das Fenster.
- Das Schließen des Fensters versteckt den Viewer im Infobereich. Der entfernte App-Dienst und Roon laufen unverändert weiter.
- **Beenden** im Menü des Infobereichs beendet nur den Viewer.
- **Neu laden**, `F5` und `Strg+R` laden die Oberfläche vollständig neu.
- **Im Standardbrowser öffnen** öffnet dieselbe Serveroberfläche im normalen Browser.
- Externe Links werden automatisch an den Windows-Standardbrowser übergeben.
- **Verbindung einrichten** öffnet Serveradresse, Token, Zoom und Autostart-Einstellungen erneut.

## Zoom und Darstellung

Der Viewer speichert einen Zoomwert von 90 bis 130 Prozent in Zwei-Prozent-Schritten. Änderungen über `Strg` und Mausrad werden ebenfalls gespeichert und beim nächsten Start wiederhergestellt.

Ein kleinerer Zoom zeigt mehr Inhalte und eignet sich für niedrige Auflösungen. Ein größerer Zoom verbessert die Lesbarkeit auf Touchgeräten oder bei größerem Betrachtungsabstand. Die eigentlichen Layoutoptionen der Roon-AI-Playlist-Oberfläche werden weiterhin zentral in deren UI-Konfiguration festgelegt.

## Autostart und minimierter Betrieb

Mit aktiviertem Autostart öffnet Windows den Viewer nach der Anmeldung. Optional kann er dabei zunächst nur im Infobereich erscheinen. Diese Einstellung startet ausschließlich den Viewer; der zentrale App-Dienst muss auf seinem eigenen Rechner bereits verfügbar sein.

## Verbindung und automatische Wiederherstellung

RoonAIViewer prüft die Erreichbarkeit des Servers unabhängig von der angezeigten Webseite. Meldet die Oberfläche irrtümlich **Server offline**, obwohl die native Prüfung erfolgreich ist, lädt der Viewer die Seite einmal automatisch neu.

Bei einem echten Serverausfall bleibt der Viewer geöffnet. Sobald Server und Netzwerk wieder verfügbar sind, kann die Oberfläche über **Neu laden**, `F5` oder `Strg+R` erneut verbunden werden.

## Sicherheit und lokale Daten

Der API-Token wird mit dem Windows-Datenschutzmechanismus DPAPI für das aktuelle Benutzerkonto verschlüsselt gespeichert. Andere Windows-Benutzer können diesen gespeicherten Wert nicht ohne Weiteres verwenden.

Gespeicherte Verbindungseinstellungen befinden sich im Benutzerprofil unter:

- `%APPDATA%\RoonAIViewer\settings.xml`

Das lokale Browserprofil befindet sich unter:

- `%LOCALAPPDATA%\RoonAIViewer\WebView2`

Der Viewer speichert keine eigene Roon-Bibliothek, keine Wrapped-Daten und keine Hörbuchdaten. Diese Informationen verbleiben auf dem zentralen App-System.

## Fehlerbehebung

### Verbindungstest schlägt fehl

- Serveradresse einschließlich `http://` und Port prüfen.
- Sicherstellen, dass Server- und Viewer-Rechner im selben Netzwerk sind.
- Roon AI Playlist auf dem Serverrechner öffnen und dessen Verbindung prüfen.
- Windows-Firewall des Serverrechners kontrollieren.
- API-Token auf Tippfehler oder versehentliche Leerzeichen prüfen.
- Bei Verwendung eines Rechnernamens testweise die lokale IP-Adresse verwenden.

### Oberfläche bleibt auf „Server offline“

- **Neu laden** im Tray-Menü verwenden.
- `F5` oder `Strg+R` drücken.
- Über **Verbindung einrichten** erneut testen.
- Prüfen, ob sich die Serveradresse im Standardbrowser öffnen lässt.

### Leeres oder weißes Fenster

- Viewer vollständig über **Beenden** schließen und neu starten.
- Microsoft Edge WebView2 Runtime reparieren oder aktualisieren.
- Lokales WebView2-Profil bei der Deinstallation mit entfernen und den Viewer anschließend neu installieren.

### Darstellung ist zu groß oder zu klein

- **Verbindung einrichten** öffnen und den Zoom anpassen.
- Alternativ `Strg` und Mausrad verwenden.
- Prüfen, ob zusätzlich in Roon AI Playlist ein hoher Browser-Zoom eingestellt wurde.

### Viewer startet, der Server aber nicht

Das ist erwartetes Verhalten. Der Viewer startet keinen entfernten Rechner und keinen App-Dienst. Der zentrale Server muss unabhängig vom Viewer laufen.

## Deinstallation

RoonAIViewer kann unter **Windows > Installierte Apps** oder über den Eintrag im Startmenü deinstalliert werden. Während der Deinstallation kann gewählt werden, ob Verbindungseinstellungen und Browserprofil ebenfalls gelöscht werden sollen.

Das Entfernen des Viewers verändert keine Roon-Daten und keine Daten auf dem entfernten Roon-AI-Playlist-System.
