# Overclocking / Undervolting (V1)

## Sicherheitshinweise

!!!info Risiko beim Overclocking
Jedes Overclocking geht über die ursprüngliche Auslegung der Hardware hinaus. Das Risiko hängt davon ab, wie weit du taktest und ob du innerhalb der Chip-Grenzen bleibst.
!!!

!!!danger Instabiles RAM-Overclocking
Instabiles RAM-OC kann **SYSNAND/EMUNAND** und **SD-Karten** beschädigen, besonders auf **SYSNAND**. Teste Einstellungen auf **EMUNAND** und sichere sie, bevor du **Horizon OC** installierst.
!!!

---

## Erista-Grenzen

### Lade-IC (Charger IC)

- Erista nutzt ein **15-A-PMIC**; dieses Limit wird beim Overclocking selten erreicht.
- Der eigentliche Engpass ist das **18-W-Board-Limit**.

### CPU-Grenzen

- Das **18-W-Limit** wird bei **1785 MHz** ohne UV bzw. bei **2091 MHz** mit **CPU UV1** erreicht.

### GPU-Grenzen

- Das **18-W-Limit** wird bei **921 MHz** ohne GPU-UV bei moderaten Speedo-Werten erreicht.

Niedrigere Spannung (**Undervolting, UV**) senkt Verbrauch, Strom und Wärme und hilft, das Board-Limit einzuhalten.

### GPU Scheduling

| Einstellung | GPU-Auslastung |
|-------------|----------------|
| **On** | ~96,7 % |
| **Off** | ~99,7 % |

**Empfehlung:** GPU Scheduling **On**.

!!!danger GPU Scheduling deaktivieren
Deaktiviertes GPU Scheduling erhöht den Stromverbrauch leicht. Mit Vorsicht nutzen.
!!!

---

## Konsole überwachen

- **Status Monitor Overlay** zeigt, ob das Lade-IC-Limit überschritten wurde (z. B. **-1 W** beim Laden).
- Für aussagekräftige Werte: Akku bei **10–90 %** halten.
- Über **90 %** reduziert das Ladegerät die Leistungsabgabe.
- Leicht negativer Verbrauch (ca. **-0,1 W**) bei Akku über 90 % ist unkritisch.
- Deutlich negativer Verbrauch (ca. **-0,5 W**) ist **nicht sicher**.
- Für genaue Messungen mit niedrigerem Akkustand testen.

---

## Speedo und RAM-Typ prüfen

1. **Hekate** starten.
2. **Console Info → HW & Fuses** öffnen.
3. **DRAM ID**, **CPU Speedo**, **GPU Speedo** und **SoC Speedo** notieren.

CPU-/GPU-Speedos liegen etwa bei **1980–2200**, SoC-Speedos bei **1899–2050**. Höhere Speedo-Werte brauchen weniger Spannung für denselben Takt. Ein CPU-/GPU-Speedo um **2100** gilt als gut.

### Speedo-Brackets

- Speedos sind in **Brackets** eingeteilt.
- Der **CPU-UV-Modus** hängt von der Position im Bracket ab; die resultierende **Spannung** hängt vom konkreten Speedo ab.
- Entscheidend ist die **resultierende Spannung**, nicht der UV-Modus allein: Zwei Konsolen mit gleichem UV-Modus können unterschiedliche CPU-Spannungen haben.

---

## RAM-Typen

Erista nutzt verschiedene RAM-Module. Bessere Typen erreichen höhere Takte, brauchen weniger Spannung und vertragen engere Timings als schlechtere Typen. Nicht nur der Typ zählt, sondern auch das **Binning**: schlechtere Typen können bessere übertreffen.

- Samsung **MGCH**
- Hynix **NLE**
- Micron **WT:C**

Fast alle Erista-Konsolen haben **Samsung MGCH**. **Hynix NLE** und **Micron WT:C** sind selten, können aber etwas höhere Takte erreichen – vorsichtig testen.

---

## Horizon OC – Einstellungen

### CPU Settings

| Einstellung | Wert / Empfehlung |
|-------------|-------------------|
| **CPU Boost Clock** | **2091 MHz** (empfohlen); **2295 MHz** nur bei gutem Binning, kann instabil sein |
| **CPU Undervolt Mode** | **1–5** (höchsten stabilen Wert nutzen) |
| **CPU VMIN** | **800 mV** |
| **CPU Max Voltage** | **1225 mV** |

