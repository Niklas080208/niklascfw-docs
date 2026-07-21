# NAND Backup wiederherstellen

Mit dieser Anleitung spielst du ein **SysNAND-Backup** zurück auf die interne eMMC. Voraussetzung ist das Backup aus **[NAND Backup erstellen](nand_backup)**.

!!!danger Nur dein eigenes Backup verwenden
Stelle **ausschließlich** das Backup wieder her, das du selbst von **dieser** Konsole erstellt hast. Ein falsches Backup kann die Switch unbrauchbar machen.
!!!

---

## Restore vorbereiten

>>> Backup-Ordner auf die SD legen
Liegt `backup/` nicht mehr auf der microSD, kopiere den Ordner zurück in den **Root** der SD-Karte.

>>> Restore-Ordner anlegen
Öffne `backup/xxxxxx/` und verschiebe **BOOT0**, **BOOT1** und **rawnand.bin.XX** (exakte Bezeichnung siehe Screenshot) in den Unterordner `backup/xxxxxx/restore/`.

![Backup-Dateien für Restore vorbereiten|700x420](/images/switch/system-backup/nand-backup/restore_pc.jpg)

---

## Restore in Hekate

>>> Hekate öffnen und Tools starten
Starte **Hekate** und tippe auf **Tools**.

![Hekate Tools|700x420](/images/switch/system-backup/nand-backup/hekate_tools.jpg)

>>> Restore eMMC öffnen
Wähle **Restore eMMC**.

![Restore eMMC|700x420](/images/switch/system-backup/nand-backup/restore_emmc2.jpg)

>>> BOOT0 und BOOT1 wiederherstellen
Wähle **eMMC BOOT0 & BOOT1** und warte, bis der Vorgang abgeschlossen ist. Anschließend oben rechts **Close** tippen.

![Restore BOOT0 & BOOT1|700x420](/images/switch/system-backup/nand-backup/restore_emmc1.jpg)

>>> RAW GPP wiederherstellen
Wähle **eMMC RAW GPP** und warte, bis der Vorgang abgeschlossen ist. Anschließend erneut **Close** tippen.

![Restore RAW GPP|700x420](/images/switch/system-backup/nand-backup/restore_emmc3.jpg)

>>> Switch neustarten
Starte die **Switch neu**. Optional kannst du den `backup/`-Ordner danach wieder von der SD löschen.

>>>

!!!success Fertig
Die SysNAND wurde wiederhergestellt. Bei Problemen: [Fehlerbehebung](/switch/fehlerbehebung/system-boot/hekate_fix_archive_bits).
!!!
