# Vom NiklasCFW Pack zu OmniNX

Das **NiklasCFW Pack** ist **eingestellt** und erhält **keinen Support** mehr. **OmniNX** ist der Nachfolger. Diese Anleitung zeigt, wie du **auf der Konsole** per **Ultrahand** und **NiklasCFW Downloader** wechselst, **ohne einen PC**. Das Pack wird auf die SD-Karte geladen; danach installierst du es wie bei einer normalen OmniNX-Installation.

---

## Voraussetzungen
- **NiklasCFW Pack** ist installiert und die Switch startet in die CFW (emuMMC).
- **WLAN** ist verbunden (Download dauert je nach Verbindung mehrere Minuten).
- **Ausreichend freier Speicher** auf der SD-Karte für das OmniNX-ZIP und die entpackten Dateien.
- Die **Systemzeit** muss synchronisiert sein, damit der Download erfolgreich abschließt:<br>
[!ref](nachher/dbi_time)

---

## OmniNX herunterladen (Ultrahand)

>>> Ultrahand öffnen
**Ultrahand** öffnen (**L** + **R** + **Plus**, oder im Handheld von links nach rechts wischen).<br>
Wähle nun den **NiklasCFW Downloader**.

![Ultrahand – Pakete](/images/switch/omninx/migrate/ultrahand-pakete.jpeg)
>>> Updater aktuallisieren
Öffne nun den **Update_Checker** und klicke dich bis zum Update Eintrag.

![NiklasCFW Downloader – Update_Checker](/images/switch/omninx/migrate/downloader-update-checker.jpeg)
![NiklasCFW Downloader – Updater aktuallisieren](/images/switch/omninx/migrate/update-checker-version.jpeg)

>>> Ultrahand-Pakete neu laden
Zurück zum **Ultrahand-Hauptmenü** (**B**) und das Paket **Ultrahand Reload** ausführen. Die Paketliste sieht danach **genauso aus** wie zuvor (siehe Schritt 1) – wichtig ist nur der Reload.

![Ultrahand – Pakete](/images/switch/omninx/migrate/ultrahand-pakete.jpeg)

>>> NiklasCFW Downloader erneut öffnen
**NiklasCFW Downloader** noch einmal starten. Jetzt erscheint der Bereich **„Auf OmniNX wechseln“** statt eines neuen NiklasCFW-Pack-Updates.

![Auf OmniNX wechseln](/images/switch/omninx/migrate/omninx-wechseln.jpeg)

Im **Hinweis** steht, dass das NiklasCFW Pack ausläuft und OmniNX der Nachfolger ist. Weitere Infos gibt es auf dem **NiklasCFW YouTube-Kanal** und im **Discord**.

>>> OmniNX herunterladen
**OmniNX** auswählen (Anzeige **neuste**) und mit **A** bestätigen. Den Download **vollständig abwarten** (Fortschrittsbalken bis 100 %).

![OmniNX – Download](/images/switch/omninx/migrate/omninx-download.jpeg)
![OmniNX Download fertig](/images/switch/omninx/migrate/omninx-auswahl.jpeg)

!!!info Download und Upload
Ein Vorgang läuft **zweimal** ab: Zuerst wird die Datei (z. B. .zip) **heruntergeladen**, danach auf die SD-Karte **hochgeladen**. Beide Phasen müssen durchlaufen werden.

![Download-Phase](/images/switch/omninx/updates/pack/ultrahand-download.png)
![Upload-Phase](/images/switch/omninx/updates/pack/ultrahand-upload.png)
!!!
>>>

---

## Neustart in Hekate (RebootNX)

>>> Zurück zu Ultrahand → RebootNX
Nach dem Download zurück zum **Ultrahand-Hauptmenü** (Pakete) und **RebootNX** auswählen.

[![RebootNX in Ultrahand](/images/switch/omninx/migrate/ultrahand-rebootnx.jpeg)](/images/switch/omninx/migrate/ultrahand-rebootnx.jpeg)
>>> In RebootNX: Hekate starten
Unter **System** **Hekate** wählen und mit **A** bestätigen.

[![RebootNX – Hekate](/images/switch/omninx/migrate/rebootnx-hekate.jpeg)](/images/switch/omninx/migrate/rebootnx-hekate.jpeg)
>>>

## Installation abschließen

Das OmniNX-Pack liegt nun auf der SD-Karte. Ab hier gilt die **normale Installationsanleitung** ab dem Schritt "**Installation durchführen**":

[!ref](vorbereitung/installation_omninx#installation-durchführen)

Dort startest du den **OmniNX Installer** aus dem Hekate Launch-Menü, bestätigst Modus und Variante und wartest den Kopiervorgang ab. Anschließend folgst du den Hinweisen zu **emuMMC**, **Pack einrichten** usw.

---

!!!success Migration abgeschlossen
Sobald der Installer **„Erfolgreich“** meldet und du CFW/emuMMC wie gewohnt startest, ist der Wechsel vom **NiklasCFW Pack** zu **OmniNX** erledigt. Bei Problemen: [Fehlerbehebung](/switch/fehlerbehebung/system-boot/hekate_fix_archive_bits).
!!!
