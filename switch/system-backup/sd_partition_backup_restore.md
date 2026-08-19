# SD Partition Backup und Restore (emuMMC)

Diese Anleitung gilt für **partition-basierten emuMMC** auf der microSD (RAW Partition). Du sicherst die emuMMC-Partition und stellst den Inhalt danach wieder her – auf derselben SD oder nach einem Wechsel auf eine neue Karte.

!!!info Wann brauche ich das?
Nur wenn dein emuMMC als **SD emuMMC Raw Partition** eingerichtet ist – nicht bei **file-basiertem** emuMMC. Unsicher? In Hekate unter **emuMMC** nachsehen, welcher Typ aktiv ist.
!!!

---

+++ Gleiche SD
Backup und Restore auf **derselben** microSD – z. B. vor dem Neu-Partitionieren für Android/Linux, ohne die Karte zu tauschen.

>>> Backup erstellen
In **Hekate:** **Tools → Backup eMMC**. Unten **SD emuMMC Raw Partition** auf **An** stellen.

Oben links **Boot0** und **Boot1** sichern. Wenn fertig → **Close**.

Unten links **SD emuMMC RAW GPP backup** starten. Wenn fertig → **Close**.

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>

>>> Restore-Ordner vorbereiten
Nach dem Backup entsteht ein gleichnamiger **Ordner** auf der SD. Der **Inhalt** aus dem `emummc`-Ordner muss in den **Restore-Ordner** `emummc` verschoben werden – sonst schlägt der Restore fehl.

![Backup in den Restore-Ordner verschieben (1)|700x420](/images/switch/system-backup/sd-partition/backup_in_den_restore_ordner_verschieben_1.png)

![Backup in den Restore-Ordner verschieben (2)|700x420](/images/switch/system-backup/sd-partition/backup_in_den_restore_ordner_verschieben_2.png)

>>> Restore durchführen
**Tools → Restore → eMMC.** Unten **SD emuMMC Raw Partition** auf **An** stellen.

Oben links **Boot0** und **Boot1** wiederherstellen. Wenn fertig → **Close**.

Unten links **SD emuMMC RAW GPP** wiederherstellen. Wenn fertig → **Close**.

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>
>>>

+++ Wechsel auf neue SD
Backup auf der alten Karte, Wechsel auf eine **neue** microSD, Partitionierung und Restore.

>>> Backup erstellen
In **Hekate:** **Tools → Backup eMMC**. Unten **SD emuMMC Raw Partition** auf **An** stellen.

Oben links **Boot0** und **Boot1** sichern. Wenn fertig → **Close**.

Unten links **SD emuMMC RAW GPP backup** starten. Wenn fertig → **Close**.

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>

>>> Backup-Ordner und SD-Inhalt sichern
Nach dem Backup entsteht ein gleichnamiger **Ordner** auf der SD. **Alle Daten von der SD-Karte auf den PC sichern** – die SD kann in der Switch oder am PC stecken.

!!!warning Switch ausschalten
Bevor du die microSD entnimmst, die **Switch vollständig ausschalten**.
!!!

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Nach_dem_Backup_Ausschalten_und_an_den_PC.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Nach_dem_Backup_Ausschalten_und_an_den_PC.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>

>>> Restore-Ordner vorbereiten
Der **Inhalt** aus dem `emummc`-Ordner muss in den **Restore-Ordner** `emummc` verschoben werden – sonst schlägt der Restore fehl.

![Backup in den Restore-Ordner verschieben (1)|700x420](/images/switch/system-backup/sd-partition/backup_in_den_restore_ordner_verschieben_1.png)

![Backup in den Restore-Ordner verschieben (2)|700x420](/images/switch/system-backup/sd-partition/backup_in_den_restore_ordner_verschieben_2.png)

>>> Neue SD vorbereiten
Für das Partitionieren reichen im **Root** der neuen SD:

- Ordner `bootloader/`
- Datei `payload.bin`

![Neue SD vorbereiten|700x420](/images/switch/system-backup/sd-partition/neue_sd_fertig_machen_neu.png)

**Tools → Partition SD Card.** Die emuMMC-Partition (RAW) so verschieben, bis **Zahl + FULL** angezeigt wird.

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/SD_Partitionieren_fur_SD_File_Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/SD_Partitionieren_fur_SD_File_Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>

!!!tip SD aus der Switch entnehmen
Das Video zeigt den Weg, wenn du die SD **zum schnelleren Kopieren** lieber am PC bearbeitest. Vor dem Entnehmen: Switch ausschalten.
!!!

>>> SD-Inhalt zurückkopieren
**Close → USB Tools → SD Card → SD UMS** starten und alle gesicherten Dateien wieder auf die SD kopieren. Alternativ über den SD-Slot am PC.

![Fehlenden SD-Inhalt zurückkopieren|700x420](/images/switch/system-backup/sd-partition/fehlender_sd_inhalt_wieder_auf_die_switch_kopieren.png)

![SD fertig vorbereitet|700x420](/images/switch/system-backup/sd-partition/sd-fertig.png)

>>> Restore durchführen
**Tools → Restore → eMMC.** Unten **SD emuMMC Raw Partition** auf **An** stellen.

Oben links **Boot0** und **Boot1** wiederherstellen. Wenn fertig → **Close**.

Unten links **SD emuMMC RAW GPP** wiederherstellen. Wenn fertig → **Close**.

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>
>>>
+++

---

!!!success Restore abgeschlossen
Du kannst wieder normal in den **emuMMC** booten und CFW wie gewohnt nutzen.
!!!

<video controls preload="metadata" style="width: 100%; max-width: 640px;">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Boot_emuMMC.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Boot_emuMMC.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>
