# NAND Backup erstellen

Ein **SysNAND-Backup** sichert den internen Speicher deiner Switch (eMMC). Lege es an, **bevor** du CFW installierst oder Systemdaten veränderst.

!!!info Was wird gesichert?
- **eMMC BOOT0 & BOOT1** – kleine Partitionen, Backup dauert nur Sekunden
- **eMMC RAW GPP** – Hauptsystempartition; kann je nach SD-Karte und Switch-Modell **bis zu 45 Minuten** dauern
!!!

---

## Backup in Hekate erstellen

>>> Hekate öffnen und Tools starten
Starte **Hekate** und tippe auf **Tools**.

![Hekate Tools|700x420](/images/switch/system-backup/nand-backup/hekate_tools.jpg)

>>> Backup eMMC öffnen
Wähle **Backup eMMC**.

![Backup eMMC|700x420](/images/switch/system-backup/nand-backup/backup_emmc.jpg)

>>> BOOT0 und BOOT1 sichern
Wähle **eMMC BOOT0 & BOOT1**. Der Vorgang dauert nur wenige Sekunden.

![eMMC BOOT0 & BOOT1|700x420](/images/switch/system-backup/nand-backup/backup_emmca.jpg)

Ist das Backup fertig, tippe oben rechts auf **Close**.

![Backup BOOT abgeschlossen|700x420](/images/switch/system-backup/nand-backup/backup_emmcb.jpg)

>>> RAW GPP sichern
Wähle **eMMC RAW GPP**. Je nach SD-Karte und Switch-Version kann das **bis zu 45 Minuten** dauern.

![eMMC RAW GPP|700x420](/images/switch/system-backup/nand-backup/backup_emmcc.jpg)

Ist das Backup fertig, erneut oben rechts auf **Close** tippen.

![Backup GPP abgeschlossen|700x420](/images/switch/system-backup/nand-backup/backup_emmcd.jpg)

>>> Backup auf den PC kopieren
Verbinde die Switch per USB mit dem PC. Im **Root** der microSD findest du einen Ordner `backup/` – kopiere ihn **vollständig auf deinen PC** und lösche ihn anschließend von der SD, wenn du Speicherplatz brauchst.

>>>

!!!success Fertig
Das SysNAND-Backup liegt sicher auf dem PC.
!!!

[!ref](nand_backup_restore)

!!!danger Nicht nur auf der SD lassen
Ein Backup **nur** auf der microSD schützt nicht vor SD-Ausfall oder versehentlichem Löschen. Archiviere `backup/` immer **zusätzlich am PC** (oder extern).
!!!
