# Anleitung: Android und Linux installieren per neuen Ultrahand Methode 🛑Achtung 2 Verschiedene❗

---

Achtung es gibt 2 Verschiedene Arten von emuMMC 

1) SD Partition weit Verbreitet>RAW1

2) SD File>SD00


Welchen du hast? Findest du unter **[Welchen emuMMC hab ich?](https://docs.niklascfw.de/switch/gut-zu-wissen/system/emummc_arten/)**



MACHT BITTE BEVOR IHR IRGENDWAS MACHT EIN BACKUP

> Tipp💡  
> Solltet ihr die Switch erst zurück bekommen haben und Ihr habt Android-Partition und die Linux-Partition schon bestellt dann macht direkt die 4 und 5 unabhängig des Emummc.


---

## Methode 1: SD Partition emuMMC (RAW1)

Diese Methode ist für dich, wenn deine SD-Karte als **RAW-Partition** eingerichtet ist.

### 1) Backup erstellen 

- Wie in **[SD Partition Backup und Restore (emuMMC)](https://docs.niklascfw.de/switch/system-backup/sd_partition_backup_restore/)** 
>⚠️ nur nicht die SD Wechseln und nach dem Backup kein Restore⛔️

- Starte Hekate und geh zu **Tools > Backup eMMC**.
- Aktiviere **SD emuMMC Raw Partition**.
- Führe nacheinander die Backups für **Boot0 & Boot1** und **SD emuMMC RAW GPP backup** durch.
- Nimm die SD-Karte aus der Switch und verschiebe das Das Backup das du in \backup\f2dc5397(der kann bei dir anders heißen)\emummc findest. Nach \backup\f2dc5397(der kann bei dir anders heißen)\restore\emummc (Sonnst schlägt nachher der Restore fehl)
- Sichere anschließend den **kompletten SD Inhalt** auf deinem PC.

### 2) SD-Karte für Android vorbereiten (Partitionierung)
- **Wichtig:** nach dem Backup Lösche alle Dateien von der SD-Karte, **außer** dem Ordner `bootloader` und der Datei `payload.bin`.
- Stecke die SD-Karte wieder in deine Switch.
- Geh in Hekate zu **Tools > Partition SD Card**.
- Verschiebe die Partitionen für **emuMMC (RAW)** und **Android** an die gewünschte Stelle. Denk daran: Android braucht **mindestens 32 GB**. Da du Apps nicht auf der SD-Karte installieren kannst, überleg dir die Größe gut.

### 3) Daten wiederherstellen (Restore)

> 🚨Hier den Restore machen! Wie in **[SD Partition Backup und Restore (emuMMC)](https://docs.niklascfw.de/switch/system-backup/sd_partition_backup_restore/)** 
- Kopiere alle deine gesicherten Daten zurück auf die SD-Karte.
- Geh in Hekate zu **Tools > Restore > eMMC**.
- Aktiviere **SD emuMMC Raw Partition**.
- Führe die Restores für **Boot0 & Boot1** und **SD emuMMC RAW GPP** durch.

### 4) Android und/oder Linux herunterladen:
- Boote in deine CFW und lade die Android-Installationsdateien oder Linux-Installationsdateien über **Ultrahand > Niklas CFW downloader >Android und/oder Linux** herunter.
- **Achtung:** Die Switch darf nicht in den Standby gehen während des Downloads.

1) NiklasCFW Downloader
--![|700x420](/images/android-und-linux-installieren-per-neuen-ultrahand-methode/NiklasCFWDL.jpg)--


2) Android Laden
--![|700x420](/images/android-und-linux-installieren-per-neuen-ultrahand-methode/DownloaderAndroid.jpg)--


3) Linux Laden
--![|700x420](/images/android-und-linux-installieren-per-neuen-ultrahand-methode/DownloaderLinux.jpg)--

### 5) Android installieren
- Boote die Switch neu (Reboot NX > Hekate). Die Switch startet direkt in Hekate.
- Geh zu Tools > Partition SD Card und wähle Flash Android.,
- Bestätige mit Continue, wenn "Do you want to reboot into Recovery to finish Android installation?" erscheint.
- Im Recovery-Menü machst du einen Factory Reset (Format data/factory reset).
- Geh zurück und wähle Apply Update > Choose from Switch SD. **Scroll bis Switchroot** da drin sind dann die installationsdateien.
  Installiere zuerst die LineageOS-Datei und anschließend die Gapps-Datei. 

--![|500x320](/images/android-und-linux-installieren-per-neuen-ultrahand-methode/rebootnxhekate.jpg)--

### 5) Linux Installieren
- Boote die Switch neu (Reboot NX > Hekate). Die Switch startet direkt in Hekate.
- Geh zu Tools > Partition SD Card und wähle Flash Linux.
  Der Linux Flasher öffnet sich und fragt ob du Continue (Weiter) machen oder Cancel (Abbrechen) willst.


---


## Methode 2: Android-Partition mit bestehendem SD File emuMMC

Diese Methode ist die einfachste, wenn dein emuMMC bereits im **SD File-Format** vorliegt.

### 1) Backup erstellen
- Nimm die SD-Karte aus der Switch und sichere **alle Dateien** auf deinem PC.

### 2) SD-Karte für Android vorbereiten (Partitionierung)
- **Wichtig:** Lösche nach dem Backup alle Dateien von der SD-Karte, **außer** dem Ordner `bootloader` und der Datei `payload.bin`.
- Stecke die SD-Karte wieder in die Switch.
- Geh zu **Tools > Partition SD Card** und erstelle die Partition für Android. Du kannst die Größe frei wählen, aber beachte die Mindestanforderung von **32 GB**.  
  Da keine Apps auf der SD-Karte installiert werden können, wähle die Größe sorgfältig.

## 3) Daten wiederherstellen
- Kopiere alle zuvor gesicherten Datennwieder auf die SD-Karte.

### 4) Methode 2: Android-Partition mit bestehendem SD File emuMMC
- Boote in deine CFW und lade die Android-Installationsdateien über **Ultrahand > Niklas CFW downloader >Android und/oder Linux** herunter.
- **Achtung:** Die Switch darf nicht in den Standby gehen während des Downloads. 

### 5) Android installieren
- Boote die Switch neu (Reboot NX > Hekate). Die Switch startet direkt in Hekate.
- Geh zu Tools > Partition SD Card und wähle Flash Android.,
- Bestätige mit Continue, wenn "Do you want to reboot into Recovery to finish Android installation?"erscheint.
- Im Recovery-Menü machst du einen Factory Reset (Format data/factory reset).
- Geh zurück und wähle Apply Update > Choose from Switch SD. **Scroll bis Switchroot** da drin sind dann die installationsdateien.
- Installiere zuerst die LineageOS-Datei und anschließend die Gapps-Datei.

### 5) Linux Installieren
- Boote die Switch neu (Reboot NX > Hekate). Die Switch startet direkt in Hekate.
- Geh zu Tools > Partition SD Card und wähle Flash Linux.
- Der Linux Flasher öffnet sich und fragt ob du Continue (Weiter) machen oder Cancel (Abbrechen) willst.

