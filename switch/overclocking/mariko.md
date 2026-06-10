# Overclocking / Undervolting (V2,Lite,OLED)

!!!danger Haftungsausschluss
Falsches bzw. zu starkes Übertakten kann zu **irreparablen Schäden** an der Hardware führen. Wir übernehmen hierfür **keine Haftung**. Außerdem wird davon abgeraten, im **Handheldbetrieb** die Konsole über **8,6 W** (V2/OLED) bzw. **6,5 W** (Lite) zu betreiben, da der Akku sonst beschädigt werden kann.
!!!

---

## Grundvoraussetzungen

- **OmniNX OC Pack** installiert
- Folgende Tools mittels **Package Manager** in Ultrahand aktiviert:
  - **Overlays**
    - Horizon OC Monitor
    - Horizon OC
    - FPSLocker (optional)
    - ReverseNX-RT (optional)
  - **Sysmodules**
    - SaltyNX

!!!info Empfehlung
Stelle Ultrahand auf **Englisch** um: Die Menüs sind übersichtlicher und die Fehlersuche leichter. Dokumentiere jeden Schritt mit **Notizen**, damit du Änderungen später nachvollziehen kannst.
!!!

---

## Die Tools

| Tool | Beschreibung |
|------|--------------|
| **Horizon OC** | Übertaktungsprogramm; erweitertes CPU-, GPU- und RAM-Tuning mit benutzerfreundlichen Konfigurationstools. |
| **Horizon OC Monitor** | Detailliertes Überwachungstool: aktuelle Taktraten, Stromverbrauch, Auflösung, FPS. |
| **FPSLocker** | Reguliert die Bildwiederholfrequenz (FPS) von Spielen. |
| **ReverseNX-RT** | Alternative zu ReverseNX; schaltet in Echtzeit zwischen Handheld- und Docking-Modus. |
| **SaltyNX** | Sysmodule zum Einfügen von benutzerdefiniertem Code. |

---

## Installation & Vorbereitung

In der Regel ist die CFW nach Installation des **OmniNX OC Pack** bereits overclocking-ready. Wichtig:

- Unter `sd:/atmosphere/kips/` muss die Datei **`hoc.kip`** liegen.
- In der **`hekate.ipl`** muss eine entsprechende Referenzierung vorhanden sein.

>>> Safety Settings prüfen
Öffne **Horizon OC** (nachfolgend: **HOC**) und stelle unter **Safety Settings** sicher, dass **Uncapped Clocks** und **Thermal Throttle** auf **ON** stehen.
![Platzhalter: HOC Safety Settings](/images/switch/allgemein/placeholder.png)

>>> CPU High UV setzen
Unter **CPU Settings** muss **CPU High UV** mindestens auf **1** stehen (Voraussetzung für uncapped OC).
![Platzhalter: HOC CPU Settings](/images/switch/allgemein/placeholder.png)

>>> Referenzwerte vergleichen
Unter **Temporary Overrides** die maximalen Werte für CPU/GPU/RAM prüfen und mit den Tabellen unten vergleichen.
![Platzhalter: HOC Temporary Overwrites](/images/switch/allgemein/placeholder.png)

!!!warning Neustart nach HOC-Änderungen
Wurden Einstellungen in **Horizon OC** geändert, ist ein **Neustart der Konsole** zwingend nötig. Ohne Neustart werden die Werte nicht übernommen.
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

---

## Horizon OC – Begrifflichkeiten

| Menüpunkt | Bedeutung |
|-----------|-----------|
| **Edit App Profile** | Homebrew-/Spiel-spezifische Übertaktungswerte |
| **Edit Global Profile** | Globale Werte für alles (werden durch **App Profile** überschrieben, falls gesetzt) |
| **Temporary Overrides** | Temporäre Werte; werden durch Neustart zurückgesetzt |
| **Settings** | Voreinstellungen (Taktfrequenz, Timing, Spannung usw.) |
| **About** | Entwicklerinfos und Danksagungen |

### Safety Settings

| Einstellung | Beschreibung |
|-------------|--------------|
| **Uncapped Clocks** | Entfernt die Taktbegrenzung. Vorsicht, besonders im Handheld. (Standard: **ON**) |
| **Thermal Throttle** | Senkt Taktraten ab einer Temperaturschwelle. (Standard: **ON**) |
| **Handheld TDP** | Senkt Taktraten, wenn der Akku zu viel Leistung zieht. (Standard: **ON**; 9600 mW bei V2/OLED, 6400 mW bei Lite) |
| **TDP Threshold** | Schwellenwert für Handheld TDP |
| **Thermal Thrott Limit** | Temperaturschwelle für Thermal Throttle |

