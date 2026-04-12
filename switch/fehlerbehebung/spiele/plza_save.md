# Defekten Legenden Z-A Spielstand reparieren

> ⚠️ **Voraussetzung:**  
Man benötigt eine gemoddete Switch und auf dem PC muss [Python 3.x](https://www.python.org/downloads/) installiert sein

---

## 🧩 Schritte

### 1. Programm herunterladen
Lade das Tool von GitHub herunter und entpacke es in einen neuen Ordner (Name beliebig):

🔗 [plza-recovery v1.2.2 – GitHub Release](https://github.com/azalea-w/plza-recovery/releases/tag/v1.2.2)

---

### 2. Savegame hinzufügen
Füge deine Savefile (`main`) zu den entpackten Dateien hinzu.

---

### 3. Ordner öffnen
Öffne den entpackten Ordner, klicke in die **Adresszeile** und tippe:

```
cmd
```

Dann **Enter** drücken.

---

### 4. Befehl ausführen
Im geöffneten CMD-Fenster folgenden Befehl eingeben:

```
python main.py main
```

---

### 5. Ergebnisdatei umbenennen
Nach dem Ausführen erscheint eine neue Datei namens `main_modified`.  
Benenne sie um in:

```
main
```

---

### 6. Savegame auf die SD-Karte kopieren
Kopiere die neue `main` in:

```
/switch/JKSV/[Spiel]/Checkpoint/
```

(Die alte Datei vorher löschen!)

---

### 7. Wiederherstellen in JKSV
Starte **JKSV** auf deiner Switch und führe **Restore** für dein Spiel aus.
