---
icon: tools
label: "Partition-emuMMC anpassen"
order: 97
description: "Partition-emuMMC mit NANDFixPro (Level 1) auf eine CFW-kompatible Firmware – Hekate, Windows."
meta:
  description: "SysNAND-Backup, emuMMC-RAW-Sicherung, NANDFixPro Level 1, BOOT0/1. USB 2.0, nur RAW-Partition-emuMMC. Fortgeschrittene."
---

# Partition-emuMMC auf eine CFW-kompatible Firmware anpassen

!!!warning Fortgeschritten & Risiko
Diese Anleitung richtet sich an **erfahrene Nutzer**. Du arbeitest an **eMMC/emuMMC-Daten** und **Firmware-Bestandteilen**. **Downgrades sind riskant** – mach sie nur, wenn du die Folgen einschätzt und **alle Sicherungen** hast. Im Zweifel Schritte **nicht** überspringen. Falsche Bedienung kann zu **Datenverlust** oder einem **nicht mehr startenden System** führen.
!!!

!!!info Optional: Video & Firmware-Links
Wer sich zusätzlich **visuell** einarbeiten will: Auf dem **[YouTube-Kanal des NANDFixPro-Autors](https://www.youtube.com/c/sthetixofficial)** gibt es ein aktuelles Tutorial zum **Level-1**-Downgrade; in der **Videobeschreibung** sind oft direkte **Firmware-Links** eingetragen.
!!!

## Einordnung: Bluescreen & „Atmosphère unterstützt die FW noch nicht“

Wenn die Konsole nach einem **System-Update** in **CFW** (z. B. emuMMC oder „Semi-Stock“) nur noch einen **blauen Bildschirm** zeigt, liegt das oft daran, dass **Atmosphère die installierte Firmware noch nicht unterstützt** – das ist **kein automatischer Brick**.  
**Power-Taste ca. 12 Sekunden halten** erzwingt eine Abschaltung; danach wieder normal in **Hekate** booten.

In **Hekate** kannst du unter **HW & Fuses** u. a. den **Burnt-Fuse-Stand** prüfen und mit einem **Fuse-Check-Payload** abgleichen. **OFW (SysNAND)** sollte weiterhin starten, solange dazu nichts verändert wurde – sinnvoll, das vor riskanten Schritten kurz zu verifizieren.

!!!tip Szene & Updates
Nach Wechseln in der Atmosphère-Entwicklung können **neue Firmware-Releases** eine Weile **ohne passende Atmosphère-Version** bleiben. Wer **nicht warten** will und die Risiken trägt, nutzt u. a. **NANDFixPro Level 1**, um die **RAW-GPP** (hier: des **Partition-emuMMC**) auf eine **niedrigere, von Atmosphère unterstützte** Systemversion anzupassen – **ohne** installierte Titel und Spielstände zu verlieren, wenn alles korrekt läuft.
!!!

## Wann ist das nötig?

Wenn **Atmosphère** die **Firmware deines Partition-emuMMC** (z. B. nach SysNAND-Update und Neuaufbau des emuMMC) **noch nicht unterstützt**, lässt sich der emuMMC **nicht normal in CFW starten**.  
Mit **NANDFixPro** und einer **passenden Ziel-Firmware** wird die **RAW-GPP** des **SD-RAW-Partition-emuMMC** auf diese Version gebracht.

!!-info Voraussetzungen
- **Nur Partition-emuMMC (SD RAW)** – **kein SD-File-emuMMC**: Hekate kann einen **Datei-basierten** emuMMC für dieses Einbinden in **USB-Tools** / die beschriebenen Schritte **nicht** wie die RAW-Partition nutzen (siehe [emuMMC-Typen](emummc_arten)).
- **USB-Datenkabel** **USB-A zu USB-C**; möglichst **USB-2.0**-tauglich. Am PC **keinen USB-3.0-Port** für die Switch verwenden – der **andere USB-Handshake** führt hier oft zu **instabilem Verhalten** oder **Übertragungsfehlern**.
- **Windows-PC**, **Hekate**, **Lockpick RCM** (o. Ä.) zum Key-Dump.
- **Zwei entpackte Ordner** am PC: **NANDFixPro** und **Ziel-Firmware** (jeweils **eigener Ordner**).
!!!

Unterschiedliche emuMMC-Typen: [Welchen emuMMC hab ich?](emummc_arten)

---

## Vorbereitung am PC (zuerst)

Leg **NANDFixPro** und die **Ziel-Firmware** am PC bereit, **bevor** du an der Konsole Keys und Sicherungen erstellst – so bleibt der Ablauf ohne unnötige Unterbrechungen.

>>> NANDFixPro bereitlegen
**NANDFixPro** von [GitHub (Releases)](https://github.com/sthetix/NANDFixPro/releases) laden und das Archiv in einen **eigenen Ordner** entpacken.

![NANDFixPro – entpackter Ordner am PC (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Kompatible Ziel-Firmware
Die **Ziel-Firmware** (muss zu deiner **geplanten Atmosphère-Version** passen) besorgen und in einen **eigenen Ordner** entpacken. **Passende Pakete** findest du über einschlägige **Switch-CFW-Quellen** oder verlinkt z. B. unter Tutorial-Videos zum Thema.

**Hinweis:** **Quellen und Rechtslage** sind **eigenverantwortlich** zu prüfen.

![Firmware-Ordner für NANDFixPro (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)
>>>

---

## prod.keys auslesen

>>> Konsole in Hekate starten
Starte die Konsole in **Hekate**.

>>> Lockpick RCM öffnen
Im **Launch**-Menü **Lockpick RCM** starten.

![Hekate – Launch-Menü mit Lockpick RCM (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Keys vom SysNAND (höchste FW)
Im Lockpick-RCM-Menü mit **Vol +/-** steuern, mit **Power** bestätigen. Wähle **Dump from SysMMC** (bzw. den Eintrag zum Auslesen vom **SysNAND** mit der **höchsten Firmware**).

![Lockpick RCM – Dump from SysMMC / NAND wählen (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Keys auf der SD ablegen
Es werden u. a. **prod.keys** und **dev.keys** unter **`/switch/`** auf der SD (Kartenroot) abgelegt.

>>> Zurück zu Hekate
Zurück ins Lockpick-Hauptmenü, dann **Reboot to Hekate** (Neustart zu Hekate).
>>>

---

## Pflicht: SysNAND komplett sichern (Hekate)

Bevor du den **emuMMC** oder andere NAND-Bereiche anfasst, **sichere den SysNAND vollständig** – das ist die Rückversicherung, falls etwas schiefgeht.

>>> Tools → Backup eMMC (Sys)
Im **Hekate-Hauptmenü** **Tools** → **Backup eMMC**. Hier den **SysNAND** sichern (**SD emuMMC Raw Partition** bleibt **OFF** / Standard für reinen Sys-Backup-Pfad, je nach Hekate-Anzeige).

>>> BOOT0 & BOOT1 (Sys)
Zuerst **eMMC BOOT0 & BOOT1** (bzw. die für den **internen eMMC** angebotenen BOOT0/1-Backups) erstellen.

>>> Anschließend eMMC RAW GPP
Danach **eMMC RAW GPP** sichern. Der Lauf kann je nach **SD-Geschwindigkeit** **sehr lange** dauern – **nicht abbrechen**, warten bis Hekate fertig ist.

![Hekate – SysNAND Backup BOOT0/1 und RAW GPP (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)
>>>

---

## Sicherung des Partition-emuMMC (Hekate)

Zusätzlich – wenn du den **emuMMC auf der SD-RAW-Partition** anpasst – dieselbe Logik für **diesen** emuMMC:

>>> Tools → Backup eMMC
Wieder **Tools** → **Backup eMMC**.

![Hekate – Tools, Backup eMMC (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> SD emuMMC Raw Partition aktivieren
**SD emuMMC Raw Partition** auf **ON** stellen.

>>> BOOT0/1 und RAW GPP des emuMMC
**SD emuMMC BOOT0 & BOOT1** sowie **SD emuMMC RAW GPP** sichern.

![Hekate – SD emuMMC Raw Partition ON, Backup-Optionen (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> USB und SD als Laufwerk
Menü schließen, Switch per **USB** mit dem PC verbinden. **USB Tools** → **Read only** beachten (später **OFF**), zunächst **SD card** wählen, damit der PC die SD sieht.

![Hekate – USB Tools, SD card als Laufwerk (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)
>>>

---

## RAW GPP mit NANDFixPro (Level 1)

>>> Windows 11: Kompatibilitätsmodus (falls nötig)
Unter **Windows 11 (64 Bit)** ggf. für **NANDFixPro.exe** den **Kompatibilitätsmodus Windows 7** setzen: Rechtsklick → Eigenschaften → Kompatibilität.

![Windows – Kompatibilitätsmodus für NANDFixPro.exe (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> NANDFixPro starten
**NANDFixPro.exe** starten. Startet sie nicht, **run.bat** im selben Ordner ausführen. **Popups** ggf. mit **OK** bestätigen, bis alle Komponenten installiert sind.

>>> Level 1 und Ziel-Firmware
Für einen **einfachen Downgrade** nutzt du **Level 1**: Ziel-**Firmware-Ordner** in NANDFixPro auswählen.

![NANDFixPro – Firmware-Ordner auswählen (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Switch verbinden, USB Tools, SD card
Switch per **USB** (möglichst **USB 2.0**) verbinden. In **Hekate** → **Tools** → **USB Tools**: **Read only** auf **OFF**, dann **SD card**.

>>> Get Keys from SD
In NANDFixPro **Get Keys from SD** – **prod.keys**-Import mit **OK** bestätigen. SD am PC **sicher auswerfen**. Auf der Switch Status mit **Close** schließen; **USB** kann je nach Ablauf **zunächst stecken bleiben**.

![NANDFixPro – Get Keys from SD (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Hekate: Emu RAW GPP (Partition-emuMMC)
Zurück in **Hekate**: **eMMC RAW GPP** gilt für den **SysNAND**. Für einen **emuMMC in der RAW-Partition** den Eintrag **Emu RAW GPP** / **emu RAW GPP** wählen (Bezeichnung je nach Hekate-Version).

![Hekate – Read only OFF, Emu RAW GPP (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Start Level 1 Process
In **NANDFixPro**: **Start Level 1 Process** → **YES**. Der Lauf dauert oft **mehrere Minuten** (realistisch **gut 10 Minuten** und mehr, je nach SD und PC) – **warten**, bis **OK** erscheint.

![NANDFixPro – Start Level 1 Process (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> USB neu verbinden, SD card erneut
**USB trennen**, auf der Switch **Close**, Switch **erneut** verbinden, in Hekate wieder **USB Tools** → **SD card**.
>>>

---

## BOOT0/1 auf die SD kopieren und in Hekate schreiben

>>> Copy BOOT to SD
In NANDFixPro **Copy BOOT to SD** → **Yes** → **OK**. SD danach wieder **sicher auswerfen**.

![NANDFixPro – Copy BOOT to SD (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> USB entfernen, Hekate Restore
Popups schließen, **USB** abziehen. **Tools** → **Restore eMMC**. **SD emuMMC Raw Partition** **ON**.

![Hekate – Restore eMMC, SD emuMMC Raw Partition (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> SD emuMMC BOOT0 & BOOT1 wiederherstellen
**SD emuMMC BOOT0 & BOOT1** aus der **Sicherung** zurückschreiben. **Power**-Abfragen und **Hinweise** in Hekate **bestätigen** (Text genau lesen). **RAW GPP** in diesem Schritt **nicht** verwechseln.

![Hekate – Restore SD emuMMC BOOT0 & BOOT1 (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)
>>>

---

## Abschluss und Prüfung

>>> CFW starten
Über **Home** / **Close** ins **Launch**-Menü, **Atmosphère** (bzw. deinen **emuMMC-CFW**-Eintrag) starten – kein Bluescreen mehr, wenn Version und Schritte passen.

![Hekate – Launch-Menü, CFW starten (Platzhalter)|700x420](/images/switch/allgemein/placeholder.png)

>>> Firmware-Version prüfen
Unter **Systemeinstellungen → Konsole** die **Systemversion** prüfen – sie soll der **Ziel-Firmware** entsprechen. **Spiele und Daten** bleiben bei korrektem Ablauf erhalten.
>>>

---

## Siehe auch

[!ref](emummc_arten)
[!ref text="SD-Partition: Sicherung und Wiederherstellung (emuMMC)"](../../system-backup/sd_partition_backup_restore)
[!ref target="blank" text="NANDFixPro (GitHub)"](https://github.com/sthetix/NANDFixPro/releases)
[!ref target="blank" text="Sthetix (YouTube)"](https://www.youtube.com/c/sthetixofficial)
