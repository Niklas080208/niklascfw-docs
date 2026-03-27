---
icon: package
label: "OmniNX Pack"
order: 20
author:
  name: NiklasCFW
  avatar: /assets/niklas-pfp.png
---

# OmniNX-Pack aktualisieren

Hier geht es um das **Aktualisieren** des **OmniNX-Packs** (z. B. Standard/Light/OC) in der CFW/emuMMC – per **UltraHand**, **OmniNX Downloader** und **OmniNX Installer**.

---

## Voraussetzungen

!!!warning Uhrzeit
Die **Uhrzeit** sollte synchronisiert sein (z. B. für Downloads). Anleitung: [Einrichtung](/Switch/omninx/pack_einrichten/#systemzeit-synchronisieren).
!!!

---

## CFW-Pack aktualisieren (OmniNX)

>>> UltraHand öffnen
**UltraHand** öffnen (**L** + **R** + **Plus**).

![UltraHand – Home](/images/omninx/updates/pack/ultrahand-home.jpg)
>>> OmniNX Downloader starten
**OmniNX Downloader** in der Paketliste auswählen (**A**).

![OmniNX Downloader auswählen](/images/omninx/updates/pack/ultrahand-home-downloader.jpg)
>>> OmniNX Updater → OmniNX herunterladen
**OmniNX Updater** auswählen, darin die erste Option **OmniNX** wählen und warten, bis der Download abgeschlossen ist.

![OmniNX Downloader – OmniNX Updater](/images/omninx/updates/pack/omninx-downloader.jpg)
![OmniNX Downloader – OmniNX Download](/images/omninx/updates/pack/omninx-downloading.jpg)


!!!info Download und Upload
Ein Vorgang läuft **zweimal** ab: Zuerst wird die Datei (z. B. .zip) **heruntergeladen**, danach auf die SD-Karte **hochgeladen**. Beide Phasen müssen durchlaufen werden.

![Download-Phase](/images/omninx/updates/pack/ultrahand-download.png)
![Upload-Phase](/images/omninx/updates/pack/ultrahand-upload.png)
!!!
>>> Zurück zu UltraHand → RebootNX
Nach dem Download zurück zum **UltraHand**-Hauptbildschirm (Pakete) und **RebootNX** auswählen.

![RebootNX auswählen](/images/omninx/updates/pack/ultrahand-rebootnx.jpg)
>>> In RebootNX: Hekate starten
In RebootNX die **Hekate**-Sektion öffnen und **Hekate** auswählen, um den Bootloader zu starten.

![RebootNX – Hekate-Sektion](/images/omninx/updates/pack/rebootnx-home.jpg)
![Hekate starten](/images/omninx/updates/pack/rebootnx-hekate.jpg)
>>> In Hekate Launch: OmniNX Installer starten
Du landest im **Hekate Launch**-Bildschirm (Staging). Auf den Eintrag **OmniNX Installer** tippen – der Installer-Payload startet.

![Hekate Launch-Menü](/images/omninx/installation/staging-launch.png)
>>> Anzeige prüfen und bestätigen
Der Installer zeigt **Modus** (Update), **Pack-Variante** und **Aktuelle Installation**. Mit **A** (rechter Joy-Con) oder **Power-Taste** bestätigen.

![OmniNX-Installer-Payload](/images/omninx/updates/pack/installer-update-home.jpeg)
!!!info Switch Lite
Bei der **Switch Lite** funktioniert nur die **Power-Taste** zur Bestätigung.
!!!
>>> Update abwarten
Der Installer kopiert die neuen Dateien. Fortschritt auf dem Bildschirm verfolgen.

![Installation](/images/omninx/updates/pack/installer-update-progress.jpeg)
>>> Abschluss – Reboot in Hekate
Wenn **„Erfolgreich“** angezeigt wird, erneut **A** oder **Power** drücken. Der Installer startet **Hekate** neu – danach CFW wie gewohnt starten.

![Installation abgeschlossen](/images/omninx/installation/payload-done.jpeg)
>>> Uhrzeit in Hekate setzen
Nach dem Neustart in **Hekate** die **Uhrzeit** setzen.

![Uhrzeit in Hekate setzen](/images/omninx/installation/hekate-clock.png)
>>>

---

!!!success Fertig
OmniNX-Pack-Update ist abgeschlossen. Bei Problemen: [Fehlerbehebung](/Switch/fehlerbehebung/).
!!!
