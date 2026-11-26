# MQB Control Hub 1.6.0 RC1 – Redesign + Firmware GitHub

**Der Windows-Build und beide Signaturen sind vorbereitet. GitHub-Veröffentlichung der EXE-Anhänge steht noch aus.**

## Update für vorhandenen Manager 1.5.4

Dieser Build ist **kompatibel mit der bestehenden tokenfreien Updateprüfung von Manager 1.5.4**. Es ist kein manueller EXE-Austausch nötig, sobald der folgende Release mit seinen Assets online ist.

[New GitHub Release](https://github.com/JanikLAC/MQBManager-Releases/releases/new)

| Einstellung | Wert |
|---|---|
| Tag | `manager-v1.6.0-rc1` |
| Target | `main` |
| Titel | `MQB Control Hub 1.6.0 RC1 – Neuer Launcher + Firmware Center` |
| Typ | **Pre-release** |

Das vorbereitete ZIP `MQBManager_1.6.0_GITHUB_RELEASE_UPLOAD.zip` **vollständig entpacken** und genau zwei Dateien **unverändert und einzeln** hochladen:

- `MQBManager_update.json`
- `MQB_Display_Manager.exe`

## Prüfsummen

| Datei | SHA-256 |
|---|---|
| `MQB_Display_Manager.exe` | `5889c4b6ba76fad1ccf32d76c97bfa7e99d382f398647e776ba3acca8a3d2df9` |
| `MQBManager_update.json` | `be9c37bd2753dad5893521f39f5f2bc9e5e60430985576fdf90ead93c79b0058` |

Manifest: `mqb-public-v1`, Tag `manager-v1.6.0-rc1`, **minimum_manager = 1.5.4**, Ed25519-Signatur mit dem bereits im öffentlichen Manager-Kanal hinterlegten Prüfschlüssel.

## Neuer Launcher

- Neues Win32-Layout mit an die Fensterbreite angepassten Karten, Abständen und Buttonpositionen
- Links sechs neu strukturierte Bereiche mit dezent animierten Hover-Zuständen
- USB-Live-Monitor als **kleine 180x180-Darstellung in einer eigenen Karte**; Übertragungsprotokoll weiterhin MQBVIEW1 (160x160)
- Trennung der GitHub-Repositories für Manager-/Display-Updates
- Firmware-Updateprüfung mit eigener Ed25519-Signatur sowie SHA-256 und innerer Paketprüfung

## Firmware

Der neue Firmwarekanal befindet sich unter [JanikLAC/MQBFirmwareReleases_Controller](https://github.com/JanikLAC/MQBFirmwareReleases_Controller). Das erste Testrelease `firmware-v0.11.0-test` muss dort mit `MQBFirmware_update.json` und `MQB_V0.11.0.mqbupdate` gesondert veröffentlicht werden.

Der Launcher sucht Firmware **ohne Token**, lädt und prüft sie; **er flasht nur nach ausdrücklicher Benutzerbestätigung**. Der Firmwarestand `0.11.0` ist **unverändert**, es wurde keine `0.11.1` erfunden.

## Prüfung und Sicherheit

Windows-x64-Build, PE-Version, reproduzierbarer Neu-Build und beide signierten Manifeste unabhängig geprüft. Die ursprünglichen Firmware-Images und ihre SHA-256-Prüfsummen stimmen überein.

**Offen:** Bedien- und Designprüfung auf echtem Windows, USB-Liveansicht mit angeschlossenem CrowPanel und realer Firmware-Flash-Test. Deshalb RC1/Prerelease und nicht automatisch als stabil freigeben.

Niemals den privaten Signierschlüssel, Token, 1&1-Passwort oder unveröffentlichte Konfiguration als Release-Asset hochladen.

**Powered By Janik Lowis**
