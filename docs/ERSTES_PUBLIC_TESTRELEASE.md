# Erstes öffentliches Testupdate: Manager 1.5.3 → 1.5.4

**Status:** Die erforderlichen Dateien wurden lokal gebaut und signiert, aber das GitHub-Release ist erst dann online, wenn die **beiden Assets** über die GitHub-Weboberfläche hochgeladen und das Release veröffentlicht wurden.

## 1. Release anlegen

[Neues GitHub-Release erstellen](https://github.com/JanikLAC/MQBManager-Releases/releases/new)

| Feld | Wert |
|---|---|
| Repository | `JanikLAC/MQBManager-Releases` (**public**) |
| Tag | `manager-v1.5.4-test` |
| Target | `main` |
| Titel | `MQBManager 1.5.4 – Public-Onlineupdate-Test` |
| Typ | **Set as a pre-release** |

Das heruntergeladene **`MQBManager_1.5.4_GITHUB_RELEASE_UPLOAD.zip`** auf dem PC vollständig entpacken.

Folgende **zwei Dateien unverändert und einzeln** als Release-Assets anhängen:

1. `MQBManager_update.json`
2. `MQB_Display_Manager.exe`

Die restlichen Textdateien (Anleitung, Prüfsummen, Notizen) kannst du optional als Release-Beschreibung verwenden. **Nicht nur das ZIP hochladen.**

Danach auf **Publish release** klicken.

## 2. Erwartete Dateiprüfsummen

| Datei | SHA-256 |
|---|---|
| `MQB_Display_Manager.exe` **1.5.4** | `1ab7db0e5adb1611984662ee4f94ef1126a82452cec9536e4a879800ff814c35` |
| `MQBManager_update.json` | Die im gelieferten ZIP enthaltene signierte Datei nicht verändern; lokale SHA-Datei liegt im Paket. |

Im signierten Katalog stehen folgende Werte:

```text
format = mqb-public-v1
tag = manager-v1.5.4-test
version = 1.5.4
minimum_manager = 1.5.3
asset = MQB_Display_Manager.exe
```

Der Manifest-Schlüssel **öffentlich** ist im Manager eingebettet; der private Signierschlüssel darf **nie** in dieses Repository gelangen.

## 3. Test auf Windows

1. Den alten Manager vollständig schließen.
2. **`MQBManager_1.5.3_Windows_START_OHNE_TOKEN.zip`** in einen neuen Ordner entpacken.
3. Darin `MQB_Display_Manager.exe` ausführen, **nicht direkt aus dem ZIP/WinRAR**.
4. In der Titelleiste **`MQB Control Hub 1.5.3`** kontrollieren.
5. **Manager aktualisieren → Online-Updates suchen**: Der Manager muss `1.5.4` anzeigen.
6. **Update herunterladen**, nach erfolgreicher Prüfung **Update installieren**, Bestätigung geben.
7. Der Manager soll nach Sicherung/Austausch und Neustart **`1.5.4`** anzeigen.

Falls es nicht funktioniert, das Manager-Log mit `GITHUB_STATUS`, `GITHUB_TAG`, `GITHUB_VERSION` und Helper-Fehlern teilen. **Keine Tokens oder Passwörter mitsenden.**

**Wichtig:** Alte 1.5.1/1.5.2-Clients unterstützen diesen öffentlichen Kanal noch nicht; 1.5.3 muss einmalig manuell aus dem ZIP gestartet werden. GitHub-Updates betreffen nur den Windows-Manager, **nicht** die CrowPanel-Firmware.
