# MQBManager – öffentliche Releases

Offizieller Download- und Updatekanal für **MQB Display Manager** (Windows x64).

**Powered By Janik Lowis**

Dieses Repository ist **öffentlich** und enthält ausschließlich für die Veröffentlichung bestimmte Updateinformationen und Release-Downloads. Der Entwicklungs- und Quellcodebereich unter `JanikLAC/MQBManager` bleibt **privat**.

## Online-Updates ohne GitHub-Token

Ab **Manager 1.5.3** ist dieser Kanal fest eingebaut:

- Repository: `JanikLAC/MQBManager-Releases`
- Release-Abfrage: öffentliche GitHub-Releases-API
- Kein GitHub-PAT / Token erforderlich
- Installation nur nach ausdrücklicher Bestätigung des Benutzers
- Manifest-Signatur (Ed25519), SHA-256, Dateigröße und Windows-Dateiversion werden geprüft

> **Teststand:** Der erste geplante Online-Test ist `1.5.3 → 1.5.4`. Das GitHub-Prerelease muss noch mit zwei Dateien veröffentlicht werden, bevor es der Manager findet. Der tatsächliche automatische EXE-Austausch muss auf Windows getestet werden.

## Das erste Test-Release

Tag: **`manager-v1.5.4-test`**  
Titel: **`MQBManager 1.5.4 – Public-Onlineupdate-Test`**  
Release-Typ: **Prerelease**

Es muss genau diese zwei Assets enthalten:

- `MQBManager_update.json` – signierter Updatekatalog
- `MQB_Display_Manager.exe` – Windows-x64-EXE

**Nicht das Upload-ZIP als einzelnes Release-Asset anhängen.** ZIP vollständig entpacken und die zwei Dateien **unverändert** einzeln hochladen.

[Anleitung mit Prüfsummen](docs/ERSTES_PUBLIC_TESTRELEASE.md) · [Releases ansehen](https://github.com/JanikLAC/MQBManager-Releases/releases)

## Sicherheitsregeln

- Keine privaten Signierschlüssel, GitHub-Tokens oder 1&1-Zugangsdaten in Commits oder Release-Assets speichern.
- Die digitale Herkunft eines Updates wird mittels **fest eingebettetem öffentlichem Ed25519-Schlüssel** und signiertem Manifest geprüft, nicht nur durch GitHub/HTTPS.
- GitHub-Release-Dateien sind **öffentlich herunterladbar**.
- Test-Releases sind **keine stabilen Produktionsfreigaben**, solange Windows-Start, Update-Rollback und Display-Hardware nicht praktisch getestet wurden.

## Frühere Versionen

Alte Releases können später mit ihren tatsächlichen Versionsnummern und Testständen zusätzlich archiviert werden. Historische EXEs werden dabei nicht künstlich umversioniert.
