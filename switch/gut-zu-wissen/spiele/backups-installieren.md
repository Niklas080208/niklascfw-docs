# Backups installieren (XCI / XCZ / NSP / NSZ)

Installiere Switch-Backups über **Sphaira (MTP Install)** oder **DBI (MTP Responder)** per USB vom PC.

---

## Dateiformate

{.compact .striped}

| Format | Bedeutung |
| --- | --- |
| **XCI** | 1:1 Cartridge-Dump (Base Game, ggf. Updates/DLC) |
| **XCZ** | Komprimierte XCI, kleinere Datei |
| **NSP** | eShop-Format (Spiele, Updates, DLC) |
| **NSZ** | Komprimierte NSP, Dekompression beim Install |

!!!tip USB 3.0
Nutze ein **USB-3-Kabel** und einen **USB-3-Port** am PC für stabile MTP-Übertragung.
!!!

---

+++ Sphaira – MTP Install
>>> Sphaira und MTP Install
**Sphaira** starten → **Minus (−)** → **MPT Install** (MTP Install).

>>> Switch per USB verbinden
Am PC erscheinen u. a.:

- Album (Image SD)
- Games
- **Install (NSP, XCI, NSZ, XCZ)** ← **hierhin kopieren**
- microSD card

>>> Dateien kopieren
Backups (**XCI, XCZ, NSP, NSZ**) in **Install (NSP, XCI, NSZ, XCZ)** ziehen. Sphaira startet die Installation automatisch, sobald Dateien den Ordner erreichen.
>>>

+++ DBI – MTP Responder
>>> DBI MTP Responder
**DBI** → **MTP Responder**. Die Switch erscheint am PC mit mehreren „Laufwerken“.

>>> Richtigen Install-Ordner wählen
Unter anderem:

- 1: SD Card
- …
- **5: SD Card install** ← **Install-Ordner**
- 6: NAND install
- …

>>> Dateien kopieren
Backups nach **5: SD Card install** kopieren. DBI installiert automatisch beim Einchecken der Dateien.
+++

!!!success Fertig
Installierte Titel erscheinen nach Abschluss in der CFW wie gewohnt.
!!!
