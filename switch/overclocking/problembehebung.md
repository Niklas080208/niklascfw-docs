---
icon: alert
label: "Problembehebung"
order: 10
---

# Problembehebung

**Maximale Taktfrequenz zu niedrig**

Solltest du z. B. den GPU-Takt trotz **Uncapped Clocks** nicht über 998/1075 MHz betreiben können, sind zwei Ursachen wahrscheinlich:

1. **Zu hoher Gesamtverbrauch**: Schutzmechanismen in HOC (Safety Settings) drosseln den Takt. Mit **Undervolting** von CPU und RAM entgegenwirken und Handheld-TDP beachten.
2. **CPU High UV vergessen**: Unter **CPU Settings** muss **CPU High UV** mindestens auf **1** stehen. Danach **Neustart**.

!!!danger Boot-Probleme
Startet die Konsole nicht mehr in die CFW: Prüfe `sd:/atmosphere/kips/hoc.kip` und die Einträge in **hekate.ipl**. Im Notfall **hoc.kip** entfernen oder aus einem Backup wiederherstellen.
!!!

!!!info Hänger
Reagiert die Konsole nicht mehr: **Power-Taste lange** drücken zum Neustart.
!!!