!!!info Boost Mode und PMIC
Das Überschreiten des PMIC-Limits im **Boost Mode** ist unkritisch: Boost läuft nur kurz (typisch unter **30 Sekunden**) und belastet die Hardware nicht dauerhaft.
!!!

### GPU Settings

| Einstellung | Wert / Empfehlung |
|-------------|-------------------|
| **GPU Undervolt Mode** | **HiOpt Table** |
| **GPU VMIN** | **740–780 mV** |
| **GPU Voltage Offset** | **0** |
| **GPU DVFS Offset** | **0** |

**GPU DVFS:** Bei RAM-Overclocking steigt die minimale GPU-Spannung. **DVFS** passt **VMIN** automatisch an den RAM-Takt an. Bei Standard-RAM (**1600 MHz**) ist **GPU DVFS** nicht aktiv.

!!!warning GPU-Takt 998 MHz
Für **998 MHz GPU-Takt** GPU-Spannung **unter 950 mV** halten (exakter Wert variiert je nach IDDQ und Temperatur).
!!!

### RAM Settings

**HP Mode** deaktiviert RAM Power Down.

!!!tip HP Mode
**HP Mode** verbessert die Latenz; manche Module, besonders auf Erista, vertragen ihn nicht.
1. Maximalen RAM-Takt und Timings bei **deaktiviertem** HP Mode finden.
2. Anschließend **HP Mode aktivieren** und erneut testen.
3. Stabil → aktiv lassen, sonst deaktiviert lassen.
!!!

| Einstellung | Wert / Empfehlung |
|-------------|-------------------|
| **DVB Shift** | **1–5** (hebt SoC-Spannung für RAM-Stabilität an); meist reicht **2** |
| **Read Latency (tRWL)** | **2133** |
| **Write Latency (tRWL)** | **2133** |

Höhere Basis-Latenz erlaubt höhere Frequenz bei geringem Latenz-Nachteil. Maximalen Takt mit **2133** Basis-Latenz finden. Latenz erst danach straffen, wenn maximale Frequenz und engste Timings stehen.

- Latenz straffen lohnt nur, wenn die **RAM-Frequenz gleich bleibt**.
- **Write Latency** lässt sich meist aggressiver straffen als **Read Latency**.

#### Samsung MGCH RAM

| Einstellung | Wert / Empfehlung |
|-------------|-------------------|
| **RAM Clock** | **1862–2133+ MHz** (stark abhängig vom Binning) |
| **VDD2** | **1175–1237 mV** (1175 mV garantiert sicher; 1237 mV in L4T erlaubt) |
| **Common Timings** | (4-4-4) 0-1-5-4-6 |
| **Super Tight (ST)** | (4-5-9) 1-2-6-4-6 |

Bis zu **3** individuelle RAM-Frequenzen konfigurierbar. Mit Overvolting sind höhere Takte möglich.

!!!danger RAM-Frequenzen zu nah beieinander
Zwei konfigurierte RAM-Frequenzen innerhalb von **20 MHz** können Systemabstürze auslösen (Bug, vermutlich im offiziellen Sysmodule). Frequenzen mindestens **30 MHz** voneinander trennen.
!!!

### RAM testen (Reihenfolge)

1. Mit **DVB = 2** und Common-Preset starten.
2. **ST-Timings** testen.
3. Schlägt ST fehl: Timings schrittweise lockern in dieser Reihenfolge: **t8 → t1 → t2 → t3 → t6 → t7 → t4 → t5**.
4. Über ST hinaus: gleiches schrittweises Vorgehen.

!!!info Timings t6 und t7
**t6** und **t7** sind stark frequenzabhängig und müssen oft angepasst werden.
!!!

!!!tip Prioritäten beim RAM
- Bei Problemen Timings in der genannten Reihenfolge lockern.
- RAM trägt am meisten zur Gesamtleistung bei: **maximale Frequenz zuerst**.
- **Super Tight** liefert bessere Leistung als Common Timings.
!!!

---

## Feintuning (GPU)

Optional, kann Spannungen weiter senken.

**GPU Voltage Offset**

- Die **High UV Table** ist standardmäßig sehr eng, in manchen Fällen etwas locker.
- **GPU Voltage Offset** strafft sie weiter. Mit **High UV** Werte **-5, -10, -15** oder **-20** testen.
- Manche GPUs werden unter **0** instabil.
- Bei seltenen Speedo-Bracket-Positionen können höhere UV-Offsets funktionieren – vorsichtig testen.

