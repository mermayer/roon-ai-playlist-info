# RoonAIViewer user guide

## What is RoonAIViewer?

RoonAIViewer is a lightweight Windows client for a Roon AI Playlist installation running on another computer. It displays the complete web interface in a dedicated Windows window and is particularly useful on a second PC, Windows tablet, or permanent music display.

The viewer does not run its own application service and does not connect directly to the Roon API. It therefore creates no additional Roon zone queries. Playback, metadata, Wrapped, and all actions continue to be supplied by the central Roon AI Playlist system.

## When is the viewer useful?

RoonAIViewer is a good choice when:

- Roon AI Playlist runs continuously on another computer,
- the interface should behave like a dedicated application on a Windows device,
- browser tabs and an address bar are undesirable,
- the window should remain available in the notification area after being closed,
- zoom and connection details should persist,
- the interface should start automatically with Windows.

A regular browser remains sufficient for occasional use without an installation.

## Comparison with the complete app, server mode, and a browser

| Capability | Complete Windows app | Server + Configuration | Browser | RoonAIViewer |
|---|---:|---:|---:|---:|
| includes the central application service | yes | yes | no | no |
| direct connection to the Roon API | through the application service | through the application service | no | no |
| full local Player window | yes | no | browser window | yes |
| local configuration | yes | on demand from notification area | no | no |
| access to a remote application service | supported | not applicable | yes | yes |
| notification-area operation | yes | yes | no | yes |
| Windows autostart | yes | yes | browser-dependent | yes |
| persistent zoom | yes | configuration only | browser-dependent | yes, 90–130% |
| protected local token storage | yes | yes | browser-dependent | yes |

## Requirements

- 64-bit Windows 10 or Windows 11
- .NET Framework 4.8
- Microsoft Edge WebView2 Evergreen Runtime
- network access to the computer running Roon AI Playlist
- server address including its port
- API token when protection is enabled on the server

WebView2 is normally present on Windows 11 and is already installed on many Windows 10 systems. If it is missing, the runtime can be installed during viewer setup; this one-time step requires an internet connection.

## Preparing the server computer

Before configuring the viewer:

1. Start Roon AI Playlist on the server computer.
2. For a permanently remote-controlled system, select **Server + Configuration** during application installation or later under **Configuration > Basic**.
3. Ensure that it accepts connections from the local network.
4. Allow the selected port through the server computer's firewall.
5. Configure an API token for network access.
6. Note the computer name or local IP address and port.

The server should be accessible only on a trusted private network. Direct exposure to the internet is not intended.
Server + Configuration is optional but avoids keeping a second full Player interface loaded on the server computer. It does not restrict Viewer functions or server-side audiobook capture.

## Installation

1. Run the separately supplied RoonAIViewer installer.
2. Change the installation folder if required.
3. Complete the installation.
4. Open RoonAIViewer from the desktop or Start menu.

RoonAIViewer is registered under **Windows > Installed apps**.

## First connection

The connection setup window opens on first launch:

1. Enter the server address, for example `http://roon-server:3000` or a local IP address and port.
2. Enter the API token configured on the server. Leave the field empty when token protection is disabled.
3. Select **Verbindung testen** to test the connection.
4. Choose an interface zoom between 90 and 130 percent.
5. Optionally enable Windows autostart.
6. Optionally start the viewer minimised in the notification area.
7. Save the settings.

After a successful test, the viewer opens the interface provided by the server.

## Daily use

- Left-click the viewer icon in the Windows notification area to open or activate the window.
- Closing the window hides the viewer in the notification area. The remote application service and Roon continue running.
- **Beenden** in the notification-area menu exits only the viewer.
- **Neu laden**, `F5`, and `Ctrl+R` perform a complete reload.
- **Im Standardbrowser öffnen** opens the same server interface in the normal web browser.
- External links are automatically passed to the Windows default browser.
- **Verbindung einrichten** reopens the server address, token, zoom, and autostart settings.

## Zoom and display

The viewer stores a zoom value from 90 to 130 percent in two-percent steps. Changes made with `Ctrl` and the mouse wheel are also stored and restored on the next launch.

A smaller zoom displays more content and may suit lower resolutions. A larger zoom improves readability on touch devices or at a greater viewing distance. Layout options of the Roon AI Playlist interface itself continue to be managed in its central UI configuration.

## Autostart and minimised operation

With autostart enabled, Windows launches the viewer after sign-in. It can optionally start only in the notification area. This setting launches the viewer only; the central application service must already be available on its own computer.

## Connection and automatic recovery

RoonAIViewer checks server availability independently of the displayed web page. If the interface incorrectly reports **Server offline** while the native check succeeds, the viewer automatically reloads the page once.

During a real server outage, the viewer remains open. When the server and network become available again, use **Neu laden**, `F5`, or `Ctrl+R` to reconnect the interface.

## Security and local data

The API token is encrypted for the current Windows user with Windows DPAPI. Other Windows users cannot readily reuse the stored value.

Connection settings are stored in the user profile under:

- `%APPDATA%\RoonAIViewer\settings.xml`

The local browser profile is stored under:

- `%LOCALAPPDATA%\RoonAIViewer\WebView2`

The viewer stores no independent Roon library, Wrapped history, or audiobook data. This information remains on the central application system.

## Troubleshooting

### Connection test fails

- Check the server address, including `http://` and the port.
- Ensure that the server and viewer computers are on the same network.
- Open Roon AI Playlist on the server computer and verify its connection.
- Check Windows Firewall on the server computer.
- Check the API token for typing errors or unintended spaces.
- If a computer name is used, try the local IP address instead.

### Interface remains on “Server offline”

- Use **Neu laden** in the notification-area menu.
- Press `F5` or `Ctrl+R`.
- Open **Verbindung einrichten** and test again.
- Check whether the server address opens in the default browser.

### Blank or white window

- Exit the viewer completely through **Beenden** and restart it.
- Repair or update Microsoft Edge WebView2 Runtime.
- Remove the local WebView2 profile during uninstallation and reinstall the viewer.

### Display is too large or too small

- Open **Verbindung einrichten** and adjust the zoom.
- Alternatively use `Ctrl` and the mouse wheel.
- Check whether Roon AI Playlist also has a high browser zoom configured.

### Viewer starts but the server does not

This is expected. The viewer does not start a remote computer or application service. The central server must run independently.

## Uninstallation

RoonAIViewer can be removed under **Windows > Installed apps** or through its Start menu entry. During uninstallation, the connection settings and browser profile can optionally be removed as well.

Removing the viewer does not change Roon data or any data on the remote Roon AI Playlist system.