### RAM Settings

| Einstellung | Beschreibung |
|-------------|--------------|
| **SOC DVB Shift** | Erhöht die SoC-Spannung zur RAM-Stabilisierung, besonders ab 2400 MHz+. |
| **HP Mode** | Verbessert Latenz durch Deaktivierung des Energiesparmodus. (Standard: **OFF**) |
| **RAM VDD2 Voltage** | Spannung des Speichercontrollers; Stabilität der CPU-RAM-Kommunikation |
| **RAM VDDQ Voltage** | Versorgung der Datenausgangspuffer, Signalintegrität |
| **Step Mode** | Schrittweite der Frequenzliste (z. B. 66 MHz: 1600 → 1666 → 1733) |
| **Ram Max Clock** | Maximale RAM-Taktrate |
| **RAM Latency Editor** | Konfiguration der Lese- und Schreiblatenz (tRWL) |
| **RAM Timings Reductions** | Reaktionszeit des Arbeitsspeichers |

### CPU Settings

| Einstellung | Beschreibung |
|-------------|--------------|
| **CPU Low UV** | Vordefinierte Undervolt-Level; höherer Wert = stärkeres Undervolting |
| **CPU High UV** | Undervolt bei Maximal-Takt; niedrige Werte stabiler, **1** = Minimum für uncapped OC |
| **CPU UV Tbreak** | Frequenz, an der niedrige und hohe UV-Modi wechseln |
| **CPU Low VMIN** | Mindestspannung bei niedrigster Taktfrequenz |
| **CPU High VMIN** | Mindestspannung bei höchster Taktfrequenz |
| **CPU Max Voltage** | Maximale Spannungsaufnahme |
| **CPU Max Clock** | Maximal erlaubte Taktfrequenz |
| **CPU Boost Clock** | Kurzzeit-Boost (z. B. für Ladezeiten) |
| **Overwrite Boost Mode** | Eigene Boost-Frequenz aktivieren |

### GPU Settings

| Einstellung | Beschreibung |
|-------------|--------------|
| **GPU Undervolt Table** | Gewählte UV-Tabelle (empfohlen: **High UV Table**) |
| **GPU VMIN** | Minimale Spannungsaufnahme |
| **GPU Max Voltage** | Maximale Spannungsaufnahme |
| **GPU Voltage Offset** | Spannungsversatz für VMIN und Max Voltage |
| **GPU Scheduling Override** | Auslastungsregelung der GPU (empfohlen: **OFF**) |
| **GPU DVFS Mode** | Passt VMIN an den RAM-Takt an (empfohlen: **PCV Hijack**) |
| **GPU DVFS Offset** | Spannungsversatz für VMIN im DVFS-Modus |
| **GPU Voltage Table** | Detailmenü der UV-Tabelle: GPU-Taktfrequenzen und Spannungsparameter |

---

## Arbeitsspeicher (RAM)

Nintendo verbaut unterschiedliche Speichermodule (Samsung, Toshiba, Hynix usw.). Vor dem RAM-OC musst du wissen, **welches Modul** in deiner Konsole steckt, da jedes Modul anders übertaktbar ist.

Die Info findest du in **Hekate** oder unter **Ultrahand → Systeminfo** (z. B. Vendor: Samsung, Modell: K4UBE3D4AA-MGCL).

In der OC-Szene werden RAM-Module per **Tier Level** eingestuft: Je höher der Tier, desto übertaktfreudiger das Modul.

| Tier Level | RAM ID |
|------------|--------|
| **GOD-tier** | WT:B, NEI/NEE |
| **S-tier** | AA-MGCL/AA-MGCR |
| **A-tier** | AM-MGCJ, WT:E |
| **B-tier** | WT:F |
| **C-tier** | AB-MGCL |
| **D-tier** | NME |

!!!warning RAM-Info nach Umbau
Es wird immer die ID des **ab Werk verbauten** RAMs angezeigt. Nach einem **8-GB-Upgrade** oder RAM-Tausch bei einer Reparatur ist die Anzeige oft **falsch**. Dann die Person fragen, die den RAM verbaut hat.
!!!

![Platzhalter: Hekate Console Info](/images/switch/allgemein/placeholder.png)

### Richtwerte vom HOC-Entwickler

