# Keak — downloads

Installers for the [Keak](https://keak.app) desktop app, and the manifest its built-in updater reads.

There is no source code here on purpose. Keak is built in a private repository; this one exists only so
the downloads and the update check are public. A private repo cannot serve either: an anonymous visitor
gets a 404, which is exactly what the website's download buttons were doing.

## Download

| | |
|---|---|
| macOS (Intel + Apple Silicon) | [Keak-macOS.dmg](../../releases/latest/download/Keak-macOS.dmg) |
| Windows | [Keak-Windows-setup.exe](../../releases/latest/download/Keak-Windows-setup.exe) |
| Linux | [Keak-Linux.AppImage](../../releases/latest/download/Keak-Linux.AppImage) |

Those three filenames never change. `releases/latest/download/<name>` only resolves when the name is
constant, so every release publishes stable-named copies next to the versioned installers — otherwise
every link on the website breaks the moment a new version ships.

macOS is signed with a Developer ID and notarized by Apple, so it opens with no warning. Windows is
unsigned, so SmartScreen shows a panel on first run: "More info", then "Run anyway".

## Updates

The app checks `latest.json` in the newest release and updates itself. Each entry is signed, and the app
verifies that signature before installing anything.
