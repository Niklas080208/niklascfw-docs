# Android und Linux installieren (UltraHand)

Zwei Wege: **SD Partition emuMMC (RAW)** oder **SD File emuMMC (SD00)**. Wähle die Methode, die zu deinem emuMMC-Typ passt.

---

## Voraussetzungen

!!!warning Uhrzeit synchronisieren
**Bitte darauf achten, dass deine Uhrzeit synchronisiert ist.**  
Ansonsten funktioniert der Download über UltraHand nicht!
!!!

[!ref text="Uhrzeit mit DBI synchronisieren (NTP)"](../../nachher/dbi_time)

Es gibt **zwei verschiedene Arten** von emuMMC:

1. **SD Partition** – weit verbreitet, z. B. **RAW1**
2. **SD File** – z. B. **SD00**

[!ref text="Welchen emuMMC hab ich?"](../system/emummc_arten)

!!!warning Backup vor jeder Änderung
**Macht bitte, bevor ihr irgendetwas macht, ein Backup.**
!!!

!!!tip Android- und Linux-Partition schon bestellt?
Solltet ihr die Switch erst zurückbekommen haben und Android- sowie Linux-Partition schon bestellt haben, macht direkt **Schritt 4 und 5** – unabhängig vom emuMMC-Typ.
!!!

---

+++ Methode 1: SD Partition emuMMC (RAW)
Diese Methode ist für dich, wenn deine SD-Karte als **RAW-Partition** eingerichtet ist.

>>> Backup erstellen
Wie in der Anleitung **SD Partition Backup und Restore** – **aber:** SD **nicht** wechseln und nach dem Backup **kein Restore** durchführen.

[!ref text="SD Partition Backup und Restore (emuMMC)"](../../system-backup/sd_partition_backup_restore)

- Starte **Hekate** und geh zu **Tools → Backup eMMC**.
- Aktiviere **SD emuMMC Raw Partition**.
- Führe nacheinander die Backups für **Boot0 & Boot1** und **SD emuMMC RAW GPP backup** durch.
- Nimm die SD-Karte aus der Switch und verschiebe das Backup aus `\backup\f2dc5397\emummc` (der Ordnername kann bei dir anders heißen) nach `\backup\f2dc5397\restore\emummc` – sonst schlägt der Restore später fehl.
- Sichere anschließend den **kompletten SD-Inhalt** auf deinem PC.

>>> SD-Karte für Android vorbereiten (Partitionierung)
**Wichtig:** Nach dem Backup alle Dateien von der SD-Karte löschen – **außer** dem Ordner `bootloader` und der Datei `payload.bin`.

- Stecke die SD-Karte wieder in deine Switch.
- Geh in Hekate zu **Tools → Partition SD Card**.
- Verschiebe die Partitionen für **emuMMC (RAW)** und **Android** an die gewünschte Stelle. Denk daran: Android braucht **mindestens 32 GB**. Da du Apps nicht auf der SD-Karte installieren kannst, überleg dir die Größe gut.

>>> Daten wiederherstellen (Restore)
**Hier den Restore machen** – wie in der Anleitung **SD Partition Backup und Restore**.

[!ref text="SD Partition Backup und Restore (emuMMC)"](../../system-backup/sd_partition_backup_restore)

- Kopiere alle deine gesicherten Daten zurück auf die SD-Karte.
- Geh in Hekate zu **Tools → Restore → eMMC**.
- Aktiviere **SD emuMMC Raw Partition**.
- Führe die Restores für **Boot0 & Boot1** und **SD emuMMC RAW GPP** durch.

>>> Android und/oder Linux herunterladen
- Boote in deine CFW und lade die Android- und/oder Linux-Installationsdateien über **UltraHand (L + R + Plus) → OmniNX Downloader → Android und/oder Linux** herunter.
- **Achtung:** Die Switch darf während des Downloads **nicht** in den Standby gehen.

![OmniNX Downloader|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/niklascfwdl.jpg)

![Android laden|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/downloaderandroid.jpg)

![Linux laden|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/downloaderlinux.jpg)

