---
icon: alert
label: "Problembehebung"
order: 10
---

# Problembehebung

### Maximal einstellbare Taktfrequenzen zu niedrig

Solltest du z. B. den GPU-Takt trotz **Uncapped Clocks** nicht über 998/1075 MHz betreiben können, sind zwei Ursachen wahrscheinlich:

1. **Zu hoher Gesamtverbrauch**: Schutzmechanismen in HOC (Safety Settings) drosseln den Takt. Mit **Undervolting** von CPU und RAM entgegenwirken und Handheld-TDP beachten.
2. **CPU High UV vergessen**: Unter **CPU Settings** muss **CPU High UV** mindestens auf **1** stehen. Danach **Neustart**.
3. **High UV Table**: Diese Spannungstabelle muss aktiv sein damit **Werte über 1152 MHz** einstellbar werden.

!!!danger Boot-Probleme
Startet die Konsole auf Grund zu aggressiver Übertaktungswerte nicht mehr, kann man ganz einfach über eine zusätzliche Ini-Datei in die CFW booten und diese korrigieren. Zu finden unter: **Hekate - More Config - "CFW-EmuMMC (Kein OC)"**
!!!

!!!info Hard-Reset
Reagiert die Konsole nicht mehr: **Power-Taste lange** drücken zum Neustart.
Ein lautes Knacken ist dabei normal, da der Audioverstärker nur bei kontrolliertem Abschalten die Lautsprecher stumm schaltet. Beim apprupten Abschalten (Zwangsneustart) erzeugen deshalb unregulierte Spannungspitzen das hörbare Knacken.
!!!

### Hängenbleiben im 'Standby'

Es kann vorkommen, dass z. B. wenn man die Konsole über Nacht in den Standby-Modus versetzt, diese am nächsten Morgen nicht mehr aufwacht sprich im Blackscreen hängen bleibt. Mögliche Ursache hier ist ein **zu hoher "CPU Low UV"-Wert.** Da hilft dann nur ein Hardreset und erneutes anpassen der Werte und Testen bis die Konsole wieder regulär "aufwacht".

!!!info Entwicklerempfehlung
Die Entwickler von Horizon OC empfehlen generell den "CPU Low VMIN" etwas zu höher (620 - 640 mV) und dann mit "CPU Low UV" diesen für den Betrieb runterregeln zu lassen. Ein zu niedrige Minimalspannung hat keinerlei Vorteil.

