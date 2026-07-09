---
icon: sync
label: "OFW zu emuMMC Guide"
order: 100
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
- In die normale Firmware (**SysNAND**) booten.
- Wunschspiele und Updates ganz normal installieren.

>>> Neue emuMMC erstellen
- **Hekate** → **Close** → `emuMMC` → `Create emuMMC`
- **SD File** wählen (**keine Partition!**)
- Beispiel: es wird `emuMMC/SD00/` erstellt (je nach Slot auch `SD01`, `SD02` usw.)

>>> Nintendo-Ordner kopieren
- SD-Karte in den PC stecken.
- Den ganzen `Nintendo`-Ordner vom SD-Hauptverzeichnis kopieren nach `emuMMC/SD00/Nintendo` (bzw. den Ordner deiner neuen emuMMC).

>>> In die neue emuMMC wechseln
- **Hekate** → **Close** → `emuMMC` → `Change emuMMC`
- Deine neue SD-File-emuMMC auswählen.
- In diese emuMMC booten.

!!!warning Bei Linkalho
**Den Original-Account nicht durch einen Fake-Account ersetzen!**

Wenn du mit einem echten Account heruntergeladen hast, **darfst du ihn nicht löschen oder durch Linkalho ersetzen** – sonst fehlen die Lizenzen und **DBI kann die Spiele nicht dumpen**.
!!!

>>> DBI starten und MTP verwenden
!!-info DBI via Title Override starten
Falls du DBI noch nie genutzt hast:

- **R-Taste** gedrückt halten und z. B. das **Album** oder ein **Spiel** starten.
- Du landest im Homebrew-Menü → **DBI** starten.
!!!

!!!tip Cartridge Game Updates
Für **Cartridge Game Updates** muss das Cartridge Game **vorher über DBI oder Sphaira installiert** werden, damit die Updates unter `SD Install` angezeigt werden.

[!ref Spiele von Gamecards installieren](../gut-zu-wissen/spiele/spiele_installation_dbi_sphaira.md)
!!!

1. **MTP Responder** starten.
2. Switch per **USB** mit dem PC verbinden.
3. Am PC erscheint die Switch wie ein USB-Laufwerk.

Öffne den Ordner **`Installed Games`** – dort kannst du Spiele und Updates auf den PC kopieren.

>>> Zurück zur Ziel-emuMMC
- In Hekate erneut **Change emuMMC** → die emuMMC wählen, in der die Spiele dauerhaft liegen sollen.
- In diese emuMMC booten.
- **DBI** öffnen und den **MTP Responder** starten.
- Diesmal **`SD Install`** wählen → Spiele und Updates auf der SD installieren.
>>>

!!!success Fertig
Deine Spiele und Updates sind in der Ziel-emuMMC. Saves bleiben erhalten, alles sauber übertragen.
!!!

---

## Temporären SD-File-emuMMC löschen {#aufraemen}

Der in Schritt 2 erstellte **SD-File-emuMMC** (z. B. `emuMMC/SD00/`) war nur als **Zwischenschritt** zum Dumpen gedacht. Nach der Installation in deine **Ziel-emuMMC** kannst du ihn **entfernen** und so **Speicherplatz** auf der SD-Karte freigeben.

!!!warning Erst aufräumen, wenn alles übertragen ist
Lösche den temporären emuMMC nur, wenn die Spiele und Updates in der **Ziel-emuMMC** installiert sind und du sie dort getestet hast.
!!!

>>> Sicherstellen, dass die Ziel-emuMMC aktiv ist
- **Hekate** → **Close** → `emuMMC` → `Change emuMMC`
- Deine **Ziel-emuMMC** (nicht den temporären SD-File-emuMMC) auswählen.

>>> SD-File-emuMMC löschen
**Option A – über Hekate:**

- **Hekate** → **Close** → `emuMMC`
- Unter **SD FILE** den temporären Eintrag (z. B. `SD00`) auswählen und **löschen**

**Option B – am PC:**

- Switch ausschalten, SD-Karte in den PC stecken.
- Den Ordner `emuMMC/SD00/` (bzw. `SD01`, `SD02` …) des **temporären** emuMMC komplett löschen.
- SD-Karte sicher auswerfen und zurück in die Switch legen.
>>>

!!!tip Speicherplatz
Ein SD-File-emuMMC belegt mehrere GB. Nach dem Löschen steht dir der freigewordene Platz wieder für Spiele und andere SD-Inhalte zur Verfügung.
!!!
