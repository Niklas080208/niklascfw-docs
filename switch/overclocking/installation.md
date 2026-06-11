---
icon: download
label: "Installation"
order: 90
---

# Installation

In der Regel ist die CFW nach Installation des **OmniNX OC Pack** bereits overclocking-ready. Wichtig:

- Unter `sd:/atmosphere/kips/` muss die Datei **`hoc.kip`** liegen.
- In der **`hekate.ipl`** muss eine entsprechende Referenzierung vorhanden sein.

>>> Safety Settings prüfen
Öffne **Horizon OC** (nachfolgend: **HOC**) und stelle unter **Safety Settings** sicher, dass **Uncapped Clocks** und **Thermal Throttle** auf <span style="color:rgb(0, 255, 13);"><strong>ON</strong></span> stehen.
![HOC Safety Settings](/images/switch/omninx/overclocking/hoc-safety.gif)

>>> CPU High UV setzen
Unter **CPU Settings** muss **CPU High UV** mindestens auf **1** stehen (Voraussetzung für uncapped OC).
![HOC CPU Settings](/images/switch/omninx/overclocking/hoc-high-uv.gif)

>>> Referenzwerte vergleichen
Unter **Temporary Overrides** die maximalen Werte für CPU/GPU/RAM prüfen und mit den Tabellen unten vergleichen.
![HOC Temporary Overrides](/images/switch/omninx/overclocking/hoc-temp-overrides.gif)

!!!warning Neustart nach HOC-Änderungen
Wurden Einstellungen in **Horizon OC Gaea** geändert, ist ein **Neustart der Konsole** zwingend nötig. Ohne Neustart werden die Werte nicht übernommen.
!!!

### Referenzwerte (Dock)

| | CPU | GPU | RAM |
|--|-----|-----|-----|
| **Nintendo (Standard)** | 1020 / 1785 MHz Boost | 768 / 921 MHz Boost | 1600 MHz |
| **nVidia (max.)** | bis 2000 MHz | bis 1000 MHz | bis 1866 MHz |
| **CFW OC (safe)** | 1963 MHz | 998 MHz | 1866 MHz |
| **CFW OC (uncapped)** | 2397 MHz | 1267 MHz | 1996 MHz |

### Referenzwerte (Handheld)

| | CPU | GPU | RAM |
|--|-----|-----|-----|
| **Nintendo (Standard)** | 1020 MHz | 307 / 460 MHz Boost | 1333 MHz |
| **nVidia (max.)** | bis 2000 MHz | bis 1000 MHz | bis 1866 MHz |
| **CFW OC (safe)** | 1530 MHz | 460 MHz | 1600 MHz |
| **CFW OC (uncapped)** | 2397 MHz | 1267 MHz | 1996 MHz |

In der Regel sollten Werte wie **2397 / 1267 / 1996** MHz oder ähnlich sichtbar sein, mindestens höher als der Nintendo-Standard. Der RAM-Takt entspricht dem in den HOC-Settings unter **Ram Max Clock** gesetzten Wert.
>>>