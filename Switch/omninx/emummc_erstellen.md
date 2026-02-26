# emuMMC erstellen

---

## Was ist ein emuMMC?

Ein **emuMMC** (emulated MMC) ist eine **virtuelle Kopie** des internen Speichers (eMMC) deiner Nintendo Switch.

### Vorteile

- Du nutzt **Custom Firmware** auf der SD-Karte, ohne die **Original-Firmware** zu verändern.
- **Sicherheit:** Das Original-System bleibt unberührt.
- **Trennung:** CFW und OFW getrennt nutzbar.
  - In der **OFW** kannst du weiterhin **online** mit allen deinen **legitimen Spielen** spielen.

---

## Vorbereitung

Nach der Installation von **OmniNX** kannst du einen **emuMMC** anlegen. Es gibt **zwei Methoden**:

| Typ | Vorteile | Nachteile |
|-----|----------|-----------|
| **SD-File emuMMC** | Einfacher, SD wird nicht formatiert, Backup per Copy & Paste möglich | Kann etwas langsamer sein |
| **SD-Partition emuMMC** | Oft als schneller beschrieben | Mehr Aufwand, SD wird formatiert, alle Daten müssen vorher gesichert werden |

!!!tip Empfehlung
Wir empfehlen meist **SD-Partition** wegen der Stabilität, insbesondere im Zusammenspiel mit unserem **UltraHand**-Ökosystem.
!!!

---

## SD-Partition emuMMC erstellen

!!!danger Wichtig
Bei der **SD-Partition**-Methode wird die SD-Karte **formatiert**. Sichere vorher alle wichtigen Daten!
!!!

### Partitionierung starten

1. **Hekate** starten.
2. Falls du im **Launch-Menü** landest, oben rechts auf **Close** tippen.

![Hekate Close](/images/omninx/emummc/hekate-launch-close.jpeg)

3. In Hekate von **Home** zu **emuMMC** → **Create emuMMC** gehen.

![Hekate Home – emuMMC](/images/omninx/emummc/hekate-home.png)
![emuMMC – Create emuMMC](/images/omninx/emummc/create-emummc.jpg)

4. **SD Partition** auswählen und auf **Continue** tippen.

![SD Partition](/images/omninx/emummc/emummc-continue.jpg)

!!!warning Datenverlust
Wenn deine SD-Daten **größer als 1 GB** sind, wird **alles gelöscht**. Unter 1 GB kann Hekate automatisch sichern und wiederherstellen.
!!!

![Warnung bei > 1GB Daten](/images/omninx/emummc/partition-backup-no.jpg)
![Ok bei < 1GB Daten](/images/omninx/emummc/partition-backup-yes.jpg)

### Partitionsgröße

1. **Switch V1/V2 oder Lite:** Regler auf **29 Full**.

![Regler V1/V2/Lite](/images/omninx/emummc/emummc-29-full.jpg)

2. **Switch OLED:** Regler auf **58 Full**.

![Regler OLED](/images/omninx/emummc/emummc-58-full.jpg)

3. Optional: Für **Linux/Android** die entsprechenden Regler anpassen.

!!!warning Jetzt entscheiden
Diese Wahl solltest du **jetzt** treffen. Später die Partitionsaufteilung zu ändern bedeutet: **alle Partitionen** (inkl. emuMMC) werden gelöscht und neu erstellt. Mach dir die Entscheidung also vorher bewusst.
!!!

### Partitionierung durchführen

1. **Next Step** → **Start** → Meldung mit **Power** bestätigen.

![Next Step](/images/omninx/emummc/partition-next-step.jpg)
![Start](/images/omninx/emummc/partition-start.jpg)

2. Warten, bis die SD-Karte partitioniert ist (**Done**).

![Done](/images/omninx/emummc/partition-done.jpg)

3. Meldung wegdrücken, oben rechts **Close**.

### emuMMC Partition erstellen

1. **emuMMC** → **Create emuMMC** → **SD Partition** -> **Part 1** auswählen und warten.

![Part 1](/images/omninx/emummc/emummc-part1.jpg)

3. Oben rechts **Close**.

![emuMMC erstellt](/images/omninx/emummc/emummc-done.jpg)

---

## SD-File emuMMC erstellen

1. **Hekate** starten.

2. Falls du im **Launch-Menü** landest, oben rechts auf **Close** tippen.

![Hekate Close](/images/omninx/emummc/hekate-launch-close.jpeg)

3. Gehe zu **emuMMC** → **Create emuMMC**.

![emuMMC Create](/images/omninx/emummc/create-emummc.jpg)

4. Wähle **SD File** aus.

![SD File](/images/omninx/emummc/emummc-sdfile.jpeg)

5. Hekate sucht freien Speicher und erstellt den **emuMMC**.

![emuMMC wird erstellt](/images/omninx/emummc/emummc-sdfile-done.jpeg)

6. Wenn der **SD File emuMMC** erstellt wurde, oben rechts auf **Close** tippen.

---

## Prüfe, ob es geklappt hat

Gilt für **SD-Partition** und **SD-File**:

- Im **emuMMC**-Panel sollte unter der emuMMC Info & Selection Sektion ein **grüner Haken** auftauchen.

![emuMMC erstellt](/images/omninx/emummc/emummc-enabled.png)

- **Close** tippen, dann unter **Launch** die **CFW über CFW-EmuMMC** starten.

![Hekate Launch](/images/omninx/emummc/hekate-launch-emummc.jpeg)

---

## Nächste Schritte

!!!success Nächster Schritt
Weiter mit **[Pack einrichten](pack_einrichten)**.
!!!
