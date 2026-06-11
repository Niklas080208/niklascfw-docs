# Begrifflichkeiten

| Menüpunkt | Bedeutung |
|-----------|-----------|
| **Edit App Profile** | Homebrew-/Spiel-spezifische Übertaktungswerte |
| **Edit Global Profile** | Globale Werte für alles (werden durch **App Profile** überschrieben, falls gesetzt) |
| **Temporary Overrides** | Temporäre Werte; werden durch Neustart zurückgesetzt |
| **Settings** | Voreinstellungen (Taktfrequenz, Timing, Spannung usw.) |
| **About** | Entwicklerinfos und Danksagungen |

### Settings (Untermenüs)

| Untermenü | Beschreibung |
|-----------|--------------|
| **General Settings** | Allgemeine Voreinstellungen |
| **Safety Settings** | Grundlegende Systemeinstellungen für Takt- und Energiemanagement |
| **RAM Settings** | RAM-spezifische Einstellungen (Taktfrequenz, Timings, Latenz) |
| **CPU Settings** | CPU-spezifische Einstellungen (Boost, Undervolt, Voltage) |
| **GPU Settings** | GPU-spezifische Einstellungen (Taktfrequenz, Voltage, UV-Tabelle) |
| **Display Settings** | Anzeigebezogene Einstellungen |

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
| **Step Mode** | Schrittweite der Frequenzliste (z. B. 66 MHz: 1600 → 1666 → 1733) |
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
| **CPU Boost Clock** | Kurzzeit-Boost (z. B. für Ladezeiten) |
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
