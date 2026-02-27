# OmniNX Setup

<div style="text-align: center; margin: 2rem 0;">
  <img src="/assets/omninx-gross.png" alt="OmniNX Setup" style="max-width: 200px; margin-bottom: 1rem;">
  <p style="font-size: 1.2em; color: #666;">Einrichtung von OmniNX – von null bis fertige CFW</p>
</div>

---

## Was ist OmniNX?

**OmniNX** ist ein vollständiges Custom-Firmware-Setup für die Nintendo Switch. Es ist in **drei Varianten** verfügbar und legt Wert auf Flexibilität und Modularität. **Light** ist die Basis, **Standard** baut auf Light auf und **OC** baut auf **Standard** auf – jede Variante enthält also alles von der vorherigen plus die zusätzlichen Einträge.

![Hekate Preview](/images/omninx/einfuehrung/hekate-home.png)

### Varianten im Überblick

| Variante | Beschreibung |
|----------|---------------|
| **Light** | Minimal: Kern-Apps, Overlays und Packages für den Alltag. |
| **Standard** | Wie Light, plus weitere Homebrew-Apps, Themes, Mod-Tools und Cheat-Overlay. |
| **OC** | Wie Standard, plus Overclocking: OC Toolkit, sys-clk EOS, SaltySD. |

==- App-Tabelle: Was ist in welcher Variante?
Klicke zum Aufklappen.

| App / Tool / Overlay / Package | Light | Standard | OC |
|--------------------------------|-------|----------|-----|
| **Homebrew-Apps** | | | |
| Sphaira (HB-Menü) | ✓ | ✓ | ✓ |
| DBI | ✓ | ✓ | ✓ |
| Daybreak | ✓ | ✓ | ✓ |
| JKSV | ✓ | ✓ | ✓ |
| Linkalho | ✓ | ✓ | ✓ |
| DNS_mitm Tester | ✓ | ✓ | ✓ |
| Ultrahand Reload | ✓ | ✓ | ✓ |
| NXGallery | — | ✓ | ✓ |
| Switch Theme Installer | — | ✓ | ✓ |
| ThemezerNX | — | ✓ | ✓ |
| SimpleModDownloader | — | ✓ | ✓ |
| SimpleModAlchemist | — | ✓ | ✓ |
| Breeze (Cheat-Manager) | — | ✓ | ✓ |
| CyberFoil | — | ✓ | ✓ |
| Cheats-Updater | — | ✓ | ✓ |
| Sys-Clk Manager | — | — | ✓ |
| **Ultrahand-Packages** | | | |
| OmniNX Downloader | ✓ | ✓ | ✓ |
| RebootNX | ✓ | ✓ | ✓ |
| Alchemist | ✓ | ✓ | ✓ |
| Cool Curves | ✓ | ✓ | ✓ |
| Package Manager | ✓ | ✓ | ✓ |
| OC Toolkit | — | — | ✓ |
| **Overlays** | | | |
| Status Monitor | ✓ | ✓ | ✓ |
| QuickNTP | ✓ | ✓ | ✓ |
| Sysmodules (ovlSysmodules) | ✓ | ✓ | ✓ |
| Ultrahand-Menü (ovlmenu) | ✓ | ✓ | ✓ |
| EdiZon (Cheats) | — | ✓ | ✓ |
| **OC / System (nur OC-Variante)** | | | |
| sys-clk EOS | — | — | ✓ |
| SaltySD | — | — | ✓ |

===

---

## Schnellstart – empfohlener Ablauf

>>> [Voraussetzungen](voraussetzungen)
Modell prüfen, SD (FAT32), Hekate startbar, prod.keys.

>>> [Download](download)
OmniNX-Pack herunterladen, entpacken und auf die SD-Karte kopieren.

>>> [Installation – OmniNX](installation_omninx)
OmniNX Installer Payload starten (Update oder saubere Installation).

>>> [emuMMC erstellen](emummc_erstellen)
SD-File oder SD-Partition in Hekate anlegen.

>>> [Pack einrichten](pack_einrichten)
Forwarder, Systemzeit (NTP), optionale Apps.

>>> [Overclocking (OC)](overclocking) *(optional, nur OC-Pack)*
Übertakten/Undervolting mit RAM Patcher, OC Switchcraft EOS, sys-clk – nur für Fortgeschrittene.

>>> [Updates](./updates/omninx-update)
Pack und Firmware (Daybreak) aktualisieren.
>>>

---

## Alle Schritte im Überblick

| Schritt | Inhalt |
|--------|--------|
| **[Voraussetzungen](voraussetzungen)** | FAT32-SD, prod.keys, was du brauchst |
| **[Download](download)** | Pack herunterladen, entpacken, auf SD kopieren |
| **[Installation – OmniNX](installation_omninx)** | Installer-Payload starten (Update vs. saubere Installation) |
| **[emuMMC erstellen](emummc_erstellen)** | SD-File oder SD-Partition |
| **[Pack einrichten](pack_einrichten)** | Forwarder, Systemzeit, optionale Apps |
| **[Overclocking (OC)](overclocking)** | Übertakten/Undervolting (nur OC-Pack, fortgeschritten) |
| **[Updates](./updates/omninx-update)** | OmniNX-Pack und Firmware aktualisieren |

---

## Wichtige Hinweise

!!!warning Bevor du startest
- Lies alle Anleitungen vollständig durch.
- Erstelle immer ein NAND-Backup vor Modifikationen.
- Nutze nur **FAT32** für die SD-Karte – niemals exFAT.
!!!

!!!info Links
- **OmniNX Releases:** [git.niklascfw.de/OmniNX/OmniNX/releases](https://git.niklascfw.de/OmniNX/OmniNX/releases)
- **NiklasCFW Discord Server:** [discord.gg/niklascfw](https://discord.gg/niklascfw)
!!!
