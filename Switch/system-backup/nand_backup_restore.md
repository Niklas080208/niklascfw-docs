# NAND Backup wiederherstellen

> Es wird **zwingend das NAND Backup** benötigt, welches wir im Tutorial **[NAND Backup erstellen](https://docs.niklascfw.de/switch/system-backup/nand_backup/)** erzeugt haben.

1. Sofern du den `backup` Ordner nicht mehr auf deiner MicroSD gespeichert hast, so kopiere diesen wieder in den **Root** deiner Speicherkarte.
2. Öffne den Ordner `backup/xxxxxx` und verschiebe die Dateien **BOOT0**, **BOOT1** und **rawnand.bin.XX** (genaue bezeichnung siehe Screenshot) in den Ordner `backup/xxxxxx/restore`.

![|700x420](/images/nand_backup/restore_pc.jpg)
3. Starte nun in **Hekate**.
4. Klicke auf **Tools**

![| Tools|700x420](/images/nand_backup/hekate_tools.jpg)
5. Geh auf **Restore eMMC**

![| Restore|700x420](/images/nand_backup/restore_emmc2.jpg)
6. Wähle **eMMC BOOT0 & BOOT1** aus und warte bis der Vorgang abgeschlosen ist, drücke anschließend oben rechts Close.

![| eMMC BOOT0 & BOOT1|700x420](/images/nand_backup/restore_emmc1.jpg)
7. Wähle **eMMC RAW GPP** aus und warte bis der Vorgang abgeschlosen ist, drücke anschließend oben rechts Close.

![| eMMC RAW GPP|700x420](/images/nand_backup/restore_emmc3.jpg)
8. Jetzt kannst du deine **Switch neustarten** und ggf. den `backup` Ordner wieder von der Speicherkarte löschen.