| Tier | RAM ID | Ram Clock | VDD2 | VDDQ | Common Timings (T1–T8) | Super Tight (ST) Timings (T1–T8) |
|------|--------|-----------|------|------|------------------------|----------------------------------|
| GOD | WT:B | 3066–3200 | 1175 mV | 600 mV | (4-4-5) 4-2-6-5-6 | (6-6-7) 5-2-6-5-6 |
| GOD | NEI/NEE/x267 | 3100–3300 | 1175 mV | 640 mV | (3-3-2) 1-5-5-4-6 | (4-4-4) 2-7-6-5-6 |
| S | AA-MGCL/MGCR | 2766–3100 | 1175 mV | 640 mV | (4-4-5) 4-5-5-6-6 | (4-4-8) 5-5-6-7-6 |
| A | WT:E | 2500–3033 | 1175 mV | 600 mV | (2-2-2) 1-4-4-4-6 | (3-5-3) 2-5-4-S-6 |
| B | AM-MGCJ | 2633–2933 | 1175 mV | 640 mV | (3-2-4) 1-4-4-4-6 | (4-3-8) 1-5-4-4-6 |
| C | WT:F | 2633–2800 | 1175 mV | 600 mV | (4-4-2) 4-4-6-3-6 | (5-5-4) 4-5-6-5-6 |
| D | AB-MGCL | 2500–2766 | 1175 mV | 640 mV | (4-4-4) 3-4-5-6-6 | (4-4-8) 4-5-6-8-6 |
| E | NME | 2300–2566 | 1175 mV | 640 mV | (2-2-3) 0-1-2-2-6 | (5-3-4) 1-8-3-3-6 |

!!!info Reihenfolge beim RAM-Tuning
Ermittle zuerst die **maximale RAM-Frequenz**, bevor du Timings anpasst. **t7** und **t6** sind stark frequenzabhängig und müssen bei hohen Takten oft gelockert werden.

**2533 MHz** sind bekannt dafür, durch Timing-Änderungen Probleme zu verursachen. Teste vorsichtig. **JEDEC-Frequenzen** (RAM Settings → **Step Mode**) können je nach Chip mehr Leistung, engere Timings oder bessere Stabilität bringen, variieren aber stark.
!!!
>>>

## Moderates RAM-Overclocking

>>> Erster Versuch: 2200 MHz
Setze **Ram Max Clock** auf **2200 MHz**. Dieser Wert funktioniert erfahrungsgemäß auf den meisten Konsolen. **Common Timings** sowie **VDD2** und **VDDQ** aus der Tabelle übernehmen.
![Platzhalter: HOC RAM Clock](/images/switch/allgemein/placeholder.png)

>>> Höherer Start mit DVB-Shift
Startest du über 2200 MHz, beginne mit **DVB-Shift 10** und reduziere auf **2–6**, sobald die maximale RAM-Geschwindigkeit steht. Höherer DVB-Shift erhöht den Stromverbrauch kaum, aber leicht die Wärmeentwicklung.
![Platzhalter: HOC Temporary Overwrites](/images/switch/allgemein/placeholder.png)

>>> Neustart & Temporary Overrides
Nach dem Setzen der Werte: **Konsole neustarten**. Danach in **Temporary Overrides** den gewünschten RAM-Takt aktivieren.

!!!warning Absturz oder Freeze
Friert die Konsole ein oder beendet mit Fehler: **Ram Max Clock** zu hoch oder **Timings** zu straff – Werte anpassen und erneut testen. Bei eingefrorener Konsole **Power** gedrückt halten, bis sie ausgeht, dann wieder einschalten. Ein kurzes **Knacken** aus den Lautsprechern ist normal.
!!!

!!!info Stabilität testen
Passe Werte schrittweise an, bis **Startbildschirm und Spiele** stabil laufen. Wenige Benchmarks (z. B. Ultracam, Furmark-NX) reichen nicht – teste mit anspruchsvollen Spielen, z. B.:

- Zelda – Tears of the Kingdom
- Batman Arkham Knight
- Tomb Raider: Definitive Edition
- Metro 2033 / Last Light
- The Witcher 3: Wild Hunt
- Hogwarts Legacy
!!!

>>> Feintuning nach stabilem Takt
1. **DVB-Shift** von 10 schrittweise auf **2–6** reduzieren (je niedriger, desto besser).
2. Passende **Super Tight (ST)** Timings testen.
3. Schlägt ST fehl: DVB-Shift wieder erhöhen und/oder Timings lockern in dieser Reihenfolge: **t8 → t1 → t2 → t3 → t6 → t7 → t4 → t5**

