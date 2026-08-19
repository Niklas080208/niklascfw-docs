---
icon: lock
label: "prod.keys (Lockpick)"
order: 40
description: "prod.keys mit Lockpick RCM in Hekate auslesen und speichern."
---

# prod.keys dumpen mit Lockpick RCM

Falls du noch keine **prod.keys** hast, kannst du sie über **Lockpick RCM** in Hekate dumpen.

!!!info Navigation in Lockpick RCM
In Lockpick funktioniert die Navigation nur mit **Vol+ / Vol−**; bestätigen mit der **Power-Taste**.
!!!

---

## Keys dumpen

>>> Lockpick RCM starten
In **Hekate** unter **Launch** → **Lockpick RCM** auswählen.

![Lockpick RCM in Hekate|700x420](/images/switch/niklascfw-pack/guide1/bild13.jpg)

>>> Dump from SysNAND
**Dump from SysNAND** wählen, **Power** drücken und warten, bis der Dump fertig ist.

>>> Zurück nach Hekate
Mit **Vol+ / Vol−** zu **Reboot to Hekate** navigieren und mit **Power** bestätigen.

![Lockpick Dump abgeschlossen|700x420](/images/switch/niklascfw-pack/guide1/bild14.png)

>>>

!!!success Fertig
Die Keys liegen auf der SD (typisch unter `switch/`). Viele Installer und Tools erwarten `prod.keys` an der vorgesehenen Stelle.
!!!
