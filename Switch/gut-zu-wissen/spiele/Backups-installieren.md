# 📘 Backups installieren (XCI / XCZ / NSP / NSZ)

Diese Anleitung erklärt dir, wie du Switch-Backups über **Sphaira (MPT Install)** oder **DBI (MTP Responder)** installierst.

---

## 🧩 Dateiformate – Was ist was?

### XCI
- 1:1 Cartridge-Dump einer Spielkarte  
- Enthält das Base Game  
- Kann Updates/DLC enthalten

### XCZ
- Komprimierte XCI  
- Gleiche Inhalte, kleinere Datei  
- Platzsparend

### NSP
- Offizielles eShop-Format  
- Digitale Spiele, Updates & DLCs

### NSZ
- Komprimierte NSP  
- Automatische Dekomprimierung beim Installieren  
- Kleinere Dateigröße


> 💡 Vorbereitung: Stelle sicher, dass du ein geeignetes USB-3-Kabel verwendest und dass dein PC-Port ebenfalls USB-3 unterstützt.
>Geeignete Kabel findest du unter:
>
> https://www.mediamarkt.de/de/product/_isy-iuc-1029-usb-kabel-schwarz-2994540.html    
> https://www.mediamarkt.de/de/product/_hama-usb-c-stecker-auf-usb-buchse-2708227.html Für USB C zu C 
> https://www.amazon.de/dp/B087X5F3NB?


---

# 🟢 **Sphaira – MPT Install**

> 
>
> **1. Sphaira starten**  
> App auf der Switch öffnen.
>
> **2. Minus-Taste (−)** drücken  
> Menü öffnen.
>
> **3. „MPT Install“ auswählen**
>
> **4. Switch per USB verbinden**  
> Windows zeigt dann typischerweise folgende Geräte:
>
> - Album (Image SD)  
> - Games  
> - **Install (NSP, XCI, NSZ, XCZ)** ← **HIER MUSST DU REIN**  
> - microSD card
>
> **5. Backups in den Ordner „Install (NSP, XCI, NSZ, XCZ)“ ziehen**
>
> Unterstützte Formate:
> - XCI  
> - XCZ  
> - NSP  
> - NSZ  
>
> **6. Installation**  
> Sphaira installiert sobald die Dateien den Ordner "berühren" Automatisch los. 

---

# 🔵 **DBI – MTP Responder & SD Card Install**

> **1. DBI öffnen**
>
> **2. „MTP Responder“ auswählen**  
> Die Switch wird am PC als mehrere Partitionen angezeigt.
>
> **3. Windows zeigt z. B. folgende Einträge:**
>
> - 1: SD Card  
> - 2: Nand USER  
> - 3: Nand SYSTEM  
> - 4: Installed games  
> - **5: SD Card install** ← **DIES IST DER INSTALL-ORDNER**  
> - 6: NAND install  
> - 7: Saves  
> - 8: Album  
> - 9: Gamecard  
> - DBIlogs
>
> **4. Backups in „5: SD Card install“ kopieren**
>
> Unterstützte Formate:
> - XCI  
> - XCZ  
> - NSP  
> - NSZ  
>
> **5. Installation**  
> DBI installiert sobald die Dateien den Ordner "berühren" Automatisch los. 

---

