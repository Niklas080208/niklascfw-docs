# Firmware updaten

Hier geht es um das **Aktualisieren** der **Switch-Firmware** (Horizon OS) in der CFW/emuMMC mit **Daybreak**.

!!!danger Themes vorher deinstallieren
Installierte **Custom Themes müssen vor dem Firmware-Update zwingend deinstalliert** werden. Sonst stößt du nach dem Update oft auf einen Fehler (typisch: **0100000000000001000**).
!!!

[!ref text="Custom Theme Fehler beheben"](/switch/fehlerbehebung/theme-visual/0100000000000001000_beheben_(custom_theme))

---

## Voraussetzungen

!!!warning Uhrzeit
Die **Uhrzeit** sollte synchronisiert sein (z. B. für Downloads). Anleitung: [Einrichtung](/switch/vorbereitung/pack_einrichten/#systemzeit-synchronisieren).
!!!

---

## Firmware der CFW (emuMMC) updaten

!!!info Firmware-Update
Die **neueste Firmware** ist nicht immer nötig. Spätestens wenn ein **Spiel** ein Update verlangt, kannst du aktualisieren. Sollte eine Firmware nicht empfohlen sein, wird das bekannt gegeben.
!!!

### Firmware herunterladen (UltraHand / OmniNX Updater)

>>> UltraHand öffnen
**UltraHand** öffnen (**L** + **R** + **Plus**).

![UltraHand – Home](/images/switch/omninx/updates/pack/ultrahand-home.jpg)
>>> OmniNX Downloader starten
**OmniNX Downloader** in der Paketliste auswählen (**A**).

![OmniNX Downloader auswählen](/images/switch/omninx/updates/pack/ultrahand-home-downloader.jpg)
>>> OmniNX Updater → Firmware herunterladen
**OmniNX Updater** auswählen, darin die **Firmware**-Option (z. B. gewünschte Version) wählen und warten, bis der Download abgeschlossen ist.

![UltraHand – OmniNX Downloader](/images/switch/omninx/updates/pack/omninx-downloader.jpg)
![OmniNX Downloader – Firmware Download](/images/switch/omninx/updates/firmware/omninx-updater-firmware.jpg)
>>>

---

### Firmware installieren (Daybreak)

1. **UltraHand** schließen, **Sphaira** starten.
2. **Daybreak** öffnen.

![Daybreak](/images/switch/omninx/updates/firmware/daybreak-start.jpg)

3. **Install** wählen.
4. **Firmware-Verzeichnis** wählen (z. B. **Firmware.21.0.1**).

![Firmware-Verzeichnis wählen](/images/switch/omninx/updates/firmware/daybreak-fw-select.jpg)

5. Daybreak prüft die Firmware (**Update is valid!**).
6. **Continue** → **Preserve Settings**.
7. **Install (FAT32 + exFAT)** wählen.
8. **Continue** bestätigen (**Ready to begin update installation**).
9. Installation abwarten (100 %), dann **Reboot**.

![Daybreak – Install](/images/switch/omninx/updates/firmware/daybreak-check-continue.jpg)
![Preserve Settings](/images/switch/omninx/updates/firmware/daybreak-preserve.jpg)
![Install FAT32 + exFAT](/images/switch/omninx/updates/firmware/daybreak-exfat.jpg)
![Firmware Update](/images/switch/omninx/updates/firmware/daybreak-continue.jpg)
![Reboot](/images/switch/omninx/updates/firmware/daybreak-install-finished.jpg)

10. Nach dem Neustart ist die neue Firmware aktiv.

---

## Experimentell: Firmware-Prüfung deaktivieren

!!!warning Nur wenn Daybreak blockiert
Wenn du beim Installieren die Meldung **„Nicht unterstützte Firmware-Version“** siehst, ist die gewählte Firmware **neuer als dein aktuelles Atmosphere** offiziell unterstützt. **Normalerweise:** erst **OmniNX / Atmosphere aktualisieren**, dann die Firmware installieren.

In **neueren OmniNX-Versionen** kann man die Daybreak Prüfung **experimentell** abschalten – nur wenn du die Firmware **trotzdem** installieren willst und weißt, dass du danach ggf. **Atmosphere nachziehen** musst.
!!!

>>> Wann tritt das auf?
Beim Schritt **Installieren** bricht Daybreak ab und zeigt z. B. **Maximal unterstützte Firmware ist 23.0.0** – obwohl die Firmware-Dateien schon auf der SD liegen.

![Daybreak – Firmware blockiert|700x420](/images/switch/omninx/updates/firmware/daybreak-experimental/daybreak-firmware-blockiert.jpg)

>>> Einstellungen in Daybreak
Zurück ins **Daybreak-Hauptmenü**. Wähle **Einstellungen** (neben Installieren und Beenden).

![Daybreak – Einstellungen|700x420](/images/switch/omninx/updates/firmware/daybreak-experimental/daybreak-firmware-pruefung-aus.jpg)

>>> Firmware-Prüfung ausschalten
Tippe auf **Firmware-Prüfung**, bis der Schalter **aus** ist. Unten steht dann z. B. **Auch Firmware > 23.0.0**. Mit **Zurück** ins Hauptmenü.

![Daybreak – Firmware-Prüfung aus|700x420](/images/switch/omninx/updates/firmware/daybreak-experimental/daybreak-einstellungen-menu.jpg)

>>> Erneut installieren
Wieder **Installieren** wählen und die Anleitung oben ab **Firmware-Verzeichnis wählen** fortsetzen.
>>>

!!!danger Auf eigenes Risiko
Ohne Prüfung kann die Installation **klappen oder Probleme machen**, wenn Atmosphere die Firmware noch nicht sauber unterstützt. Nach dem Update [OmniNX aktualisieren](/switch/updates/omninx-update). Die Prüfung danach wieder **ein** lassen, wenn du sie nicht dauerhaft brauchst.
!!!

---

!!!success Fertig
Firmware-Update ist abgeschlossen. Bei Problemen: [Fehlerbehebung](/switch/fehlerbehebung/system-boot/hekate_fix_archive_bits).
!!!
