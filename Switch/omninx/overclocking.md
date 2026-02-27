# Overclocking / Undervolting (nur für Fortgeschrittene)

!!!danger Haftungsausschluss
Falsches bzw. zu starkes Übertakten kann zu **irreparablen Schäden** an der Hardware führen. Wir übernehmen hierfür **keine Haftung**. Außerdem wird davon abgeraten, im **Handheldbetrieb** die Konsole über **8,6 W** (V2/OLED) bzw. **6,5 W** (V1/Lite) zu betreiben, da der Akku sonst beschädigt werden kann.
!!!

---

## Grundvoraussetzungen

- **OmniNX OC Pack** installiert
- Folgende Tools mittels **Package Manager** in Ultrahand aktiviert:

  **Packages**
  - RAM Patcher
  - OC Switchcraft EOS

  **Overlays**
  - sys-clk
  - Status Monitor
  - FPSLocker (optional)
  - ReverseNX-RT (optional)

- **SaltyNX**

---

## Tools im Detail

| Tool | Beschreibung |
|------|--------------|
| **RAM Patcher** | Wird hauptsächlich für die Freischaltung der 8‑GB-RAM-Module verwendet, bringt aber auch die benötigte „kip“-Grundlage mit, um ungedeckeltes Übertakten möglich zu machen. (4‑GB-Rampatch inkl. Kip) |
| **OC Switchcraft EOS** | Bietet Einstellungen zur Regulierung der maximalen Taktraten von RAM/CPU/GPU sowie die Definition der Spannungswerte für Undervolting oder extremes OC. |
| **sys-clk** | Sysmodule zum Einstellen der Taktfrequenzen von CPU, GPU und RAM – global oder je nach Anwendung und angedocktem Zustand. |
| **Status Monitor** | Überwachungstool mit mehreren Menüs: aktuelle Taktraten, Stromverbrauch, Auflösung, FPS. |
| **FPSLocker** | Reguliert die Bildwiederholfrequenz (FPS) von Spielen. |
| **ReverseNX-RT** | Alternative zu ReverseNX, schaltet in Echtzeit zwischen Handheld- und Docking-Modus. |
| **SaltyNX** | Sysmodule zum Einfügen von benutzerdefiniertem Code. |

---

## OC-Aktivierung

Die **loader.kip** muss beim Start geladen werden; ohne sie kann die Konsole nicht über Nintendos Standardwerte hinaus betrieben werden.

1. **RAM Patcher** im Ultrahand-Menü öffnen.
2. **„RAM Patch inkl. OC Kip Patch! – 4 GB“** ausführen. (Bei 8‑GB-Umbau den passenden Punkt wählen.)
3. Konsole/CFW **neustarten** – die Kip-Datei wird danach automatisch geladen.

**Prüfen mit sys-clk:** Unter **Temporary Overrides** die maximalen Werte für CPU/GPU/RAM prüfen und mit der Tabelle vergleichen.

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

In der Regel sollten Werte wie **2397 / 1267 / 1996** MHz oder ähnlich sichtbar sein – mindestens höher als der Nintendo-Standard. Der RAM-Takt entspricht dem in **OC Switchcraft EOS** gesetzten Wert.

---

## OC Switchcraft EOS

Vor dem Übertakten von CPU/GPU/RAM die Grundeinstellung vornehmen. Nur die relevanten Werte anpassen, der Rest sollte **Default** bleiben.

**RAM**
- **Timings:** Reaktionszeit des Arbeitsspeichers
- **Max Clock:** Maximale RAM-Taktrate
- **Vddq:** Versorgung der Datenausgangspuffer, Signalintegrität
- **Vdd2:** Spannungsversorgung des Speichercontrollers; Stabilität CPU–RAM

**CPU**
- **UV Level:** Vordefinierte Undervolt-Level
- **High Freq UV Level:** Undervolt bei maximaler Taktfrequenz („1“ Minimum für uncapped OC)
- **Low/High Freq VMin:** Mindestspannung bei niedriger/hoher Taktfrequenz
- **Volt Limit:** Maximale Spannungsaufnahme
- **Boost Clock / Max Clock:** Taktfrequenzen

**GPU**
- **UV Level:** tabellenbasierte Spannungsregulierung
- **Auto Vmin Offset / Vmin / Vmax / Volt Offset:** Spannung und Undervolting

!!!warning Timings
Die **Timings** müssen zum verbauten **RAM-Modul** passen. Dafür im Menü das passende **Preset/Template** der Entwickler laden.
!!!

Nach dem Setzen aller Werte die Konsole **einmal neustarten**, damit die Einstellungen aktiv werden.

!!!danger Boot-Probleme
Startet die Konsole nicht mehr in die CFW: **loader.kip** unter `sd:/atmosphere/kips` entfernen und durch die originale Kip aus `sd:/switch/.packages/RamPatcher/...` ersetzen.
!!!

---

## sys-clk Overlay

1. Im Ultrahand-Menü unter **Overlays** **sys-clk** auswählen.
2. Unter **Settings** aktivieren: **Uncapped Clocks**, **Boost Mode Override**, **Auto CPU Boost**.
3. Unter **Temporary Overrides** die Frequenzen anpassen. Zum Einstieg die **Referenzwerte** aus der Tabelle (z. B. nVidia-Max oder 2397/1267/1996 MHz) nutzen.
4. Im **Status Monitor** prüfen, ob Taktraten und **Stromverbrauch (W)** stimmen – im Handheld **max. 8,6 W** (V2/OLED) bzw. **6,5 W** (V1/Lite).

!!!info Hänger
Reagiert die Konsole nicht mehr: **Power-Taste lange** drücken zum Neustart.
!!!

Empfohlen: **10–15 Minuten** mit einem anspruchsvollen Spiel testen (z. B. Zelda TotK, Batman Arkham Knight, Tomb Raider, Metro, Witcher 3, Hogwarts Legacy). Keine Grafikfehler oder Abstürze → Einstellung ist stabil.

---

## Optimierung / Feintuning

Jede CPU, GPU und jeder RAM ist unterschiedlich. Nach erfolgreichem Maximum bei CPU/GPU kann der **Arbeitsspeicher (RAM)** feinjustiert werden.

Viele getestete Konsolen laufen stabil bis **2200 MHz RAM** und teils darüber. Für höhere/stabilere Taktraten: **Vddq** auf 640 mV, **Vdd2** auf 1175 mV – dabei die **max. Leistungsaufnahme** (siehe Disclaimer) beachten.

**Faustregel:** Je höher der Takt, desto mehr Spannung/Strom wird benötigt.
