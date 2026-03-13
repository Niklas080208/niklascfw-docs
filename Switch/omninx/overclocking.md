# Overclocking / Undervolting (nur für Fortgeschrittene)

!!!danger Haftungsausschluss
Falsches bzw. zu starkes Übertakten kann zu **irreparablen Schäden** an der Hardware führen. Wir übernehmen hierfür **keine Haftung**. Außerdem wird davon abgeraten, im **Handheldbetrieb** die Konsole über **8,6 W** (V2/OLED) bzw. **6,5 W** (V1/Lite) zu betreiben, da der Akku sonst beschädigt werden kann.
!!!

---

## Grundvoraussetzungen

- **OmniNX OC Pack** installiert
- Folgende Tools mittels **Package Manager** in Ultrahand aktiviert:
  - **Packages**
    - RAM Patcher
    - OC Switchcraft EOS
  - **Overlays**
    - sys-clk
    - Status Monitor
    - FPSLocker (optional)
    - ReverseNX-RT (optional)
  - **Sysmodules**
    - SaltyNX

---

## Tools im Detail

| Tool | Beschreibung |
|------|--------------|
| **RAM Patcher** | Wird hauptsächlich für die Freischaltung der 8‑GB-RAM-Module verwendet, bringt aber auch die benötigte „kip“-Grundlage mit, um ungedeckeltes Übertakten möglich zu machen. (4‑GB-Rampatch inkl. Kip) |
| **OC Switchcraft EOS** | Bietet diverse Einstellungen zur Regulierung der maximalen Taktraten von RAM/CPU/GPU sowie die Definition der Spannungswerte für Undervolting oder extremes OC. |
| **sys-clk** | Mit dem Switch-Sysmodule können die Taktfrequenzen von CPU, GPU und RAM global oder je nach laufender Anwendung und angedocktem Zustand eingestellt werden. |
| **Status Monitor** | Detailliertes Überwachungstool mit mehreren Menüs: aktuelle Taktraten, Stromverbrauch, Auflösung, FPS. |
| **FPSLocker** | Reguliert die Bildwiederholfrequenz (FPS) von Spielen. |
| **ReverseNX-RT** | Alternative zu ReverseNX, schaltet in Echtzeit zwischen Handheld- und Docking-Modus. |
| **SaltyNX** | Sysmodule zum Einfügen von benutzerdefiniertem Code. |

---

## OC-Aktivierung

Die **loader.kip** muss beim Start geladen werden; ohne sie kann die Konsole nicht über Nintendos Standardwerte hinaus betrieben werden.

1. **RAM Patcher** im Ultrahand-Menü öffnen.
2. **„RAM Patch inkl. OC Kip Patch! – 4 GB“** ausführen. (Bei 8‑GB-Umbau den passenden Punkt wählen.)
3. Konsole/CFW **neustarten** – die Kip-Datei wird danach automatisch geladen.

![Ultrahand - RAM Patcher](/images/omninx/overclocking/010_OC-Aktivierung_RamPatcher.jpg)

**Prüfen mit sys-clk:** Unter **Temporary Overrides** die maximalen Werte für CPU/GPU/RAM prüfen und mit der Tabelle vergleichen.

### Referenzwerte (Dock)

| <p> | CPU | GPU | RAM |
|--|-----|-----|-----|
| **Nintendo (Standard)** | 1020 / 1785 MHz Boost | 768 / 921 MHz Boost | 1600 MHz |
| **nVidia (max.)** | bis 2000 MHz | bis 1000 MHz | bis 1866 MHz |
| **CFW OC (safe)** | 1963 MHz | 998 MHz | 1866 MHz |
| **CFW OC (uncapped)** | 2397 MHz | 1267 MHz | 1996 MHz |

### Referenzwerte (Handheld)

| <p> | CPU | GPU | RAM |
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
- **Timings:** Definieren die Reaktionszeit des Arbeitsspeichers
- **Max Clock:** Maximale Taktrate für den Arbeitsspeicher
- **Vddq:** Versorgung der Datenausgangspuffer, Signalintegrität
- **Vdd2:** Spannungsversorgung des Speichercontrollers in der CPU; regelt die Stabilität der CPU-RAM-Kommunikation

**CPU**
- **UV Level:** Vordefinierte Undervolt-Level; je höher der Wert, desto stärker das Undervolting
- **High Freq UV Level:** Undervolt bei maximaler Taktfrequenz; niedrige Werte meist stabiler, **„1“** ist das Minimum für uncapped OC
- **Low Freq VMin / High Freq VMin:** Mindestspannung bei niedrigster bzw. höchster Taktfrequenz
- **Volt Limit:** Maximale Spannungsaufnahme
- **Boost Clock:** Taktfrequenz, die automatisch genutzt wird (z. B. um Ladezeiten zu beschleunigen)
- **Max Clock:** Maximal erlaubte Taktfrequenz

