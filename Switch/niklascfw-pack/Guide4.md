# NiklasCFW_Pack und Firmware updaten

---

## ⚠️ Voraussetzungen

<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">⚠️ Wichtig</h4>
<p style="color: #212529; margin-bottom: 0;"><strong>Bitte darauf achten, dass deine Uhrzeit synchronisiert ist.</strong></p>
<p style="color: #212529; margin-bottom: 0;">Ansonsten funktioniert der Download über UltraHand nicht!</p>
</div>

---

## 🔄 CFW Pack aktualisieren

### Schritt 1: Vorbereitung

1. Starte die Switch in die **CFW**
2. Aktiviere die **Internet-Verbindung** in den Einstellungen der Switch
3. Deaktiviere den **Flugzeugmodus**

### Schritt 2: UltraHand öffnen

1. Öffne **UltraHand**  
   *Vom linken Bildschirmrand nach rechts wischen oder **L + R + Plus** gleichzeitig drücken*

![|700x420](/images/Guide4/Bild1.jpg)

### Schritt 3: Update-Checker verwenden

1. Gehe zu **NiklasCFW Downloader** → **Update_Checker**
2. **3x klicken** für ✔️
3. Wähle **NiklasCFW_Pack x.x.x** aus (*x steht für Platzhalter der Versionsnummer*)
4. Gehe zu **NiklasCFW Downloader**

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>ℹ️ <strong>Wichtig:</strong> Im Anschluss aus dem Niklas CFW Downloader raus und wieder rein. Damit er neu Laden kann!</small></p>
</div>

![|700x420](/images/Guide4/Bild2.jpg)
![|700x420](/images/Guide4/Bild3.jpg)

### Schritt 4: CFW Pack herunterladen

1. Nach dem **Download** gehe zurück zu den **Paketen**
2. Wähle **NiklasCFW Downloader** aus

![|700x420](/images/Guide4/Bild3.jpg)

3. Gehe zu **CFW_Pack** und wähle **NiklasCFW_Pack x.x.x** aus  
   *Auch hier steht x als Platzhalter für die Versionsnummer*

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>ℹ️ Der <strong>Fortschrittsbalken</strong> läuft <strong>2x</strong> durch, da er erst <strong>downloadet</strong> und anschließend das <strong>CFW_Pack entpackt</strong>.</small></p>
</div>

![|700x420](/images/Guide4/Bild5.jpg)
![|700x420](/images/Guide4/Bild6.jpg)

### Schritt 5: Update Script ausführen

1. Wenn das **CFW_Pack** erfolgreich geladen wurde, gehe zurück zu den **Paketen**
2. Wähle **RebootNX** → **Boot Optionen** oder **Payloads** → **Tegra Explorer**
3. Falls du im **Hekate** landest, wähle dort nochmal **Tegra Explorer** aus

![|700x420](/images/Guide4/Bild7.jpg)
![|700x420](/images/Guide4/Bild8.jpg)

4. In **Tegra Explorer**:
   - Falls eine Meldung erscheint, drücke diese weg
   - Navigiere zu den **Scripts** (ganz unten)
   - Du findest **zwei Update-Scripts**:

![|700x420](/images/Guide4/Bild9.jpg)

>⚠️ Achtung nur kleiner als 1.4.1
<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">📋 Welches Script soll ich wählen?</h4>
<p style="color: #212529; margin-bottom: 0.5rem;"><strong>🟢 Clean Script (Empfohlen):</strong></p>
<ul style="color: #212529; margin-bottom: 0.5rem;">
<li>Entfernt alte Apps und Mods, die mit der neuen Atmosphere-Version nicht kompatibel sind</li>
<li>Verhindert Abstürze und Probleme</li>
<li>Deine Spiele und Spielstände bleiben erhalten</li>
</ul>
<p style="color: #212529; margin-bottom: 0.5rem;"><strong>🟡 Dirty Script:</strong></p>
<ul style="color: #212529; margin-bottom: 0;">
<li>Behält alle alten Apps und Mods</li>
<li>Kann zu Abstürzen führen, da alte Apps nicht mit der neuen Atmosphere funktionieren</li>
<li>Nur verwenden, wenn du genau weißt, was du tust</li>
</ul>
</div>

5. Wähle **1.NiklasCFW - Update Script.te (Clean)** aus  
   *Das Clean Script wird empfohlen, da es Probleme vermeidet*

   **Bei größer 1.4.1 Wähle Wähle ganz unten NiklasCFW - Install Skript.te aus**

