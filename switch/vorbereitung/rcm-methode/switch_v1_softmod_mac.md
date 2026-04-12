# Nintendo Switch V1 – Softmod mit Hekate-Payload (macOS)

Es gibt mehrere Möglichkeiten die Payload über macOS an eure Nintendo Switch zu schicken, hier erklären wir euch zwei davon. Einmal via CrystalRCM (ein offline Tool) und einmal per WebRCM (erfordert eine Internetverbindung). Welche Methode ihr davon auswählt liegt an euch.

---

## 🛠️CrystalRCM (offline Tool)

1. Lade dir die aktuelle Version von **CrystalRCM** über **Github** herunter und installiere diese auf deinem Mac.
   → [CrystalRCM](https://github.com/prayerie/CrystalRCM)
2. Starte **CrystalRCM**.
![|700x420](/images/switch/vorbereitung/rcm/crystalrcm1.png)
3. Versetze deine **Switch** in den **RCM-Modus** und verbinde diese mit deinem **Mac** via **USB**.
![|700x420](/images/switch/vorbereitung/rcm/crystalrcm2.png)
4. Klicke nun auf **select Payload** und wähle die `payload.bin` aus dem **NiklasCFW Pack** aus und klick anschließend auf **Push!** um die Payload an deine Switch zu schicken.
![|700x420](/images/switch/vorbereitung/rcm/crystalrcm3.png)
5. Wenn die Payload erfolgreich an deine Switch geschickt wurde, startet diese jetzt in Hekate.
![|700x420](/images/switch/vorbereitung/rcm/crystalrcm4.png)
---

## 🧰 WebRCM (erfordert eine Internetverbindung)

## Voraussetzungen
- **Kompatibler Browser:** Google Chrome, Microsoft Edge, Opera, Samsung Internet oder QQ Browser  
  *(Safari, Firefox & Co. funktionieren nicht – wegen fehlender WebUSB-Unterstützung)*  
- Funktioniert **nicht** unter Windows (WebUSB-Beschränkung).  
  → Auf Windows stattdessen **TegraRcmGUI** oder **TegraRcmSmash** verwenden.

## Schritte
1. Switch wie gewohnt in den **RCM-Modus** versetzen.  
2. Switch per **USB-C-Datenkabel** verbinden.  
3. **[webrcm.github.io](https://webrcm.github.io/)** im kompatiblen Browser öffnen.  
4. **CTCaer hekate** auswählen (*andere Optionen nicht verwenden!*) und dann **„Do the thing!"** anklicken.  

![|700x420](/images/switch/allgemein/payload_macos.jpg) 
5. Im Dialogfenster das Gerät **APX** auswählen und **Verbinden** klicken.  
6. Payload wird gesendet → Switch startet in **Hekate**.

---

> ⚠️ **Achtung (macOS-Nutzer)**  
> macOS erstellt automatisch versteckte Dateien wie `.DS_Store` und `._Dateiname`.  
> Diese können Probleme mit der CFW verursachen.  
>  
> **Lösung:**  
> - SD-Karte nur im **FAT32-Format** nutzen.  
> - Dateien am besten **auf einem Windows-PC** oder über einen **Linux-Live-Stick** auf die SD kopieren.  
> - Alternativ vor Nutzung auf der Switch alle „._“-Dateien und `.DS_Store` entfernen.

---

**Getestet auf:** macOS
