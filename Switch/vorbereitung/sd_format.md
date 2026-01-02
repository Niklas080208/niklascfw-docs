# SD auf FAT32 formatieren

In dieser Anleitung findest du **drei verschiedene Methoden**, um deine SD-Karte auf **FAT32** zu formatieren.  
Bitte lies dir alle Punkte aufmerksam durch und wähle die Methode, die für dich am besten passt.

---

## ⚠️ Voraussetzungen

<div style="background-color: #fff3cd; border-left: 4px solid #ffc107; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<h4 style="color: #856404; margin-top: 0;">⚠️ Wichtig</h4>
<ul style="color: #212529; margin-bottom: 0;">
<li>Ein <strong>SD-Kartenleser</strong> ist erforderlich!</li>
<li>Sichere alle wichtigen Daten vorher, da beim Formatieren <strong>alles gelöscht</strong> wird!</li>
</ul>
</div>

---

## 🧰 Option 1: Mit Rufus

### Schritt 1: Rufus herunterladen

Lade **Rufus** herunter: [https://rufus.ie/de/](https://rufus.ie/de/)

### Schritt 2: Formatierung durchführen

1. Öffne Rufus und stelle alles so ein wie in den Beispielbild.

**Aktiviere bei **1TB SD-Karten** den **Haken für USB-Festplatten**.**

![|700x420](/images/sdcard/Rufus.png)


2. Wähle deinen **SD-Datenträger** oben in der Liste aus.  
   *Achtung: Der Name kann bei jedem unterschiedlich sein!*

3. Erweiterte Laufwerkseigenschaften einblenden

4. Klicke auf **Start**, um die Formatierung zu beginnen.

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>💡 <strong>Tipp:</strong> Rufus löscht beim Formatieren alle Partitionen! </small></p>
</div>

---

## ⚙️ Option 2: Über Hekate (Switch)

### Schritt 1: Hekate starten


1. Entnehme den **bootloader Ordner** und die **payload-Datei** aus deinem Pack.
2. Starte die Switch in **Hekate**.

![|700x420](/images/sdcard/Hekate_Format1.jpg)


### Schritt 2: SD-Karte formatieren

1. Gehe zu: **Tools** → **Partition SD-Karten**
2. Wenn du bereits eine **emuMMC-Partition** auf der SD hast, kannst du sie gleich hier erstellen.
3. Klicke auf **Next Step** Hekate erstellt dann automatisch aus deiner **exFAT SD** eine **FAT32 SD**.


![|700x420](/images/sdcard/Hekate_Format2.jpg)




<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>💡 <strong>Hinweis:</strong> Bei dem Bild handelt es sich nur um eine Beispiel Formatierung. Man könnte auch ohne auswahl über Next Step auf FAT32 formatieren. </small></p>
</div>

---

## 💻 Option 3: Mit GUIFormat

1. Lade das Tool **GUIFormat** herunter.
2. Wähle deine SD-Karte im Tool aus. **Hierbei ist zu beachten das du den richtigen Laufwerksbuchstaben erwischst, denn das Tool erkennt auch Festplatten!**
3. Stelle sicher, dass als **Dateisystem FAT32** ausgewählt ist. Und die vorgebenenen Parameter zu nutzen. 
4. Klicke auf **Start**, um die Formatierung zu starten. Geht nur wenn alle Fenster die mit Windows Explorer zu tun haben geschlossen wurden. 

![|500x320](/images/sdcard/AlleFensterSchliessen.png)



Fertig – deine SD-Karte ist jetzt im **FAT32-Format**!

![|420x700](/images/sdcard/guiformat.png)

---

## ✅ Zusammenfassung

| Methode | Plattform | Besonderheit |
|---------|-----------|--------------|
| **Rufus** | Windows | Einfache GUI, ideal für große Karten |
| **Hekate** | Nintendo Switch | Direktes FAT32-Formatieren aus Hekate |
| **GUIFormat** | Windows | Nur zur Not Verwenden |

---

<div style="background-color: #e7f3ff; border-left: 4px solid #2196F3; padding: 1rem; margin: 1rem 0; border-radius: 4px;">
<p style="color: #212529; margin: 0;"><small>ℹ️ <strong>Hinweis:</strong> Nach der Formatierung kannst du deine Daten (z. B. CFW-Dateien, emuMMC, etc.) wieder auf die Karte kopieren.</small></p>
</div>