6. Das **Update Script** zeigt dir die Details an:
   - Lies die Informationen auf dem Bildschirm
   - Drücke **A** (oder **Power** bei Switch Lite) um die Installation zu starten
   - Zum Abbrechen drücke **B** oder eine **Lautstärke-Taste**

![|700x420](/images/Guide4/Bild10.jpg)

7. Das Script führt automatisch folgende Schritte aus:
   - Entfernt alte CFW-Komponenten
   - Installiert das neue **NiklasCFW_Pack**
   - Bereinigt das System
   - Nach erfolgreicher Installation, drücke **A**  um zu **Hekate** zu gelangen

![|700x420](/images/Guide4/Bild11.png)

8. Nach dem **Reboot** zu **Hekate** kannst du deine **CFW** wieder starten

### Schritt 6: Update prüfen

Im **Hekate** oder beim **Booten der CFW** kannst du anhand der **Versionsnummer** erkennen, ob du auf **der neuen Version** bist.

![|700x420](/images/Guide4/Bild9.jpg)
![|700x420](/images/Guide4/Bild10.jpg)

---

## 📱 Firmware der CFW updaten

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #1565C0; margin-top: 0;">ℹ️ Hinweis</h4>
<p style="color: #212529; margin-bottom: 0;">Es ist <strong>nicht immer notwendig</strong>, in der CFW die <strong>aktuellste Firmware</strong> zu haben.</p>
<p style="color: #212529; margin-bottom: 0;">Frühestens, wenn ein <strong>Spiel</strong> nach einem <strong>Firmware-Update</strong> verlangt, würde ich eine Aktualisierung durchführen. Es schadet in der Regel aber nicht zu aktualisieren.</p>
<p style="color: #212529; margin-bottom: 0;"><strong>Sollte man eine Firmware nicht aktualisieren sollen, werden wir das bekannt geben.</strong></p>
</div>

### Schritt 1: Firmware herunterladen

Der Download der **Firmware** funktioniert genauso wie beim **Update des CFW_Packs**:

1. **UltraHand öffnen** → **NiklasCFW Downloader** → **Update_Checker**
2. Wähle **NiklasCFW_Pack x.x.x** aus (*x steht für Platzhalter der Versionsnummer*)
3. Gehe zu **NiklasCFW Downloader**

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>ℹ️ <strong>Wichtig:</strong> Im Anschluss aus dem Niklas CFW Downloader raus und wieder rein. Damit UltraHand neu Laden kann!</small></p>
</div>

4. Dann wieder **NiklasCFW Downloader** → **Firmware** → **Firmware xx.x.x** auswählen

![|700x420](/images/Guide4/Bild12.jpg)
![|700x420](/images/Guide4/Bild13.jpg)

### Schritt 2: Firmware installieren

1. Wenn der **Download** beendet ist, schließe **UltraHand**
2. Starte **Sphaira**
3. Wir benötigen nun **Daybreak**

![|700x420](/images/Guide4/Bild14.jpg)

4. In **Daybreak** wähle **Install** aus

![|700x420](/images/Guide4/Bild15.png)

5. Wähle das **Firmware-Verzeichnis** aus (z.B. **Firmware.21.0.1**)

![|700x420](/images/Guide4/Bild16.png)

6. **Daybreak** validiert die Firmware automatisch:
   - Die Firmware-Version wird angezeigt
   - **exFAT-Unterstützung** wird geprüft
   - Nach erfolgreicher Validierung erscheint **"Update is valid!"**

![|700x420](/images/Guide4/Bild17.png)

7. Wähle **Continue** und dann **Preserve Settings** aus  
   *Dies behält deine aktuellen Einstellungen bei*

![|700x420](/images/Guide4/Bild18.png)

8. Wähle **Install (FAT32 + exFAT)** aus  
   *Dies installiert die Treiber für beide Dateisysteme*

![|700x420](/images/Guide4/Bild19.png)

9. Bestätige die Installation mit **Continue**  
   *Die Meldung "Ready to begin update installation" erscheint*

![|700x420](/images/Guide4/Bild20.png)

10. Die Installation startet automatisch:
    - Der Fortschrittsbalken zeigt den Installationsstatus
    - Nach **100%** ist die Installation abgeschlossen
    - Wähle **Reboot** um die Switch neu zu starten

![|700x420](/images/Guide4/Bild21.png)

11. Nach dem **Neustart** sollte die neue **Firmware** installiert sein

---

## ✅ Fertig

Das Update sollte erfolgreich abgeschlossen sein!



