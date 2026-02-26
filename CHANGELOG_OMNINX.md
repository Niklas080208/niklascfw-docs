# Änderungen: OmniNX Setup & Updates (Dokumentation)

Kurze Übersicht, was hinzugekommen bzw. geändert wurde.

---

## Neu: OmniNX-Kategorie (`Switch/omninx/`)

Komplett neue Anleitung für **OmniNX Setup** (Nachfolger NiklasCFW Pack):

| Seite | Inhalt |
|-------|--------|
| **Einführung** | Was ist OmniNX, Varianten (Light/Standard/OC), App-Tabelle (ausklappbar), Ablauf, Voraussetzungen-Link |
| **Voraussetzungen** | Moddable Switch (ungepatcht/gepatcht/Modchip), SD-Karte, Hekate, prod.keys; Callouts für Patch-Status; YouTube-Embed SD-Formatierung |
| **Download** | Pack von Releases, Variante wählen, entpacken (WinRAR/7-Zip/System), auf SD kopieren, Hinweis „Dateien ersetzen“ |
| **Installation – OmniNX** | SD einstecken, Hekate Launch, OmniNX Installer tippen → Anzeige bestätigen (A/Power, Switch-Lite-Hinweis) → Installation abwarten → Abschluss → Uhrzeit in Hekate setzen; Verweise auf emuMMC/Pack einrichten |
| **emuMMC erstellen** | SD-Partition (empfohlen, UltraHand-Ökosystem) zuerst, dann SD-File; Schritte mit Bildern; gemeinsamer Block „Prüfe, ob es geklappt hat“ am Ende; Close-Hinweis bei Partition |
| **Pack einrichten** | Forwarder (Sphaira), **Systemzeit per UltraHand + QuickNTP** (nicht mehr DBI), optionale Apps |
| **Updates** (Unterordner) | Aufgeteilt in **OmniNX Update** und **Firmware Update** |

---

## Neu: Updates unterteilt (`Switch/omninx/updates/`)

- **OmniNX Update** (`omninx-update.md`): UltraHand → OmniNX Downloader → OmniNX Updater (OmniNX runterladen) → Download/Upload-Info → RebootNX → Hekate → Staging: Installer-Schritte inkl. Bilder (wie Installation) + Schritt „Uhrzeit in Hekate setzen“. Bilder unter `images/omninx/updates/pack/`.
- **Firmware Update** (`firmware-update.md`): Zuerst **Firmware herunterladen** (UltraHand → OmniNX Downloader → Updater → Firmware), dann **Daybreak** (mit echten Bildern aus `images/omninx/updates/firmware/`). Kurzversion (Firmware) entfernt.

---

## Geänderte/angepasste Dateien (außerhalb omninx)

- **index.md**: Link zu OmniNX Setup unter „Erweiterte Features“.
- **Switch/index.yaml**, **Switch/niklascfw-pack/index.yaml**: Anpassungen (u. a. Struktur/Navigation).
- **Switch/index.md**, **Switch/niklascfw-pack/index.md**: Gelöscht (Struktur über YAML/andere Seiten).
- **Switch/vorbereitung/index.md**: Anpassungen.
- **retype.yml**: Konfiguration (z. B. OmniNX/Assets).
- **images/allgemein/placeholder.png**: Platzhalter für Bilder.
- **assets/**: niklas-pfp.png, omninx-gross.png, omninx-logo.png.
- **package.json** / **package-lock.json**: Neu (falls Retype/Build).

---

## Bilder (Neu)

- **images/omninx/**  
  - download-install, einführung, einrichtung (UltraHand, QuickNTP, Sphaira), emummc, installation, voraussetzungen  
  - **updates/firmware/**: Daybreak (start, continue, fw-select, preserve, exfat, install finished, etc.)  
  - **updates/pack/**: UltraHand, OmniNX Downloader, RebootNX, Installer-Update, Download/Upload-Phasen  

---

## Links & Technik

- Interne Links auf Updates/Pack einrichten/Installation teils als **absolute Pfade** (`/Switch/omninx/...`), damit Retype sie aus dem `updates/`-Unterordner auflöst.
- Retype: Steps (`>>>`), Callouts (`!!!tip`, `!!!warning`, etc.), Details/Summary für ausklappbare Tabellen, Octicons in YAML ohne `:` (z. B. `icon: package`).

---

*Stand: Session-Ende; alle beschriebenen Änderungen sind mit `git add -A` gestaged.*
