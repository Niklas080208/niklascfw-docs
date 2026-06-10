# SD auf FAT32 formatieren

In dieser Anleitung findest du drei Wege, um deine SD-Karte auf **FAT32** zu formatieren.

---

!!!warning Wichtig
- Beim Formatieren werden alle Daten auf der SD-Karte gelöscht.
- Sichere vorher alles, was du behalten willst.
- Ein SD-Kartenleser ist für PC-Methoden erforderlich.
!!!

---

## Option 1: Mit Rufus

>>> Rufus herunterladen
Lade Rufus hier herunter: [https://rufus.ie/de/](https://rufus.ie/de/)

>>> Einstellungen übernehmen
Öffne Rufus und übernimm die Einstellungen aus dem Beispielbild.

Bei **1 TB SD-Karten** aktiviere den Haken für **USB-Festplatten**.

![|560x336](/images/switch/vorbereitung/sd-karte/rufus.png)

>>> Laufwerk prüfen
Wähle den richtigen SD-Datenträger oben in der Liste aus.

!!!warning Achtung
Der Laufwerksname kann je nach System anders aussehen. Prüfe sorgfältig, dass es wirklich die SD-Karte ist.
!!!

>>> Formatierung starten
Blende die erweiterten Laufwerkseigenschaften ein und klicke auf **Start**.

!!!warning Hinweis
Rufus löscht beim Formatieren alle Partitionen.
!!!

>>>

---

## Option 2: Über Hekate (Switch)

>>> Hekate starten
Entnehme den **bootloader-Ordner** und die **payload-Datei** aus deinem Pack und starte die Switch in Hekate.

![|700x420](/images/switch/vorbereitung/sd-karte/hekate_format1.jpg)

>>> SD-Karte in Hekate formatieren
Gehe zu **Tools** → **Partition SD Card**.
Wenn du eine **emuMMC-Partition** planst, kannst du sie in diesem Schritt direkt mit anlegen.
Klicke auf **Next Step**. Hekate erstellt aus exFAT automatisch FAT32.

![|700x420](/images/switch/vorbereitung/sd-karte/hekate_format2.jpg)
!!!info Hinweis
Bei dem Bild handelt es sich nur um eine Beispiel-Formatierung. Du kannst auch ohne Auswahl direkt über **Next Step** auf FAT32 formatieren.
!!!

>>>

---

## Option 3: Mit GUIFormat

>>> GUIFormat starten
Lade **GUIFormat** herunter und starte das Tool.

>>> Laufwerk und Dateisystem setzen
Wähle die SD-Karte mit dem richtigen Laufwerksbuchstaben aus.
Setze als Dateisystem **FAT32** und nutze die vorgegebenen Parameter.

>>> Explorer-Fenster schließen
Schließe alle geöffneten Windows-Explorer-Fenster, die auf die SD-Karte zugreifen.

![|500x320](/images/switch/vorbereitung/sd-karte/allefensterschliessen.png)
>>> Formatierung starten
Klicke auf **Start** und warte bis der Vorgang abgeschlossen ist.

!!!success Fertig
Die SD-Karte ist jetzt im **FAT32-Format**.
!!!

![|420x700](/images/switch/vorbereitung/sd-karte/guiformat.png)

>>>

---

## Zusammenfassung

| Methode | Plattform | Besonderheit |
|---------|-----------|--------------|
| **Rufus** | Windows | Einfache GUI, ideal für große Karten |
| **Hekate** | Nintendo Switch | Direktes FAT32-Formatieren aus Hekate |
| **GUIFormat** | Windows | Fallback, wenn Rufus nicht genutzt wird |

---

!!!info Hinweis
Nach der Formatierung kannst du deine Daten (z. B. CFW-Dateien, emuMMC usw.) wieder auf die Karte kopieren.
!!!
