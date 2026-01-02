# emuMMC erstellen

---

## 📖 Was ist ein emuMMC?

Ein **emuMMC (emulierte SD Card)** ist eine virtuelle Version bzw. eine 1:1 Kopie des **internen Speichers (eMMC)** einer Nintendo Switch.

### Vorteile

- Ermöglicht die Nutzung einer **Custom Firmware (CFW)** auf der SD-Karte
- **System-Modifikationen** ohne Änderung der originalen Firmware
- **Sicherheit**: Originales System bleibt unverändert

---

## 📌 Vorbereitung

Nachdem du das **CFW Pack** installiert hast (wir empfehlen natürlich unser [NiklasCFW_Pack](https://github.com/Woody-NX/NiklasCFW_Pack/releases/latest)), musst du einen **emuMMC** erstellen.

### Zwei Möglichkeiten

| Typ | Vorteile | Nachteile |
|-----|----------|-----------|
| **SD-File emuMMC** | • Einfacher zu installieren<br>• SD-Karte wird nicht formatiert<br>• Daten-Sicherung per Copy & Paste möglich | • Möglicherweise langsamer* |
| **SD-Partition emuMMC** | • Soll angeblich schneller arbeiten* | • Erfordert mehr Aufwand<br>• Sicherung nur über Umwege möglich<br>• SD-Karte wird formatiert<br>• Alle Daten müssen vorher gesichert werden |

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>* Das mit der Geschwindigkeit kann ich nicht bestätigen.</small></p>
</div>

<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">💡 Empfehlung</h4>
<p style="color: #212529; margin-bottom: 0;">Meine persönliche Empfehlung bleibt bei <strong>SD File</strong>. Was du wählst, bleibt dir überlassen.</p>
</div>

---

## 📁 SD-File emuMMC erstellen

1. Starte **Hekate**
2. Falls du im **Launch Menü** landest, klicke oben rechts auf **Close**

![|700x420](/images/Guide2/Bild1.jpg)

3. Gehe zu **emuMMC** → **Create emuMMC**
4. Wähle **SD File** aus

![|700x420](/images/Guide2/Bild2.jpg)
![|700x420](/images/Guide2/Bild3.jpg)

5. **Hekate** sucht nun nach freiem Speicher und erstellt einen **emuMMC**
6. Wenn der **SD File emuMMC** erstellt wurde, klicke oben rechts auf **Close**

### Erfolg prüfen

- Links oben sollte ein **grüner Haken** sein
- Es sollte **Enabled!** stehen
- Du kannst jetzt oben rechts auf **Close** klicken
- Gehe zu **Launch** und starte die **CFW über CFW-EmuMMC**

---

## 🗂️ SD-Partition emuMMC erstellen

<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">⚠️ Wichtig</h4>
<p style="color: #212529; margin-bottom: 0;">Bei der SD-Partition-Methode wird die SD-Karte <strong>formatiert</strong>! Sichere alle wichtigen Daten vorher!</p>
</div>

### Schritt 1: Partitionierung starten

1. Wähle **SD Partition** aus
2. Klicke auf **Continue**

![|700x420](/images/Guide2/Bild4.jpg)

<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">⚠️ Datenverlust Warnung</h4>
<p style="color: #212529; margin-bottom: 0;">Die <strong>gelb markierte Meldung</strong> erscheint, wenn deine SD-Karten-Daten <strong>größer als 1 GB</strong> sind. In diesem Fall wird <strong>alles gelöscht</strong>!</p>
<ul style="color: #212529; margin-bottom: 0;">
<li>Wenn deine Daten <strong>kleiner als 1 GB</strong> sind: Hekate sichert die Daten automatisch und stellt sie nach der Partitionierung wieder her.</li>
<li>Wenn deine Daten <strong>größer als 1 GB</strong> sind: Sichere sie vorher auf dem PC oder akzeptiere den Datenverlust mit <strong>OK</strong>.</li>
</ul>
</div>

![|700x420](/images/Guide2/Bild5.jpg)
![|700x420](/images/Guide2/Bild6.jpg)

### Schritt 2: Partition-Größe einstellen

1. **Switch V1/V2 oder Lite**:  
   Stelle den **roten Regler** auf **29 Full**

![|700x420](/images/Guide2/Bild7.jpg)

2. **Switch OLED**:  
   Stelle den **roten Regler** auf **58 Full**

![|700x420](/images/Guide2/Bild8.jpg)

3. **Linux/Android (optional)**:  
   Falls du zukünftig Linux oder Android nutzen möchtest, stelle die entsprechenden Regler auf deine Wunsch-Größe ein.

### Schritt 3: Partitionierung durchführen

1. Klicke unten rechts auf **Next Step**
2. Wähle **Start** aus
3. Bestätige die nächste Meldung mit der **Power-Taste**

![|700x420](/images/Guide2/Bild9.jpg)
![|700x420](/images/Guide2/Bild10.jpg)

4. Die SD-Karte wird nun partitioniert
5. Wenn dies abgeschlossen ist, steht **Done** da
6. Drücke diese Meldung weg und klicke oben rechts auf **Close**

![|700x420](/images/Guide2/Bild11.jpg)

### Schritt 4: emuMMC auf Partition erstellen

1. Gehe zu **emuMMC** → **Create emuMMC** → **SD Partition**
2. Eine andere Meldung erscheint
3. Wähle **Part 1** aus
4. Warte, bis dies abgeschlossen ist
5. Klicke oben rechts auf **Close**

![|700x420](/images/Guide2/Bild12.jpg)
![|700x420](/images/Guide2/Bild13.jpg)

### Erfolg prüfen

- Links oben sollte ein **grüner Haken** sein
- Es sollte **Enabled!** stehen
- Du kannst jetzt oben rechts auf **Close** klicken
- Gehe zu **Launch** und starte die **CFW über CFW-EmuMMC**

---

## ✅ Nächste Schritte

Wenn du deinen **emuMMC** erfolgreich erstellt hast:

→ Weiter mit: [NiklasCFW_Pack einrichten](Guide3)