**GPU**
- **UV Level:** Tabellenbasierte Spannungsregulierung
- **Auto Vmin Offset:** Dynamische Offset-Skalierung von Spannung und Taktfrequenz
- **Vmin / Vmax:** Regelung der Minimal- bzw. Maximalspannung
- **Volt Offset:** Undervolting-Offset zur Spannungsreduzierung

Nun können die ersten Werte gesetzt werden (orientiere dich an den Einstellungen im Menü):

![OC Switchcraft EOS – Einstellungen](/images/omninx/overclocking/021_OC-Switchraft-EOS_Ram.jpg)
<a href="/images/omninx/overclocking/022_oc-switchraft-eos_cpu.jpg">
  <img src="/images/omninx/overclocking/022_oc-switchraft-eos_cpu.jpg" width="450">
</a>
<a href="/images/omninx/overclocking/023_oc-switchraft-eos_gpu.jpg">
  <img src="/images/omninx/overclocking/023_oc-switchraft-eos_gpu.jpg" width="450">
</a>
<br><br>


!!!warning Timings
Die **Timings** müssen zum verbauten **RAM-Modul** passen. Dafür im Menü das passende **Preset/Template** der Entwickler laden – alle verfügbaren RAM-Module sind dort vordefiniert.
!!!

Nach dem Setzen aller Werte die Konsole **einmal neustarten**, damit die Einstellungen aktiv werden.

!!!danger Boot-Probleme
Startet die Konsole nicht mehr in die CFW: **loader.kip** unter `sd:/atmosphere/kips` entfernen und durch die originale Kip aus `sd:/switch/.packages/RamPatcher/...` ersetzen.
!!!

---

## sys-clk Overlay

1. Im Ultrahand-Menü unter **Overlays** **sys-clk** auswählen.
2. Unter **Settings** aktivieren: **Uncapped Clocks**, **Boost Mode Override**, **Auto CPU Boost** – für vollen Zugriff auf die Einstellungen und maximale Taktraten.
3. Unter **Temporary Overrides** die Frequenzen anpassen. Zum Einstieg die **Referenzwerte** aus der Tabelle nutzen (z. B. nVidia-Max). Mutige können sich auch gleich an den Maximalwerten **2397 / 1267 / 1996** MHz versuchen und im Worst Case die Konsole neustarten.

![sys-clk – Temporary Overrides](/images/omninx/overclocking/031_SysClk_Main.jpg)
<a href="/images/omninx/overclocking/032_sysclk_config.jpg">
  <img src="/images/omninx/overclocking/032_sysclk_config.jpg" width="450">
</a>
<a href="/images/omninx/overclocking/033_sysclk_temporary.jpg">
  <img src="/images/omninx/overclocking/033_sysclk_temporary.jpg" width="450">
</a>
<br><br>


4. Im **Status Monitor** prüfen, ob Taktraten und **Stromverbrauch (W)** stimmen – im Handheld **max. 8,6 W** (V2/OLED) bzw. **6,5 W** (V1/Lite) für den Akku einhalten.

![Status Monitor – Taktraten und Verbrauch](/images/omninx/overclocking/034_SysClk_StatusMonitor.jpg)

!!!info Hänger
Reagiert die Konsole nicht mehr: **Power-Taste lange** drücken zum Neustart.
!!!

Da es nur wenige Benchmarks (z. B. Ultracam, Furmark-NX) gibt und diese nicht ausreichend genau testen, **10–15 Minuten** mit einem anspruchsvollen Spiel testen. Geeignet sind z. B.:

- Zelda – Tears of the Kingdom
- Batman Arkham Knight
- Tomb Raider: Definitive Edition
- Metro 2033 / Last Light
- The Witcher 3: Wild Hunt
- Hogwarts Legacy

Keine Grafikfehler oder Abstürze nach einigen Minuten → **Einstellung ist stabil.**

---

## Optimierung / Feintuning

Jede CPU, GPU und jeder RAM ist unterschiedlich. Nach erfolgreichem Maximum bei CPU/GPU kann der **Arbeitsspeicher (RAM)** feinjustiert werden.

Viele getestete Konsolen laufen stabil bis **2200 MHz RAM** und teils darüber. Für höhere oder stabilere Taktraten: **Vddq** auf 640 mV, **Vdd2** auf 1175 mV setzen – dabei die **max. Leistungsaufnahme** (siehe Disclaimer) beachten.

**Faustregel:** Je höher der Takt, desto mehr Spannung/Strom wird benötigt.

