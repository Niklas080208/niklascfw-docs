# Nintendo Switch V1 – Softmod mit Hekate-Payload (Linux, Android, ChromeOS)

Mit **[WebRCM](https://webrcm.github.io/)** kann der Payload direkt im Browser gesendet werden – ohne zusätzliche Software.

## Voraussetzungen
- **Kompatibler Browser:** Google Chrome, Microsoft Edge, Opera, Samsung Internet oder QQ Browser  
  *(Safari, Firefox & Co. funktionieren nicht – wegen fehlender WebUSB-Unterstützung)*  
- Funktioniert **nicht** unter Windows (WebUSB-Beschränkung).  
  → Auf Windows stattdessen **TegraRcmGUI** oder **TegraRcmSmash** verwenden.

---

## Schritte
1. Switch wie gewohnt in den **RCM-Modus** versetzen.  
2. Switch per **USB-C-Datenkabel** verbinden.  
3. **[webrcm.github.io](https://webrcm.github.io/)** im kompatiblen Browser öffnen.  
4. **CTCaer hekate** auswählen (*andere Optionen nicht verwenden!*) und dann **„Do the thing!"** anklicken.  

![|700x420](/images/allgemein/payload_macos.jpg) 
5. Im Dialogfenster das Gerät **APX** auswählen und **Verbinden** klicken.  
6. Payload wird gesendet → Switch startet in **Hekate**.

---

## Hinweise für Linux-Nutzer
Falls „Access Denied“-Fehler erscheint:  
1. Datei erstellen: `/etc/udev/rules.d/50-switch.rules`  
2. Folgenden Inhalt einfügen:
   ```
   SUBSYSTEM=="usb", ATTR{idVendor}=="0955", MODE="0664", GROUP="plugdev"
   ```
3. System neu starten.

---

**Getestet auf:** Linux, Android (unrooted) und Chromebooks
