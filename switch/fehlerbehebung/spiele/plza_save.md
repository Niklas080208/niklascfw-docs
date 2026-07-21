---
icon: tools
label: "Legenden Z-A Spielstand reparieren"
order: 150
description: "Defekten Savegame-Stand von Legenden Z-A mit plza-recovery reparieren."
---

# Defekten Legenden Z-A Spielstand reparieren

!!!warning Voraussetzung
Du brauchst eine **gemoddete Switch** und auf dem PC muss **[Python 3.x](https://www.python.org/downloads/)** installiert sein.
!!!

[!button variant="secondary" text="plza-recovery herunterladen" icon="download" target="blank" corners="pill"](https://github.com/azalea-w/plza-recovery/releases/tag/v1.2.2)

---

## Savegame reparieren

>>> Tool herunterladen
Lade **plza-recovery** von GitHub herunter und entpacke es in einen neuen Ordner.

>>> Savegame hinzufügen
Füge deine Save-Datei `main` zu den entpackten Dateien hinzu.

>>> Ordner in CMD öffnen
Öffne den entpackten Ordner, klicke in die **Adresszeile** und gib Folgendes ein:

```text
cmd
```

Danach **Enter** drücken.

>>> Reparatur ausführen
Führe im geöffneten Fenster folgenden Befehl aus:

```text
python main.py main
```

>>> Ergebnisdatei umbenennen
Nach dem Ausführen entsteht eine Datei namens `main_modified`. Benenne sie um in:

```text
main
```

>>> Savegame auf die SD kopieren
Kopiere die neue `main` nach:

```text
/switch/JKSV/[Spiel]/Checkpoint/
```

Die alte Datei vorher löschen oder ersetzen.

>>> In JKSV wiederherstellen
Starte **JKSV** auf der Switch und führe für das Spiel **Restore** aus.


