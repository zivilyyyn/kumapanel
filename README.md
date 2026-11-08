# KumaPanel

Unofficial Windows tray client for [Uptime Kuma](https://github.com/louislam/uptime-kuma). Click the tray icon to open a WebView2 panel with your Kuma dashboard — no browser window, no separate app per monitor.

## Features

- System tray icon; left-click to toggle the panel, right-click for menu (open, reload, autostart, exit)
- WebView2 panel with persistent login session
- Status overview hidden on the dashboard root; the monitor list fills the width
- Click a monitor or group to open its detail; click it again (or the close button) to return to the list
- Window height is 80% of the work area; page zoom 80%
- Starts with Windows on first run (user-level Run key, toggleable from the tray menu)
- Groups are collapsed on launch

## Configuration

Settings live outside the repository, in `%APPDATA%\KumaPanel\settings.json`:

```json
{"url": "http://your-kuma-host:3001", "lang": "zh"}
```

`url` is the base URL of your Uptime Kuma instance. `lang` is `zh` or `en` (tray menu language).

## Build

Requirements: .NET 10 SDK, Windows 10/11, WebView2 Runtime (ships with Windows 11).

```
dotnet publish src/KumaPanel.csproj -c Release -o app
```

## License

MIT. Not affiliated with the Uptime Kuma project.