!!!tip Prioritäten beim RAM
- Bei Problemen zuerst **t7** und **t6** lockern (stark frequenzabhängig).
- RAM trägt am meisten zur Gesamtleistung bei: **maximale Frequenz zuerst**.
- Selten scheitern Module selbst bei Common Timings; dann auch diese lockern.
- **Höherer Clock ist oft relevanter als extrem niedrige Timings**, wenn z. B. 2800 MHz nur mit Common Timings stabil laufen.
!!!

### HP Mode

**HP Mode** verbessert die Latenz und damit **1 %-Low-Werte** sowie weniger Ruckler. Manche RAM-Module vertragen ihn nicht.

1. Maximalen Takt und Timings bei **deaktiviertem** HP Mode finden.
2. Anschließend **HP Mode aktivieren** und erneut testen.
3. Stabil → aktiv lassen, sonst deaktiviert lassen.

---

## CPU & GPU

CPU-Takt spielt unter Atmosphere bei den meisten Apps und Spielen eine **untergeordnete** Rolle; Fokus liegt auf **RAM-Durchsatz** und **GPU**. Extremes OC lohnt selten, **Stabilität** hat Priorität.

**Undervolting (UV)** ist nötig für Stabilität und begrenzten Strombedarf. Im Handheld weiterhin **max. 8,6 W** (V2/OLED) bzw. **6,5 W** (Lite) einhalten. Gelegentliche Spitzen sind unkritisch, dauerhaft höhere Werte vermeiden.

Ein **Speedo**-Wert (Ultrahand → **+** → **System**) über **1600** bei Mariko-Chips (V2, Lite, OLED) ist ein gutes Zeichen für erfolgreiches OC.

### CPU – empfohlene Startwerte

| Einstellung | Wert |
|-------------|------|
| CPU Low VMIN | 590 mV |
| CPU High VMIN | 720 mV |
| CPU Max Voltage | 1120 mV (Standard) |
| CPU Max Clock | 2193 MHz |
| CPU Boost Clock | 2397 MHz |

![Platzhalter: HOC CPU Settings – Startwerte](/images/switch/allgemein/placeholder.png)

**Overwrite Boost Mode** auf **On**, sonst greift der Boost-Wert nicht.

Nach stabilem Neustart **CPU Low UV** und **CPU High UV** setzen: mit **4** beginnen und so hoch wie möglich steigern. Manche Konsolen starten schon bei **CPU Low UV = 1** nicht mehr; **CPU High VMIN** ist oft wichtiger.

**CPU UV Tbreak** meist auf Standard **1683 MHz Tbreak** lassen. Hilft **CPU High UV = 1** nicht, **1581 MHz Tbreak** testen.

### GPU – empfohlene Startwerte

Bei der GPU auf **Artefakte** neben Abstürzen achten; sie treten oft erst nach einigen Minuten im Spiel auf.

Frequenzen **über 1305 MHz** GPU-Takt nur mit **extremer Vorsicht**; hier droht am ehesten Hardwareschaden. Relevant ist vor allem die **GPU Voltage Table** (Frequenzen ab 1267 MHz aktivieren).

| Einstellung | Wert |
|-------------|------|
| GPU VMIN | 550 mV |
| GPU Max Voltage | 800 mV |
| GPU Voltage Offset | -10 |
| GPU Scheduling Override | Do not override |
| GPU DVFS Mode | PCV Hijack |
| GPU DVFS Offset | -10 mV |
| GPU Voltage Table | 76,8 MHz bis 1267,2 MHz → **AUTO** |

![Platzhalter: HOC GPU Settings – Startwerte](/images/switch/allgemein/placeholder.png)

---

## Monitoring

**Horizon OC Monitor** (erweiterte Version von Status Monitor) zeigt Frequenzen, Stromverbrauch, Auflösung, FPS und Temperaturen.

Bei den Layouts **Mini** und **Micro** sind nicht alle Elemente voraktiviert. Einstellungen erreichst du mit **Y**:

- **Elements**: Was angezeigt wird
- **Toggles**: Detailwerte pro Element

!!!info Echte Temperaturen
Aktiviere den Toggle **Real Temperatures**, damit CPU, GPU und RAM echte Werte zeigen. **TMP** ist nur ein berechneter Wert und meist niedriger, daher eher deaktivieren.
!!!

---

## Maximale Bildqualität

