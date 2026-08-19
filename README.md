# DATIpilot: moto Terminal-App

Dieses Repository ist ein eingefrorener Snapshot der moto Terminal-Anwendung mit Stand vom **28.02.2026**. Die Software wurde im Rahmen des Förderprojekts DATIpilot entwickelt und wird hier zum Projektabschluss als Open Source unter der GNU Affero General Public License v3.0 (AGPL-3.0) veröffentlicht.

Die Terminal-App läuft auf NFC-Kiosk-Geräten (Raspberry Pi mit Touchdisplay) im Offenen Ganztag. Kinder melden sich per RFID-Chip an und ab; das Gerät kommuniziert mit dem Backend der [moto OGS-App](https://github.com/moto-nrw/dati-pilot-moto-ogs-app) über deren IoT-Schnittstelle.

## Komponenten

| Komponente | Technologie |
|---|---|
| App | React, TypeScript, Vite |
| Desktop-Shell | Tauri (Rust) |
| NFC | PN5180-Lesegerät am Raspberry Pi |

## Lokaler Start

Voraussetzungen: Node.js mit npm sowie eine laufende Instanz der moto OGS-App als Backend.

```bash
npm install
cp .env.example .env          # API-URL und Geräteschlüssel eintragen
npm run dev
```

Für den Desktop-Build wird zusätzlich die Rust-Toolchain benötigt (`npm run tauri build`).

## Status

Dieses Repository ist ein Archiv-Stand zum Projektende und wird nicht weitergepflegt. Es werden keine Issues, Pull Requests oder Sicherheits-Patches bearbeitet. Die aktive Weiterentwicklung von moto läuft getrennt von diesem Archiv unter [moto.nrw](https://moto.nrw).

## Lizenz

GNU Affero General Public License v3.0, siehe [LICENSE](LICENSE).