**GPU DVFS Offset**

- Zuerst **Auto**, danach so weit wie möglich senken, sobald die maximale RAM-Frequenz steht.
- **Auto VMIN Offset** bei niedriger Frequenz testen (z. B. **420 MHz**), sonst dominiert die GPU-Spannung über **GPU DVFS**.
- Verbessert die Akkulaufzeit im Handheld bei hohem RAM-OC.
- Positiver Offset ist möglich, sollte nur bei Problemen genutzt werden.

---

## Feintuning (RAM)

Optional, kann die Leistung verbessern.

**Ram Latency** (Read/Write Latency, tRWL)

Standardverhalten:

- Bis einschließlich **1866 MHz**: **1866 tRWL**
- Darüber: **2133 tRWL**

Du kannst verschieben, ab welcher Frequenz das höhere Latenzprofil gilt, Profile mit **`-`** deaktivieren oder alle Custom-Werte entfernen, um zum Standard zurückzukehren.

!!!danger Read und Write getrennt
Lese- und Schreiblatenz sind **immer getrennt** und unabhängig einstellbar.
!!!

!!!info Performance-Hinweise
- **1866 tRWL** kann etwas schneller sein als **2133 max**, nur wenn das RAM die Frequenz ohne Reduktion hält.
- Gleiches gilt für **1600**- und **1333-tRWL**-Profile.
- **1333 tRWL** ist im Handheld oft nützlich, skaliert aber meist nur bis ca. **2133–2400 MHz** (stark abhängig vom RAM-Silizium).
- **Write Latency** lässt sich meist aggressiver (niedriger) setzen als **Read Latency**.
!!!

---

## Takteinstellungen

### Erista [HAC-001] – Maximum (Netzbetrieb)

| Komponente | Takt |
|------------|------|
| **CPU** | **2091 MHz** (nur bei gutem Binning), sonst **1785 MHz** |
| **GPU** | **998 MHz** (nur mit **UV2**, Spannung unter **950 mV** anstreben); **921 MHz** (sicher, mit Undervolt) |
| **RAM** | **1862–2133+ MHz** (stabil, **VDD2** innerhalb **1175 mV**; stark abhängig vom RAM-Typ) |

Sehr gutes Binning kann **2295 MHz** CPU erlauben; instabil oder spannungshungrig, nicht empfohlen.

### Erista [HAC-001] – Maximum sicher (Akku)

| Komponente | Takt |
|------------|------|
| **CPU** | **1785 MHz** |
| **GPU** | **460 MHz** |
| **RAM** | **1862–2133+ MHz** (stabil, **VDD2** innerhalb **1175 mV**; stark abhängig vom RAM-Typ) |

Module mit **2208 MHz+**: im Akkubetrieb höchstens **2188 MHz** nutzen. Der SoC verträgt hohe Frequenzen schlecht; der Verbrauch steigt darüber stark an.

!!!warning Akku-Verbrauch
Dauerhaft **über 8,6 W** im Akkubetrieb kann den Akku schädigen. Vermeide das über längere Zeit.
!!!

---

## Stabilität testen

Für Stabilitätstests siehe die Anleitung [Stabilität testen](/switch/overclocking/testing/).

---

## Problembehebung

**Konsole startet nach HOC-Installation nicht mehr in EMUNAND**

- **Atmosphere** oder **HOC** veraltet → aktualisieren.
- **CPU UV** zu hoch → senken oder auf **0** setzen.

**Konfigurationen werden nicht übernommen**

- Nach Änderungen in **Horizon OC** **Neustart** der Konsole.

**Takte lassen sich nicht über 1785 / 921 / 1600 setzen**

- **KIP** wird nicht geladen → prüfen, ob `sd:/atmosphere/kips/hoc.kip` vorhanden ist.
- **hekate_ipl.ini** falsch konfiguriert:
  - Boot-Eintrag muss `kip1=atmosphere/kips/*` enthalten.
  - Eintrag muss **unter** `pkg3=atmosphere/package3` (oder `fss0`) stehen.

---

## Einrichtungshilfe

Schritt-für-Schritt-Setup (extern, Englisch): [How to get 60 FPS](https://rentry.co/howtoget60fps).