Wenn die nötige Leistung aus der Konsole geholt ist, kannst du mit dem **ReverseNX-RT**-Overlay mehr Grafikqualität und Auflösung aus den Spielen holen (ohne Mods). Stellst du ein Spiel auf **„Fake Docked“** (entspricht dem normalen Dockmodus), bekommst du z. B. mehr Auflösung, Tiefenschärfe und Details in der Ferne auch im Handheldbetrieb angezeigt. Die Auflösung wird dann von max. 1080p auf die tatsächliche Auflösung des Switch-Bildschirms runterskaliert. Dieser Prozess bringt dir aber am Ende ein schärferes Bild.

:::content-center
||| Standard
<a href="/images/switch/omninx/overclocking/041_maxquali-standard.jpg" target="_blank" rel="noopener">![Max. Bildqualität – Standard](/images/switch/omninx/overclocking/041_maxquali-standard.jpg)</a>
||| Fake Docked
<a href="/images/switch/omninx/overclocking/042_maxquali-fakedocked.jpg" target="_blank" rel="noopener">![Max. Bildqualität – Fake Docked](/images/switch/omninx/overclocking/042_maxquali-fakedocked.jpg)</a>
|||
:::

!!!warning Nicht global
Die Einstellung ist **nicht** global wie bei HOC-Profilen: Für **jedes Spiel** muss ReverseNX-RT einzeln gesetzt und gespeichert werden.
!!!

!!!danger Reihenfolge
**Zuerst das Spiel starten**, danach das Overlay einstellen. Sonst sind keine Einstellungen möglich.
!!!

---

## Bildwiederholrate / FPS

Für viele wichtiger als reine Auflösung ist eine stabile, hohe **Bildwiederholungsrate (FPS)**. Dafür sorgt der **FPSLocker**.

![Ultrahand - FPSLocker](/images/switch/omninx/overclocking/051_fpslocker_main.jpg)

!!!warning 30-FPS-Limit vieler Spiele
Viele Spiele (z. B. **Zelda – Breath of the Wild**) unterstützen ab Werk **keine Werte über 30 FPS.** Wer höhere FPS ohne passenden Patch einstellt, erlebt dass Figuren und die Welt **deutlich schneller** laufen.
!!!

Um **über 30 FPS** das richtige Spielgefühl zu bekommen, bietet der FPSLocker unter **„Advanced settings“** die nötigen Tools. Dort findest du in der Regel:

- **Check/download config file**
- **Convert config to patch file**

:::content-center
||| Check/Download Config
<a href="/images/switch/omninx/overclocking/052_fpslocker_check-download.jpg" target="_blank" rel="noopener">![FPSLocker – Check/Download](/images/switch/omninx/overclocking/052_fpslocker_check-download.jpg)</a>
||| Convert to Patch
<a href="/images/switch/omninx/overclocking/053_fpslocker_convert.jpg" target="_blank" rel="noopener">![FPSLocker – Convert](/images/switch/omninx/overclocking/053_fpslocker_convert.jpg)</a>
||| Convert (Schritt 2)
<a href="/images/switch/omninx/overclocking/054_fpslocker_convert.jpg" target="_blank" rel="noopener">![FPSLocker – Convert](/images/switch/omninx/overclocking/054_fpslocker_convert.jpg)</a>
|||
:::

Konverter ausführen, Spiel **neustarten**, dann die Bildrate schrittweise bis z. B. **60 FPS** erhöhen.

Für höhere Frameraten brauchst du mehr Leistung; die Switch stößt schnell an Grenzen. **Tears of the Kingdom** kann bei 60 FPS laufen, **Batman: Arkham Knight** vielleicht nur bei ~35 FPS, besonders bei Third-Party-Titeln.

---

## Problembehebung

**Maximale Taktfrequenz zu niedrig**

Solltest du z. B. den GPU-Takt trotz **Uncapped Clocks** nicht über 998/1075 MHz betreiben können, sind zwei Ursachen wahrscheinlich:

1. **Zu hoher Gesamtverbrauch**: Schutzmechanismen in HOC (Safety Settings) drosseln den Takt. Mit **Undervolting** von CPU und RAM entgegenwirken und Handheld-TDP beachten.
2. **CPU High UV vergessen**: Unter **CPU Settings** muss **CPU High UV** mindestens auf **1** stehen. Danach **Neustart**.

!!!danger Boot-Probleme
Startet die Konsole nicht mehr in die CFW: Prüfe `sd:/atmosphere/kips/hoc.kip` und die Einträge in **hekate.ipl**. Im Notfall **hoc.kip** entfernen oder aus einem Backup wiederherstellen.
!!!

!!!info Hänger
Reagiert die Konsole nicht mehr: **Power-Taste lange** drücken zum Neustart.
!!!
