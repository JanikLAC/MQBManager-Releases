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
| `MQB_Display_Manager.exe` | `78e02ecd9de96d76584b8ffba1fd5ef9bf3c6c73232bd48e6457b56b7bb4d41b` |
| `MQBManager_update.json` | `97d3140108b74d046257495bb3621a9a9347eec691742d63ae0c9c812281c6bd` |

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
