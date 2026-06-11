# Arbeitsspeicher (RAM)

Nintendo verbaut unterschiedliche Speichermodule (Samsung, Toshiba, Hynix usw.). Vor dem RAM-OC musst du wissen, **welches Modul** in deiner Konsole steckt, da jedes Modul anders übertaktbar ist.

Die Info findest du in **Hekate** oder unter **Ultrahand → Systeminfo** (z. B. Vendor: Samsung, Modell: K4UBE3D4AA-MGCL).

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

![Hekate Console Info](/images/switch/omninx/overclocking/hekate-ram.gif)

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

---

## Moderates RAM-Overclocking

>>> Erster Versuch: 2200 MHz
Setze **Ram Max Clock** auf **2200 MHz**. Dieser Wert funktioniert erfahrungsgemäß auf den meisten Konsolen. **Common Timings** sowie **VDD2** und **VDDQ** aus der Tabelle übernehmen.
![HOC RAM Clock](/images/switch/omninx/overclocking/hoc-ram-2200.gif)

>>> Höherer Start mit DVB-Shift
Startest du über 2200 MHz, beginne mit **DVB-Shift 10** und reduziere auf **2–6**, sobald die maximale RAM-Geschwindigkeit steht. Höherer DVB-Shift erhöht den Stromverbrauch kaum, aber leicht die Wärmeentwicklung.
![HOC Temporary Overwrites](/images/switch/omninx/overclocking/dvb-shift.gif)

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
- **Höherer Clock ist oft relevanter als extrem niedrige Timings**, wenn z. B. 2800 MHz nur mit Common Timings stabil laufen.
!!!

### HP Mode

**HP Mode** verbessert die Latenz und damit **1 %-Low-Werte** sowie weniger Ruckler. Manche RAM-Module vertragen ihn nicht.

1. Maximalen Takt und Timings bei **deaktiviertem** HP Mode finden.
2. Anschließend **HP Mode aktivieren** und erneut testen.
3. Stabil → aktiv lassen, sonst deaktiviert lassen.
>>>