>>> Android installieren
- Boote die Switch neu (**Reboot NX → Hekate**). Die Switch startet direkt in Hekate.
- Geh zu **Tools → Partition SD Card** und wähle **Flash Android**.
- Bestätige mit **Continue**, wenn „Do you want to reboot into Recovery to finish Android installation?“ erscheint.
- Im Recovery-Menü machst du einen **Factory Reset** (**Format data/factory reset**).
- Geh zurück und wähle **Apply Update → Choose from Switch SD**. Scrolle bis **Switchroot** – dort liegen die Installationsdateien.
- Installiere zuerst die **LineageOS-Datei** und anschließend die **Gapps-Datei**.

![Reboot NX → Hekate|500x320](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/rebootnxhekate.jpg)

>>> Linux installieren
- Boote die Switch neu (**Reboot NX → Hekate**). Die Switch startet direkt in Hekate.
- Geh zu **Tools → Partition SD Card** und wähle **Flash Linux**.
- Der Linux-Flasher öffnet sich und fragt, ob du **Continue** (Weiter) oder **Cancel** (Abbrechen) wählen willst.

- Klicke unten links auf **Nyx Settings**.

![Nyx Settings|700x420](/images/switch/allgemein/hekate_nyx_settings.jpg)

- Wähle **Dump Joy-Con BT** aus und bestätige die Meldung mit **Ok**.

>>>

+++ Methode 2: SD File emuMMC
Diese Methode ist die einfachste, wenn dein emuMMC bereits im **SD File-Format** vorliegt.

>>> Backup erstellen
- Nimm die SD-Karte aus der Switch und sichere **alle Dateien** auf deinem PC.

>>> SD-Karte für Android vorbereiten (Partitionierung)
**Wichtig:** Nach dem Backup alle Dateien von der SD-Karte löschen – **außer** dem Ordner `bootloader` und der Datei `payload.bin`.

- Stecke die SD-Karte wieder in die Switch.
- Geh zu **Tools → Partition SD Card** und erstelle die Partition für Android. Du kannst die Größe frei wählen, aber beachte die Mindestanforderung von **32 GB**. Da keine Apps auf der SD-Karte installiert werden können, wähle die Größe sorgfältig.

>>> Daten wiederherstellen
- Kopiere alle zuvor gesicherten Daten wieder auf die SD-Karte.

>>> Android und/oder Linux herunterladen
- Boote in deine CFW und lade die Android- und/oder Linux-Installationsdateien über **UltraHand (L + R + Plus) → OmniNX Downloader → Android und/oder Linux** herunter.
- **Achtung:** Die Switch darf während des Downloads **nicht** in den Standby gehen.

![OmniNX Downloader|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/niklascfwdl.jpg)

![Android laden|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/downloaderandroid.jpg)

![Linux laden|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/downloaderlinux.jpg)

>>> Android installieren
- Boote die Switch neu (**Reboot NX → Hekate**). Die Switch startet direkt in Hekate.
- Geh zu **Tools → Partition SD Card** und wähle **Flash Android**.
- Bestätige mit **Continue**, wenn „Do you want to reboot into Recovery to finish Android installation?“ erscheint.
- Im Recovery-Menü machst du einen **Factory Reset** (**Format data/factory reset**).
- Geh zurück und wähle **Apply Update → Choose from Switch SD**. Scrolle bis **Switchroot** – dort liegen die Installationsdateien.
- Installiere zuerst die **LineageOS-Datei** und anschließend die **Gapps-Datei**.

![Reboot NX → Hekate|500x320](/images/switch/gut-zu-wissen/erweiterte-systeme/android-linux/rebootnxhekate.jpg)

>>> Linux installieren
- Boote die Switch neu (**Reboot NX → Hekate**). Die Switch startet direkt in Hekate.
- Geh zu **Tools → Partition SD Card** und wähle **Flash Linux**.
- Der Linux-Flasher öffnet sich und fragt, ob du **Continue** (Weiter) oder **Cancel** (Abbrechen) wählen willst.

>>> Joy-Con dumpen
- Klicke unten links auf **Nyx Settings**.

![Nyx Settings|700x420](/images/switch/allgemein/hekate_nyx_settings.jpg)

- Wähle **Dump Joy-Con BT** aus und bestätige die Meldung mit **Ok**.
+++
