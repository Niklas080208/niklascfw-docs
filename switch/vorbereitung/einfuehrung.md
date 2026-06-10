# OmniNX Setup

<div style="text-align: center; margin: 2rem 0;">
  <img src="/assets/omninx-gross.png" alt="OmniNX Setup" style="max-width: 200px; margin-bottom: 1rem;">
  <p style="font-size: 1.2em; color: #666;">Einrichtung von OmniNX – von null bis fertige CFW</p>
</div>

---

## Was ist OmniNX?

**OmniNX** ist ein vollständiges Custom-Firmware-Setup für die Nintendo Switch. Es ist in **drei Varianten** verfügbar und legt Wert auf Flexibilität und Modularität. **Light** ist die Basis, **Standard** baut auf Light auf und **OC** baut auf **Standard** auf – jede Variante enthält also alles von der vorherigen plus die zusätzlichen Einträge.

![Hekate Preview](/images/switch/omninx/einfuehrung/hekate-home.png)

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
