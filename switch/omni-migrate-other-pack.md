# Von einem anderen Pack zu OmniNX

Diese Anleitung ist für dich, wenn du **nicht** vom **NiklasCFW Pack** kommst, sondern von einem **beliebigen anderen CFW-Pack** auf **OmniNX** wechseln willst.

---

## Voraussetzungen

- Deine Switch startet bereits in eine **CFW / emuMMC**.
- Du hast Zugriff auf einen **PC**, um die microSD zu beschreiben.
- Genug freier Speicher auf der SD für OmniNX und die entpackten Dateien.

---

## OmniNX herunterladen und auf die SD kopieren

### Pack herunterladen

>>> OmniNX Releases öffnen
Gehe zu den **OmniNX Releases** und lade die gewünschte **Variante** herunter:

- **OmniNX Light** (minimal)
- **OmniNX Standard** (voll)
- **OmniNX OC** (voll, plus Overclocking)

Unsicher? Schaue in die App-Tabelle → [Varianten im Überblick](vorbereitung/einfuehrung#varianten-im-überblick).

[!button variant="secondary" text="OmniNX Releases (GitCFW)" icon="download" target="blank" corners="pill"](https://git.niklascfw.de/OmniNX/OmniNX/releases)

![OmniNX Releases](/images/switch/omninx/download-install/omninx-releases.png)

>>> Pack entpacken
Entpacke die heruntergeladene **ZIP-Datei** (z. B. mit [WinRAR](https://www.win-rar.com/), [7-Zip](https://www.7-zip.org/) oder den eingebauten Archiv-Tools deines Systems).

Im entpackten Ordner solltest du diverse Ordner und Dateien sehen: z. B. **OmniNX Standard** (oder Light/OC) sowie die für den Bootloader benötigten Dinge der Staging Area.

![OmniNX Entpacken](/images/switch/omninx/download-install/extract-omninx.gif)
>>>

---

### Auf die SD-Karte kopieren

Das entpackte Pack muss auf die **SD-Karte** der Switch. Bestehende Dateien bei Nachfrage **ersetzen / überschreiben**.

+++ Option A: SD-Kartenleser (PC)
>>> SD-Karte vorbereiten
**Switch ausschalten.** Danach **SD-Karte** aus der Switch entfernen und in den **SD-Kartenleser** am PC stecken.

>>> Dateien kopieren
Die Inhalte des entpackten Ordners in das **Stammverzeichnis (Root)** der SD-Karte kopieren.

![OmniNX auf microSD kopieren](/images/switch/omninx/download-install/copy-omninx.gif)

!!!tip Beim Kopieren
Wirst du gefragt, ob **bestehende Dateien ersetzt** oder **überschrieben** werden sollen, bestätige mit **Ja** bzw. **Ersetzen**, damit das Pack korrekt auf die SD-Karte kommt.
!!!

>>> SD sicher auswerfen
SD-Karte sicher auswerfen und zurück in die Switch legen.
>>>

+++ Option B: USB (Switch mit Hekate)
>>> Hekate & USB
**Hekate** starten (Payload injizieren oder von SD booten). Falls du im **Launch-Menü** landest, oben rechts auf **Close** tippen. Gehe zu **Tools** → **USB Tools** → **SD Card**. Switch per **USB-Kabel** mit dem PC verbinden.

![Hekate Tools](/images/switch/omninx/download-install/hekate-tools.png)
![USB Tools SD Card](/images/switch/omninx/download-install/hekate-tools-usb.png)

>>> Am PC: Dateien kopieren
Am PC erscheint das Laufwerk der SD-Karte. Alle Inhalte der entpackten ZIP auf das **Stammverzeichnis** der microSD ziehen.

![OmniNX auf microSD kopieren](/images/switch/omninx/download-install/copy-omninx.gif)

!!!tip Beim Kopieren
Auch hier: wenn du gefragt wirst, ob **bestehende Dateien ersetzt** oder **überschrieben** werden sollen, bestätige mit **Ja** bzw. **Ersetzen**.
!!!

>>> USB trennen
**USB trennen** (sicher auswerfen). In Hekate ggf. **Close**.
>>>
+++

---

## Installation abschließen

Das OmniNX-Pack liegt nun auf der SD-Karte. Ab hier gilt die **normale Installationsanleitung** ab dem Schritt "**Installation durchführen**":

[!ref](vorbereitung/installation_omninx#installation-durchführen)

Dort startest du den **OmniNX Installer** aus dem Hekate Launch-Menü, bestätigst Modus und Variante und wartest den Kopiervorgang ab. Anschließend folgst du den Hinweisen zu **emuMMC**, **Pack einrichten** usw.

---

!!!success Wechsel abgeschlossen
Sobald der Installer **„Erfolgreich“** meldet und du CFW/emuMMC wie gewohnt startest, bist du auf **OmniNX**. Bei Problemen: [Fehlerbehebung](/switch/vorbereitung/installation_omninx/troubleshooting.md).
!!!
