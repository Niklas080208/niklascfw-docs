# Nintendo Switch V1 – Softmod mit Hekate-Payload (Windows)

## Benötigt:
- **Nintendo Switch v1** (*unpatched*, Seriennummer prüfen)
- **microSD-Karte** (**FAT32 Pflicht**, 64–256 GB empfohlen)
- **RCM-Jig** (rechter Joy-Con-Schacht)
- **USB-C-Datenkabel**
- **Windows-PC**
- **`hekate.bin`** (aktueller Hekate-Payload)
- **TegraRcmGUI** (Payload-Tool für Windows)

---

## Vorbereitung am PC (TegraRcmGUI installieren)
1. **TegraRcmGUI** als **ZIP** herunterladen.
2. ZIP mit **[7‑Zip](https://www.7-zip.org/)** (kostenlos) **entpacken**.
3. Im entpackten Ordner **`TegraRcmGUI.exe`** starten.

> Tipp: In TegraRcmGUI kann man den Payload auch **per Doppelklick** senden – schneller als den „Inject“-Button zu suchen.

---

## RCM-Modus aktivieren (Switch)
1. Switch **ausschalten**.
2. **RCM-Jig** in den rechten Joy‑Con‑Schacht einsetzen.
3. **Lautstärke +** gedrückt halten.
4. **Power-Taste** kurz tippen → **Lautstärke +** weiter halten.
5. Bildschirm bleibt **schwarz** (kein Logo = RCM aktiv).

---

## Payload senden (Hekate)
1. Switch per **USB‑C** mit dem PC verbinden.
2. In **TegraRcmGUI** die Switch als **RCM-Gerät** erkennen lassen.
3. **`hekate.bin`** auswählen.
4. **Inject Payload** klicken **oder** die Payload-Datei **doppelklicken**.
5. Switch startet in **Hekate**.

### Wenn das Senden nicht klappt
- **TegraRcmGUI-Status prüfen:**  
  - Meldung **`Smashed the stack with a 0x7000 byte SETUP request!`** → **Unpatched Erista** (*CFW-fähig*).  
  - Meldung **`Smashed the stack with a 0x0000 byte SETUP request!`** → **Patched Erista** (*nicht per RCM softmodbar*).  
- **Typische Ursachen & Fixes:**  
  - Falscher Modus → Stelle sicher, dass die Switch **wirklich** im **RCM** ist (schwarzer Bildschirm, kein Logo).  
  - USB/ Treiber → Anderes **USB‑C‑Datenkabel**/Port testen; TegraRcmGUI ggf. **als Administrator** starten.  
  - Payload → Prüfe, ob **`hekate.bin`** aktuell und korrekt heruntergeladen wurde.

---

**Hinweise**
- **FAT32 ist Pflicht** – exFAT kann zu Datenverlust führen.
- Softmod ist **nicht dauerhaft** – nach jedem vollständigen Ausschalten muss der Payload erneut gesendet werden.
- Nutze aktuelle Versionen von **Hekate** und **Atmosphère** passend zu deiner Firmware.
