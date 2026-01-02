# 💾 SD Partition Backup und Restore (emuMMC)

---

## 🔄 Backup erstellen

1. **Tools → Backup eMMC**  
2. Unten: **SD emuMMC Raw Partition** → auf **An**  
3. **Oben links**: `Boot0` und `Boot1` sichern → wenn fertig → **Close**  
4. **Unten links**: `SD emuMMC RAW GPP backup` starten → wenn fertig → **Close**  

<video width="640" controls poster="/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.png">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Backup_SD_Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>

5. Nach dem Backup entsteht ein gleichnamiger **Ordner** auf der SD.  
6. **Alle Daten von der SD-Karte auf den PC sichern**  
   - SD kann in der Switch oder im PC stecken → egal  
   - **Wichtig:** Bei SD-Entnahme Switch ausschalten!


<video width="640" controls poster="/images/SD-Partition-Backup-und-Restore/Nach_dem_Backup_Ausschalten_und_an_den_PC.png">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Nach_dem_Backup_Ausschalten_und_an_den_PC.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Nach_dem_Backup_Ausschalten_und_an_den_PC.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>




---

## ⚠️ Wichtiger Hinweis für Restore

- Der **Inhalt** aus dem `emummc`-Ordner **muss in den Restore-Ordner** `emummc` verschoben werden.

![|700x420](/images/SD-Partition-Backup-und-Restore/Backup_in_den_Restore_Ordner_verschieben_1.png)

![|700x420](/images/SD-Partition-Backup-und-Restore/Backup_in_den_Restore_Ordner_verschieben_2.png)


---

## 📦 SD vorbereiten vor dem Restore

![|700x420](/images/SD-Partition-Backup-und-Restore/Neue_SD_Fertig_machen_neu.png)

Zum Partitionieren reicht:  
   - Ordner: `bootloader`  
   - Datei: `payload.bin`  
   → beide im Root der SD  

1. **Tools → Partition SD Card**  
2. Die emuMMC (RAW) so weit verschieben, **bis Zahl + FULL** steht.

<video width="640" controls poster="/images/SD-Partition-Backup-und-Restore/SD_Partitionieren_fur_SD_File_Partition.png">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/SD_Partitionieren_fur_SD_File_Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/SD_Partitionieren_fur_SD_File_Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>



**Hinweis** Das Video Zeigt den Weg wenn man die SD für das schnellere kopieren lieber aus der Switch entnimmt. 

3. **Close** > **USB Tools** > **SD Card** und dann **SD UMS** starten und alle Dateien wieder auf die SD kopieren  
   - Alternativ: über PC-SD-Slot  
   - **Wichtig:** Bei SD-Entnahme Switch ausschalten!

Fehlender SD Inhalt wieder auf die Switch SD kopieren 

![|700x420](/images/SD-Partition-Backup-und-Restore/Fehlender_SD_Inhalt_wieder_auf_die_Switch_kopieren.png)

Fertig SD ab in die Switch und Restore machen.


![|700x420](/images/SD-Partition-Backup-und-Restore/SD-Fertig.png)



---

## ♻️ Restore durchführen

1. **Tools → Restore → eMMC**  
2. Unten: **SD emuMMC Raw Partition** → auf **An**  
3. **Oben links**: `Boot0` und `Boot1` wiederherstellen → wenn fertig → **Close**  
4. **Unten links**: `SD emuMMC RAW GPP` wiederherstellen → wenn fertig → **Close**

<video width="640" controls poster="/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.png">
  <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.mp4" type="video/mp4">
  Dein Browser unterstützt kein HTML5-Video.
  <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Restore-SD-Partition.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>



---

## ✅ Fertig
- Jetzt kannst du wieder normal in den **emuMMC** booten.


<video width="640" controls poster="/images/SD-Partition-Backup-und-Restore/Restore-Testen.png">
    <source src="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Boot_emuMMC.mp4" type="video/mp4">
    Dein Browser unterstützt kein HTML5-Video.
    <a href="https://cdn.niklascfw.de/docs/images/SD-Partition-Backup-und-Restore/Boot_emuMMC.mp4" target="_blank">Video in neuem Tab öffnen</a>
</video>



---
