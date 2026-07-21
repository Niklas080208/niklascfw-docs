---
icon: archive
label: "JKSV (Spielstände)"
order: 105
description: "Spielstände mit JKSV sichern, wiederherstellen und auf andere Switches übertragen."
---

# Spielstände sichern und wiederherstellen mit JKSV

**JKSV** sichert, stellt wieder her und verwaltet **Speicherstände** auf der Switch – pro Benutzer und Spiel.

---

## Funktionen

{.list-icon}
- :icon-archive: Backups auf die SD-Karte (`/JKSV/…`)
- :icon-sync: Restore und Transfer auf andere CFW-Switches
- :icon-person: Alle Benutzerkonten und zugehörige Saves

!!!tip Forwarder / Title Override
Starte JKSV im **Highmemory-Mode** ( **R** + Spielstart oder Forwarder) – nicht nur über das Album.
!!!

---

## Spielstände sichern

>>> JKSV starten
Switch in **CFW** booten, **JKSV** öffnen.

>>> Profil und Spiel wählen
Benutzerprofil → Spiel → **Y** (*Backup*).

>>> Backup benennen
Namen vergeben (z. B. `Zelda_2025-08-11`). Save liegt unter `/JKSV/[Spielname]/[Backupname]/`.

>>>

---

## Spielstände wiederherstellen

>>> JKSV starten
Benutzerprofil → Spiel → gewünschtes Backup.

>>> Restore
**X** (*Restore*) → bestätigen. Der Save wird ins System kopiert.

>>>

!!!info Cloud-Backup
Optional: Spielstände nach **Google Drive** oder **WebDAV** hochladen.
!!!

[!ref](jksv_cloud)

!!!tip Regelmäßig sichern
Vor Modding, Updates oder Experimenten immer ein frisches Backup anlegen.
!!!
