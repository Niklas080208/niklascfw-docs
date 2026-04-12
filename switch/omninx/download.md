# OmniNX Herunterladen

## Download & Entpacken

### OmniNX-Pack herunterladen

1. Gehe zu den **OmniNX Releases**:  
   **[git.niklascfw.de/OmniNX/OmniNX/releases](https://git.niklascfw.de/OmniNX/OmniNX/releases)**
2. Lade die gewünschte **Variante** herunter:
   - **OmniNX Light** (minimal)
   - **OmniNX Standard** (voll)
   - **OmniNX OC** (voll, plus Overclocking)

   Unsicher? Schaue in die App-Tabelle → [Varianten im Überblick](einfuehrung#varianten-im-überblick).

![OmniNX Releases](/images/switch/omninx/download-install/omninx-releases.png)

### OmniNX-Pack entpacken

1. Entpacke die heruntergeladene **ZIP-Datei** (z. B. mit [WinRAR](https://www.win-rar.com/), [7-Zip](https://www.7-zip.org/) oder den eingebauten Archiv-Tools deines Systems).
2. Im entpackten Ordner solltest du nun diverse Ordner und Dateien sehen: z. B. **OmniNX Standard** (oder Light/OC) sowie die für den Bootloader benötigten Dinge der Staging Area. **Siehe folgende Abbildung:**

![OmniNX Entpacken](/images/switch/omninx/download-install/extract-omninx.gif)

---

## Auf SD-Karte kopieren

Das entpackte Pack muss auf die **SD-Karte** der Switch. **Zwei Wege:** per [**SD-Kartenleser am PC**](#option-a-über-sd-kartenleser-pc) oder per [**USB**](#option-b-über-usb-switch-mit-hekate) mit der Switch (Hekate).

### Option A: Über SD-Kartenleser (PC)

>>> SD-Karte vorbereiten
**Switch ausschalten.** Danach **SD-Karte** aus der Switch entfernen und in den **SD-Kartenleser** am PC stecken.
>>> Dateien kopieren
Die Inhalte des entpackten Ordners in das Stammverzeichnis (Root) der SD-Karte kopieren.
![OmniNX auf microSD kopieren](/images/switch/omninx/download-install/copy-omninx.gif)
!!!tip Beim Kopieren
Wirst du gefragt, ob **bestehende Dateien ersetzt** oder **überschrieben** werden sollen, bestätige mit **Ja** bzw. **Ersetzen**, damit das Pack korrekt auf die SD-Karte kommt.
!!!
>>> SD sicher auswerfen
SD-Karte sicher auswerfen und zurück in die Switch legen.
>>>

### Option B: Über USB (Switch mit Hekate)

>>> Hekate & USB
**Hekate** starten (Payload injizieren oder von SD booten). Falls du im **Launch-Menü** landest, oben rechts auf **Close** tippen. Gehe zu **Tools** → **USB Tools** → **SD Card**. Switch per **USB-Kabel** mit dem PC verbinden.

![Hekate Tools](/images/switch/omninx/download-install/hekate-tools.png)
![USB Tools SD Card](/images/switch/omninx/download-install/hekate-tools-usb.png)
>>> Am PC: Dateien kopieren
Am PC erscheint das Laufwerk der SD-Karte. Alle Inhalte der entpackten .zip Datei auf das Stammverzeichnis der microSD Karte ziehen.
![OmniNX auf microSD kopieren](/images/switch/omninx/download-install/copy-omninx.gif)
!!!tip Beim Kopieren
Auch hier wieder, wenn du gefragt wirst ob **bestehende Dateien ersetzt** oder **überschrieben** werden sollen, bestätige mit **Ja** bzw. **Ersetzen**, damit das Pack korrekt auf die SD-Karte kommt.
!!!
>>> USB trennen
**USB trennen** (sicher auswerfen). In Hekate ggf. **Close**.
>>>

!!!success Nächster Schritt
**[Installation](installation_omninx)** – Installer-Payload starten und Anweisungen folgen.
!!!
