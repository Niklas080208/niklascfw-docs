---
icon: cpu
label: "CPU / GPU"
order: 60
---

# CPU / GPU

Um CPU und/oder GPU zu übertakten sind weniger Schritte nötig als beim RAM, aber dennoch einiges zu beachten.

CPU-Takt spielt unter Atmosphere bei den meisten Apps und Spielen eine **untergeordnete** Rolle; Fokus liegt auf **RAM-Durchsatz** und **GPU**. Extremes OC lohnt selten, **Stabilität** hat Priorität.

**Undervolting (UV)** ist nötig für Stabilität und begrenzten Strombedarf. Im Handheld weiterhin **max. 8,6 W** (V2/OLED) bzw. **6,5 W** (Lite) einhalten. Gelegentliche Spitzen sind unkritisch, dauerhaft höhere Werte vermeiden.

!!!warning V1-Konsolen
Bei der ältesten Konsolengeneration (V1) ist Overclocking zwar möglich, sollte aber mit **extremer Vorsicht** genossen werden. Wir raten davon ab; diese Anleitung ist explizit **nicht** dafür ausgelegt.
!!!

Wie flexibel CPU und GPU beim Übertakten sind, hängt von vielen Faktoren ab. Ein **Speedo**-Wert (Ultrahand → **+** → **System**) über **1600** bei Mariko-Chips (V2, Lite, OLED) ist ein gutes Zeichen für ein positives Ergebnis.

Die einzelnen Einstellungsparameter findest du unter [Begrifflichkeiten](begrifflichkeiten).

---

## CPU

Die ersten Einstellungsparameter der CPU sollten immer die festen Spannungswerte und Clock-Frequenzen umfassen. Laufen diese nach einem Neustart stabil, kann mit dem Undervolting begonnen werden.

### Empfohlene Startwerte

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

---

## GPU

Stelle zuerst die CPU-Werte ein, bevor du die GPU taktest.

Bei der GPU auf **Artefakte** neben Abstürzen achten; sie treten oft erst nach einigen Minuten im Spiel auf und werden von falschen Spannungswerten oder zu hohem Versatz (Offset) erzeugt. Hier gilt: **weniger ist mehr**, Standard ist völlig in Ordnung.

Relevant ist vor allem die **GPU Voltage Table**, da man hier die nicht standardmäßig eingestellten Frequenzen ab 1267 MHz aktivieren kann. Frequenzen **über 1305 MHz** GPU-Takt nur mit **extremer Vorsicht**; hier droht am ehesten Hardwareschaden.

### Empfohlene Startwerte

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
