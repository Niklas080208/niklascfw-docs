---
icon: cpu
label: "Switch Firmware"
order: 10
author:
  name: NiklasCFW
  avatar: /assets/niklas-pfp.png
---

# Firmware updaten

Hier geht es um das **Aktualisieren** der **Switch-Firmware** (Horizon OS) in der CFW/emuMMC mit **Daybreak**.

---

## Voraussetzungen

!!!warning Uhrzeit
Die **Uhrzeit** sollte synchronisiert sein (z. B. für Downloads). Anleitung: [Einrichtung](/switch/omninx/pack_einrichten/#systemzeit-synchronisieren).
!!!

---

## Firmware der CFW (emuMMC) updaten

!!!info Firmware-Update
Die **neueste Firmware** ist nicht immer nötig. Spätestens wenn ein **Spiel** ein Update verlangt, kannst du aktualisieren. Sollte eine Firmware nicht empfohlen sein, wird das bekannt gegeben.
!!!

### Firmware herunterladen (UltraHand / OmniNX Updater)

>>> UltraHand öffnen
**UltraHand** öffnen (**L** + **R** + **Plus**).

![UltraHand – Home](/images/switch/omninx/updates/pack/ultrahand-home.jpg)
>>> OmniNX Downloader starten
**OmniNX Downloader** in der Paketliste auswählen (**A**).

![OmniNX Downloader auswählen](/images/switch/omninx/updates/pack/ultrahand-home-downloader.jpg)
>>> OmniNX Updater → Firmware herunterladen
**OmniNX Updater** auswählen, darin die **Firmware**-Option (z. B. gewünschte Version) wählen und warten, bis der Download abgeschlossen ist.

![UltraHand – OmniNX Downloader](/images/switch/omninx/updates/pack/omninx-downloader.jpg)
![OmniNX Downloader – Firmware Download](/images/switch/omninx/updates/firmware/omninx-updater-firmware.jpg)
>>>

---

### Firmware installieren (Daybreak)

1. **UltraHand** schließen, **Sphaira** starten.
2. **Daybreak** öffnen.

![Daybreak](/images/switch/omninx/updates/firmware/daybreak-start.jpg)

3. **Install** wählen.
4. **Firmware-Verzeichnis** wählen (z. B. **Firmware.21.0.1**).

![Firmware-Verzeichnis wählen](/images/switch/omninx/updates/firmware/daybreak-fw-select.jpg)

5. Daybreak prüft die Firmware (**Update is valid!**).
6. **Continue** → **Preserve Settings**.
7. **Install (FAT32 + exFAT)** wählen.
8. **Continue** bestätigen (**Ready to begin update installation**).
9. Installation abwarten (100 %), dann **Reboot**.

![Daybreak – Install](/images/switch/omninx/updates/firmware/daybreak-check-continue.jpg)
![Preserve Settings](/images/switch/omninx/updates/firmware/daybreak-preserve.jpg)
![Install FAT32 + exFAT](/images/switch/omninx/updates/firmware/daybreak-exfat.jpg)
![Firmware Update](/images/switch/omninx/updates/firmware/daybreak-continue.jpg)
![Reboot](/images/switch/omninx/updates/firmware/daybreak-install-finished.jpg)

10. Nach dem Neustart ist die neue Firmware aktiv.

---

!!!success Fertig
Firmware-Update ist abgeschlossen. Bei Problemen: [Fehlerbehebung](/switch/fehlerbehebung/).
!!!