---

## Maximale Bildqualität

Wenn die nötige Leistung aus der Konsole geholt ist, kannst du mit dem **ReverseNX-RT**-Overlay mehr Grafikqualität und Auflösung aus den Spielen holen (ohne Mods). Stellst du ein Spiel auf **„Fake Docked“** (entspricht dem normalen Dockmodus), bekommst du z. B. mehr Auflösung, Tiefenschärfe und Details in der Ferne auch im Handheldbetrieb angezeigt. Die Auflösung wird dann aber von max. 1080p auf die tatsächliche Auflösung des Switch-Bildschirms runterskaliert. Dieser Prozess bringt dir aber am Ende ein schärferes Bild.

<a href="/images/omninx/overclocking/041_maxquali-standard.jpg">
  <img src="/images/omninx/overclocking/041_maxquali-standard.jpg" width="450">
</a>
<a href="/images/omninx/overclocking/042_maxquali-fakedocked.jpg">
  <img src="/images/omninx/overclocking/042_maxquali-fakedocked.jpg" width="450">
</a>
<br><br>


!!!warning Nicht global
Die Einstellung ist **nicht** wie beim sys-clk-Overlay global – für **jedes Spiel** muss ReverseNX-RT einzeln gesetzt und gespeichert werden.
!!!

!!!danger Reihenfolge
**Zuerst das Spiel starten**, danach das Overlay einstellen. Sonst sind keine Einstellungen möglich.
!!!


---

## Bildwiederholrate / Frames per Second (FPS)

Für viele wichtiger als reine Auflösung ist eine stabile, hohe **Bildwiederholungsrate (FPS)**. Dafür sorgt der **FPSLocker**.

![Ultrahand - FPSLocker](/images/omninx/overclocking/051_FPSLocker_Main.jpg)

!!!warning 30-FPS-Limit vieler Spiele
Viele Spiele (z. B. **Zelda – Breath of the Wild**) unterstützen ab Werk **keine Werte über 30 FPS.** Wer höhere FPS ohne passenden Patch einstellt, erlebt dass Figuren und die Welt **deutlich schneller** laufen – das Spielgefühl stimmt dann nicht.
!!!

Um **über 30 FPS** das richtige Spielgefühl zu bekommen, bietet der FPSLocker unter **„Advanced settings“** die nötigen Tools. Dort findest du in der Regel:

- **Check/download config file**
- **Convert config to patch file**

<a href="/images/omninx/overclocking/052_fpslocker_check-download.jpg">
  <img src="/images/omninx/overclocking/052_fpslocker_check-download.jpg" width="300">
</a>
<a href="/images/omninx/overclocking/053_fpslocker_convert.jpg">
  <img src="/images/omninx/overclocking/053_fpslocker_convert.jpg" width="300">
</a>
<a href="/images/omninx/overclocking/054_fpslocker_convert.jpg">
  <img src="/images/omninx/overclocking/054_fpslocker_convert.jpg" width="300">
</a>
<br><br>


Einfach den **Konverter ausführen**, Spiel **neustarten** und anschließend kannst du die Bildrate schrittweise bis z. B. **60 FPS** erhöhen. Die englischen Beschreibungen im Menü erklären die Schritte im Detail.

Denk aber bitte daran, dass du für höhere Frameraten auch entsprechend mehr Leistung brauchst und die Nintendo Switch gerne an ihre Grenzen gerät. Das bedeutet, während ein "The Legend of Zelda: Tears of the Kingdom" problemlos bei dir mit 60 FPS läuft, kann ein "Batman: Arkham Knight" weiterhin mit 35 FPS vor sich hindümpeln. Manche Spiele sind einfach zu hardwarehungrig und das gilt vor allem für Third-Party-Games.


---

## Problembehebungen / Bugfixes

**Maximale Taktfrequenz zu niedrig**

> Es kann wie immer vorkommen, dass bei der ganze Konfiguration manche Werte vergessen werden, die essentiell sind um maximalen Taktraten **"Uncapped Clocks"** einstellen zu können. Solltest du z. B. deinen GPU-Takt trotz aktiviertem "Uncapped Clocks" im Sys-Clk-Overlay nicht über 998/1075 MHz betreiben können, kann das zwei Ursachen haben:
>
> 1. Dein System hat einen viel zu hohen Gesamtverbrauch und die internen Schutzmechanismen von OC Switchcraft EOS und sys-clk overlay drosseln dies durch Begrenzung des Maximaltakts. Dann musst du mit **Undervolting** der CPU und des RAMs entgegenwirken.
> 2. Oder, und das ist viel wahrscheinlicher, du hast vergessen den Wert **"High Freq UV Level = 1"** zu setzen.
