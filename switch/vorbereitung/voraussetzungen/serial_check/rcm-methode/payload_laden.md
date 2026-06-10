---
icon: upload
label: "Payload laden"
order: 300
---

# Payload laden (Hekate)

Wenn deine Switch bereits im **RCM** ist, kannst du jetzt den Payload ([`hekate.bin`](https://github.com/CTCaer/hekate/releases)) senden.

!!!warning Vorher prüfen
- Die Switch muss wirklich im RCM sein (schwarzer Bildschirm, kein Nintendo-Logo).
- Nutze ein funktionierendes USB-Datenkabel.
!!!

---

## Anleitung nach System

+++ Windows
### Benötigt
- **[TegraRcmGUI](https://github.com/eliboa/TegraRcmGUI/releases)**
- **USB-C-Datenkabel**

### Schritte
1. TegraRcmGUI starten.
2. Switch im RCM-Modus per USB verbinden.
3. **hekate** auswählen.
4. **Inject Payload** klicken.

![|460x276](/images/switch/vorbereitung/rcm/tegrarcmgui-windows.png)

### Wenn es nicht klappt
- Zeigt TegraRcmGUI `0x7000`, ist die Konsole in der Regel ungepatcht.
- Zeigt TegraRcmGUI `0x0000`, ist die Konsole gepatcht (RCM-Exploit nicht nutzbar).
- Anderen USB-Port bzw. anderes Datenkabel testen.

+++ macOS
### Option A: CrystalRCM (empfohlen)
1. CrystalRCM über die Releases laden: [CrystalRCM Releases](https://github.com/prayerie/CrystalRCM/releases)
2. `.dmg` öffnen und `CrystalRCM.app` in einen lokalen Ordner kopieren.
3. CrystalRCM starten und [`hekate.bin`](https://github.com/CTCaer/hekate/releases) auswählen.
4. Switch im RCM-Modus verbinden und prüfen, ob sie erkannt wird.
5. **Push!** klicken.

![|700x420](/images/switch/vorbereitung/rcm/crystalrcm3.png)

!!!info macOS Hinweis
Wenn macOS das Starten blockiert, öffne die App über Rechtsklick mit **Öffnen** und bestätige den Dialog.<br>
Bei **Sequoia und neuer**: [Unsigned Apps auf macOS öffnen](macos_unsigned_apps).
!!!

### Option B: WebRCM
1. Kompatiblen Browser öffnen (Chrome/Edge/Opera/Samsung Internet/QQ Browser).
2. [rcm.niklascfw.de](https://rcm.niklascfw.de) öffnen.
3. Hekate auswählen und senden.

![|700x420](/images/switch/allgemein/payload_macos.png)

### Hinweis
macOS erstellt teils versteckte Dateien wie `.DS_Store` und `._Dateiname`. Diese sollten nicht auf der CFW-SD landen.

+++ Linux / Android / ChromeOS
### WebRCM
1. Switch im RCM verbinden.
2. [rcm.niklascfw.de](https://rcm.niklascfw.de) im kompatiblen Browser öffnen.
3. Hekate auswählen und senden.

![|700x420](/images/switch/allgemein/payload_macos.png)

### Linux (USB-Rechte)
Falls Zugriffsfehler auftreten, `udev`-Regel setzen:

```bash
SUBSYSTEM=="usb", ATTR{idVendor}=="0955", MODE="0664", GROUP="plugdev"
```

Danach System neu starten.
+++

---

## Nach dem Payload

!!!success Nächster Schritt
Wenn Hekate gestartet ist, geht es weiter mit dem **[Start: Roter Faden](../../../roter_faden)** oder direkt mit der **[OmniNX Einführung](../../../einfuehrung)**.
!!!
