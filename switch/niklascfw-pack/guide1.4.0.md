# Ersteinrichtung

---

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #1565C0; margin-top: 0;">ℹ️ Wichtiger Hinweis</h4>
<p style="color: #212529; margin-bottom: 0;"> <strong>Der emuMMC bleibt unberührt</strong>. Das heißt, dass Spielstände, Spiele und Einstellungen (sofern vorhanden) erhalten bleiben. 

**Anders gesagt solange ihr nicht an irgendeinem schritt Formatieren drück bleibt alles bestehen. Löscht die Ordner wie auf den Beispielbildern. Macht Packups von Thorparty App Ordnern**</p>
</div>

## ✅ Voraussetzungen

- **FAT32 formatierte** SD-Karte > Habt ihr in den meisten Fällen schon.
- **prod.keys** sollten vor der Installation mit **LockPick_RCM** gedumpt werden (falls noch nicht vorhanden)

---

## 📥 Download und Installation

### Schritt 1: Pack herunterladen

1. Lade das **aktuelle Release** herunter:  
   → [NiklasCFW_Pack](https://github.com/Woody-NX/NiklasCFW_Pack/releases/)

![|700x420](/images/switch/niklascfw-pack/guide1/1.5.0_1.png)
![|700x420](/images/switch/niklascfw-pack/guide1/1.5.0_2.png)

### Schritt 2: Pack entpacken

1. Entpacke die heruntergeladene Datei.

### ℹ️ Wichtiger Hinweis

**Am besten mit WinRAR entpacken**, da es dabei seltener zu Fehlern kommt.

---

## 💾 CFW Pack auf SD-Karte kopieren

Es gibt **zwei Möglichkeiten**, das CFW Pack auf die SD-Karte zu kopieren:

> ℹ️ **Wichtiger Hinweis**  
> Die Optionen schließen sich natürlich gegenseitig aus.

### Option 1: Über SD-Kartenleser (PC)

1. Entferne die SD-Karte aus der Switch
2. Stecke sie in den SD-Kartenleser am PC
3. Kopiere die entpackten Dateien auf die SD-Karte

### Option 2: Über USB-Verbindung (Switch)

1. Starte **Hekate** (Bootloader)
2. Falls du im **Launch Menu** landest, klicke oben rechts auf **Close**

![|700x420](/images/switch/niklascfw-pack/guide1/bild9.jpg)

3. Gehe zu **Tools** → **USB Tools** → **SD Card**

![|700x420](/images/switch/niklascfw-pack/guide1/bild10.jpg)

4. Verbinde die Switch per **USB** mit dem PC

![|700x420](/images/switch/niklascfw-pack/guide1/bild11.jpg)
![|700x420](/images/switch/niklascfw-pack/guide1/bild12.jpg)

### Schritt 3: Dateien kopieren

1. **Hauptverzeichnis prüfen**:  
   Das Verzeichnis sollte entweder leer sein oder wie im Beispiel aussehen (je nachdem, ob du neu anfängst oder von einem anderen CFW Pack kommst).

2. **Altes CFW Pack entfernen (optional)**:  
   Falls gewünscht, lösche alles außer **emuMMC**, **JKSV** und **Nintendo**.

3. **Dateien kopieren**:  
   Kopiere die entpackten Dateien ins **Hauptverzeichnis** deiner SD-Karte.

![|700x420](/images/switch/niklascfw-pack/guide1/bild4.png)
![|700x420](/images/switch/niklascfw-pack/guide1/bild5.png)
![|700x420](/images/switch/niklascfw-pack/guide1/switchsdvorinstall.png)

4. **SD-Karte zurück in die Switch** einstecken oder **USB-Kabel** entfernen
5. **Hekate** erneut starten

---

## 🔄 Update Script ausführen

1. Im **Launch Menü** angekommen, wähle **Tegra Explorer** aus.
 Falls eine Meldung wegen keys erscheint, drücke diese weg, das kommt nach der Installation noch.

![|700x420](/images/switch/niklascfw-pack/guide1/TegraLaunch.bmp)

![|700x420](/images/switch/niklascfw-pack/guide1/vorminstall.bmp)

2. Wähle **NiklasCFW - Install Skript.te** aus

![|700x420](/images/switch/niklascfw-pack/guide1/Scriptwahl.bmp)

3. Folge den **Anweisungen** im nächsten Fenster

![|700x420](/images/switch/niklascfw-pack/guide1/Installbeendet.bmp)

4. Nach der Installation:
   - Drücke **A und für Switch Lite Power**
   - **Landest dann direkt in Hekate zum Launch**

---

## 🔑 prod.keys dumpen 💡Wegen der Key Warnmeldung Anfangs. 

<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">⚠️ Navigation</h4>
<p style="color: #212529; margin-bottom: 0;">Die Navigation funktioniert nur mit <strong>Lautstärke-Tasten</strong> und Bestätigung mit der <strong>Power-Taste</strong>.</p>
</div>

1. Starte **Hekate**
2. Gehe zu **Launch** → **Lockpick_RCM**

![|700x420](/images/switch/niklascfw-pack/guide1/Lockpickwählen.jpg)

3. Wähle **Dump from Sysnand** aus
4. Drücke die **Power-Taste** und wähle **Reboot to Hekate**

![|700x420](/images/switch/niklascfw-pack/guide1/bild14.png)

---

## ✅ Nächste Schritte

Das **CFW Pack** sollte nun fertig installiert sein!

- ✅ **Falls du bereits einen emuMMC hast**:  
  Du kannst nun unter **Launch** die **CFW** über **CFW-EmuMMC** starten.

- 📝 **Falls du noch keinen emuMMC hast**:  
  → Weiter mit: [emuMMC erstellen](guide2)

- ⚙️ **Falls du bereits einen emuMMC hast**:  
  → Weiter mit: [NiklasCFW_Pack einrichten](guide3)
