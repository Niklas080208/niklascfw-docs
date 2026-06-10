# Start: Roter Faden (0 → fertig)

Diese Seite ist der **rote Faden** durch die Dokumentation: Du kannst Schritt für Schritt vorgehen, unabhängig davon, ob du neu einsteigst oder nur einzelne Punkte nachschlägst.

!!!success Hauptpfad dieser Docs
**OmniNX ist ab jetzt der primäre Installationsweg** in dieser Dokumentation.  
Die folgenden Phasen zeigen den aktuellen, empfohlenen Ablauf von Vorbereitung bis fertigem Setup.
!!!

---

## Phase 1: Konsole & SD klären

[!ref](voraussetzungen/serial_check/serial_check.md)
[!ref](voraussetzungen/richtige_sd)
[!ref](sd_wipe)

---

## Phase 2: RCM und erster Payload

**RCM Softmod**:

[!ref text="RCM-Methode verstehen"](voraussetzungen/serial_check/rcm-methode/rcm-methode.md)
[!ref text="Payload laden (Windows/macOS/Linux)"](voraussetzungen/serial_check/rcm-methode/payload_laden)

Damit erreichst du **Hekate** bzw. den ersten Start über Payload – Grundlage für alles Weitere.

---

## Phase 3: Backup (dringend empfohlen)

Bevor du System- oder emuMMC-Daten veränderst: **SysNAND sichern**.

[!ref](../system-backup/nand_backup)
[!ref](../system-backup/nand_backup_restore)
[!ref](../system-backup/sd_partition_backup_restore)

---

## Phase 4: OmniNX installieren (primärer Pfad)

### 4.1 Überblick und Varianten

[!ref](einfuehrung)

### 4.2 Voraussetzungen-Check (optional)

Wenn du Phase 1 und 2 komplett erledigt hast, kannst du diesen Check meist überspringen.  
Als kompakte Gegenprüfung sind diese Seiten sinnvoll:

[!ref](voraussetzungen/serial_check/serial_check.md)
[!ref](voraussetzungen/richtige_sd)
[!ref](sd_wipe)

### 4.3 Download und Dateien auf SD kopieren

[!ref](download)

### 4.4 OmniNX installieren

[!ref](installation_omninx)

### 4.5 emuMMC erstellen

[!ref](emummc_erstellen)

### 4.6 Pack einrichten (Forwarder, Zeit, Basics)

[!ref](pack_einrichten)

### 4.7 Updates und optionale OC-Themen

[!ref](../updates/omninx-update)
[!ref](../updates/firmware-update)
[!ref](../overclocking)

---

Wenn du bei einem Schritt hängen bleibst, zuerst unter **Fehlerbehebung** nachschlagen oder die verlinkte Detailseite erneut komplett lesen.
