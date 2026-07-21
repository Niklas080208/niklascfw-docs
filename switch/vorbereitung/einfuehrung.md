---
icon: book
label: "OmniNX Einführung"
order: 80
author:
  name: NiklasCFW
  avatar: /assets/niklas-pfp.png
---

# OmniNX Setup

<div style="text-align: center; margin: 2rem 0;">
  <img src="/assets/omninx-gross.png" alt="OmniNX Setup" style="max-width: 200px; margin-bottom: 1rem;">
  <p style="font-size: 1.2em; color: #666;">Einrichtung von OmniNX – von null bis fertige CFW</p>
</div>

---

## Was ist OmniNX?

**OmniNX** ist ein vollständiges Custom-Firmware-Setup für die Nintendo Switch. Es ist in **drei Varianten** verfügbar und legt Wert auf Flexibilität und Modularität. **Light** ist die Basis, **Standard** baut auf Light auf und **OC** baut auf **Standard** auf – jede Variante enthält also alles von der vorherigen plus die zusätzlichen Einträge.

![Hekate Preview](/images/switch/omninx/einfuehrung/hekate-home.png)

### Features von OmniNX

- **Drei Varianten** – Light (minimal), Standard (voll) und OC (alles aus Light/Standard plus Overclocking-Tools)
- **Vollständiges CFW-Setup** – Sofort einsatzbereit mit Atmosphere, Hekate und wichtigen Tools
- **Ultrahand** – Overlay-Menü und Package-System (OmniNX Downloader, Alchemist, Package Manager und weitere)
- **Vorinstallierte Payloads** – u. a. APL (Recovery), Lockpick RCM und Pro, TegraExplorer, [modchip_toolbox](https://github.com/DefenderOfHyrule/modchip-toolbox), OmniNX Installer
- **Sicherheit und Patches** – sys-patch, DNS-MitM
- **sys-ticon (Standard und OC)** – Home-Menü: eigene Icons, Titel, Herausgeber und Versionsanzeige ([sys-ticon](https://github.com/masagrator/sys-ticon))

### Varianten im Überblick

| Variante | Beschreibung |
|----------|---------------|
| **Light** | Minimal: Kern-Apps, Overlays und Packages für den Alltag. |
| **Standard** | Wie Light, plus weitere Homebrew-Apps, Themes, Mod-Tools und Cheat-Overlay. |
| **OC** | Wie Standard, plus Overclocking: [Horizon OC](https://github.com/Horizon-OC/Horizon-OC), SaltyNX/SaltySD, FPSLocker. |

==- Inhalt: Was ist in welcher Variante?
Klicke zum Aufklappen.

**Legende:** ✓ = enthalten · — = nicht enthalten

#### Homebrew-Apps

| App | Light | Standard | OC |
| --- | ----- | -------- | -- |
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
| Furmark-NX | — | — | ✓ |
| Benchmark-Toolbox | — | — | ✓ |
| swr-ini-tool | — | — | ✓ |

#### Ultrahand-Packages

*(offload)* = liegt in `switch/.packages/.offload/`, standardmäßig deaktiviert; Aktivierung nur über das UltraHand-**Package Manager**-Package.

| Package | Light | Standard | OC |
| ------- | ----- | -------- | -- |
| OmniNX Downloader | ✓ | ✓ | ✓ |
| RebootNX | ✓ | ✓ | ✓ |
| Alchemist | ✓ | ✓ | ✓ |
| Cool Curves | ✓ | ✓ | ✓ |
| Package Manager | ✓ | ✓ | ✓ |
| Memory Kit / Memory Config / Memory Switcher *(offload)* | ✓ | ✓ | ✓ |
| Installer Configurator *(offload)* | ✓ | ✓ | ✓ |
| HOC Toolkit *(offload)* | — | — | ✓ |

#### Overlays

*(offload)* = liegt in `switch/.overlays/.offload/`, ebenfalls per **Package Manager** ein- und ausschaltbar.

| Overlay | Light | Standard | OC |
| ------- | ----- | -------- | -- |
| Horizon-OC-Monitor | ✓ | ✓ | ✓ |
| QuickNTP | ✓ | ✓ | ✓ |
| Sysmodules (ovlSysmodules) | ✓ | ✓ | ✓ |
| Ultrahand-Menü (ovlmenu) | ✓ | ✓ | ✓ |
| sys-patch Overlay *(offload)* | ✓ | ✓ | ✓ |
| DNS-MitM Manager *(offload)* | ✓ | ✓ | ✓ |
| MasterVolume *(offload)* | ✓ | ✓ | ✓ |
| EdiZon (Cheats) | — | ✓ | ✓ |
| sys-ticon | — | ✓ | ✓ |
| Horizon OC Overlay | — | — | ✓ |
| FPSLocker | — | — | ✓ |
| ReverseNX-RT | — | — | ✓ |

#### OC / System (nur OC-Variante)

| Komponente | Light | Standard | OC |
| -------- | ----- | -------- | -- |
| [Horizon OC](https://github.com/Horizon-OC/Horizon-OC) (KIP, hoc-clk) | — | — | ✓ |
| SaltyNX | — | — | ✓ |
| SaltySD | — | — | ✓ |
| Gepatchtes `exosphere.bin` | — | — | ✓ |
| FPSLocker-Patch-Entpackung (`boot_package.ini`) | — | — | ✓ |

!!!info sys-clk / Sys-Clk Manager
**sys-clk** und **Sys-Clk Manager** sind nicht fest im Pack enthalten. Optional über **OmniNX Downloader** nachinstallierbar.
!!!

===

### Basis in allen Varianten

In jeder Variante enthalten, aber nicht in der Tabelle oben aufgeführt:

- **[Atmosphere](https://github.com/Atmosphere-NX/Atmosphere)**, **[Hekate](https://github.com/CTCaer/hekate)** / Nyx, **[sys-patch](https://github.com/borntohonk/sys-patch)**, **[Ultrahand](https://github.com/ppkantorski/Ultrahand-Overlay)**
- Payloads: **[APL](https://git.niklascfw.de/OmniNX/AllgemeinerProblemLoeser)**, Lockpick RCM, **[Lockpick RCM Pro](https://github.com/sthetix/Lockpick_RCM_Pro)**, TegraExplorer, **[modchip_toolbox](https://github.com/DefenderOfHyrule/modchip-toolbox)**, **[OmniNX Installer](https://git.niklascfw.de/OmniNX/OmniNX-Installer-Payload)**
- DNS-MitM (Hosts), USB 3.0 Force, OmniNX Sphaira-Theme, Boot-Logos, HorizonOS-Logo-Patch, **[MasterVolume](https://github.com/averne/MasterVolume)**-IPS-Patch, `exosphere.ini` (optional)

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
