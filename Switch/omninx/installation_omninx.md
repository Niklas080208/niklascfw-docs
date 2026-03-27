---
icon: rocket
label: "Installation"
order: 55
author:
  name: NiklasCFW
  avatar: /assets/niklas-pfp.png
---

# Installation von OmniNX

Nach dem [Download](download) und dem Kopieren des Packs auf die SD-Karte startest du hier den **OmniNX Installer** und führst die Installation durch.

---

## Was der Installer macht

Der **OmniNX Installer** erkennt automatisch:

- **Welche Variante** auf der SD liegt (Standard / Light / OC).
- **Ob OmniNX schon installiert ist** (über `sd:/config/omninx/manifest.ini`).

Daraus wählt er:

- **Update-Modus:** Nur CFW-relevante Ordner/Dateien werden ersetzt, **Spielstände und installierte Spiele bleiben erhalten**.
- **Saubere Installation:** Kompletter Wipe von atmosphere, bootloader, config, switch; **DBI**, **Tinfoil** und **prod.keys** werden gesichert und danach wiederhergestellt.

---

## Installation durchführen

>>> SD-Karte einstecken, Switch starten und OmniNX Installer starten
**SD-Karte** wieder in die Switch stecken und die **Switch starten**. Du landest im **Hekate Launch**-Bildschirm – dort siehst du direkt die GUI mit dem **OmniNX Installer**. Einfach auf den Eintrag **OmniNX Installer** tippen, dann startet der Installer-Payload.

![Hekate Launch-Menü](/images/omninx/installation/staging-launch.png)
>>> Anzeige prüfen und bestätigen
Der Installer zeigt **Modus** (Update/Saubere Installation), **Pack-Variante** (Standard/Light/OC) und **Aktuelle Installation**. Mit **A (rechter Joy-Con)** oder **Power-Taste** bestätigen, um die Installation zu starten.



![OmniNX-Installer-Payload](/images/omninx/installation/payload-home.jpeg)
!!!info Switch Lite
Bei der **Switch Lite** funktioniert nur die **Power-Taste** zur Bestätigung.
!!!
>>> Installation abwarten
Der Installer kopiert alle Dateien in die SD-Root, legt **config/omninx/manifest.ini** an und räumt den Pack-Ordner weg. Fortschritt auf dem Bildschirm verfolgen. Bei **sauberer Installation** werden DBI, Tinfoil und prod.keys vorher gesichert und danach wiederhergestellt.

![Installation](/images/omninx/installation/payload-installation.jpeg)
>>> Abschluss
Wenn „Erfolgreich“ angezeigt wird, erneut **A** oder **Power** drücken. Der Installer startet automatisch **Hekate** (über `sd:/bootloader/update.bin`).

![Installation abgeschlossen](/images/omninx/installation/payload-done.jpeg)
>>> Uhrzeit in Hekate setzen (nach Reboot)
Nach dem Neustart in **Hekate** die **Uhrzeit** setzen.

![Platzhalter: Uhrzeit in Hekate setzen](/images/omninx/installation/hekate-clock.png)
>>>

!!!success Nach der Installation
- **Bereits emuMMC:** **Launch** → **CFW-EmuMMC** → CFW starten.
- **Noch kein emuMMC:** Weiter mit **[emuMMC erstellen](emummc_erstellen)**.
- **Nur einrichten:** Weiter mit **[Pack einrichten](pack_einrichten)**.
!!!

==- Fehler? (Troubleshooting)
**„Kein Pack gefunden“:** Ordner **OmniNX Standard**, **OmniNX Light** oder **OmniNX OC** muss genau auf der **Root** der SD-Karte liegen (nicht in einem Unterordner).

**Payload startet nicht:** Prüfe, ob `OmniNX-Installer.bin` in **sd:/bootloader/payloads/** liegt und Hekate die neueste Version ist.
===
