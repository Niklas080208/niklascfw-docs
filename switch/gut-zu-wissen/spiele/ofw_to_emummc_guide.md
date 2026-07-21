---
icon: sync
label: "OFW zu emuMMC Guide"
order: 105
description: "OFW-Spiele und Updates in die emuMMC übernehmen, ohne Spielstände zu verlieren."
---

# OFW-Spiele + Updates in emuMMC übernehmen (ohne Saves zu verlieren)

Du holst Spiele und Updates aus der echten Firmware (OFW) in eine neue emuMMC über und kannst sie dabei auch auf dem PC dumpen und archivieren. **Spielstände (Saves) bleiben erhalten.**

!!!warning Voraussetzungen für das Dumpen
Das funktioniert nur, wenn **alle** Bedingungen erfüllt sind:

- Deine Konsole muss zur **Ticketverwendung registriert** sein.
- Unter **Einstellungen → Nutzer → Nutzername → Online-Lizenz-Einstellung** muss diese **Aus** sein.
!!!

---

## Schritte im Detail

>>> In OFW Spiele und Updates installieren
In die normale Firmware (**SysNAND**) booten und Wunschspiele + Updates installieren.

>>> Neue emuMMC erstellen
**Hekate** → **Close** → `emuMMC` → `Create emuMMC` → **SD File** (**keine Partition!**). Beispiel: `emuMMC/SD00/`.

>>> Nintendo-Ordner kopieren
SD am PC: `Nintendo/` vom SD-Root nach `emuMMC/SD00/Nintendo/` (bzw. dein SD-Slot).

>>> In die neue emuMMC wechseln
**Hekate** → **Close** → `emuMMC` → `Change emuMMC` → neue SD-File-emuMMC → booten.

!!!warning Bei Linkalho
**Den Original-Account nicht durch einen Fake-Account ersetzen!** Mit echtem Account gekaufte Spiele brauchen den Account – sonst fehlen Lizenzen und **DBI kann nicht dumpen**.
!!!

>>> DBI starten und MTP verwenden
**R** gedrückt halten → Album/Spiel starten → **DBI** im HB-Menü.

1. **MTP Responder** starten.
2. Switch per **USB** mit dem PC verbinden.
3. Ordner **`Installed Games`** → Spiele/Updates auf den PC kopieren.

!!!tip Cartridge Game Updates
Cartridge-Updates erscheinen unter `SD Install` nur, wenn das Base-Game vorher per DBI/Sphaira installiert wurde.
!!!

[!ref Spiele von Gamecards installieren](spiele_installation_dbi_sphaira)

>>> Zurück zur Ziel-emuMMC
**Change emuMMC** → Ziel-emuMMC → booten → **DBI** → **MTP Responder** → **`SD Install`** → Spiele/Updates installieren.

>>>

!!!success Fertig
Spiele und Updates liegen in der Ziel-emuMMC; Saves bleiben erhalten.
!!!

---

## Temporären SD-File-emuMMC löschen {#aufraumen}

Der SD-File-emuMMC aus Schritt 2 war nur ein **Zwischenschritt**. Nach erfolgreicher Installation in der **Ziel-emuMMC** kannst du ihn löschen.

!!!warning Erst aufräumen, wenn alles übertragen ist
Nur löschen, wenn Spiele in der **Ziel-emuMMC** installiert und getestet sind.
!!!

>>> Ziel-emuMMC aktivieren
**Hekate** → **Close** → `emuMMC` → `Change emuMMC` → **Ziel-emuMMC** wählen.

>>> SD-File-emuMMC entfernen
**Option A (Hekate):** `emuMMC` → unter **SD FILE** temporären Eintrag (z. B. `SD00`) löschen.

**Option B (PC):** SD am PC → Ordner `emuMMC/SD00/` (bzw. Slot) des **temporären** emuMMC löschen.

>>>

!!!tip Speicherplatz
Ein SD-File-emuMMC belegt mehrere GB – nach dem Löschen steht der Platz wieder für Spiele zur Verfügung.
!!!

[!ref text="Ausführlicher Guide (erweitert)"](../../erweiterte-guides/ofw_to_emummc_guide)
