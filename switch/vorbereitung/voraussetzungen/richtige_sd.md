---
icon: database
label: "Richtige SD-Karte"
order: 200
---

# Die richtige Speicherkarte

Die microSD-Karte ist das Herzstück des Systems. Hier liegen Spiele, Homebrew-Apps und oft auch wichtige Systemdaten. Eine minderwertige oder zu langsame Speicherkarte kann dabei nicht nur zu langen Ladezeiten führen, sondern auch zu Datenfehlern, Abstürzen oder gar einem beschädigten Dateisystem.

---

!!!info Hinweis
Bei einer **Switch V1, V2 und Lite** werden mindestens **256 GB** Speicher empfohlen.  
Bei einer **Switch OLED** werden **512 GB** empfohlen.
!!!

---

## Kurzfassung

- **Größe:** Mindestens **256 GB** (V1/V2/Lite), **512 GB** für OLED empfohlen.
- **Qualität:** Schnelle, zuverlässige Markenkarte (z. B. Samsung EVO Plus/Select, PRO Ultimate, T7/T9, Kingston Canvas Go! Plus).
- **Wichtig für CFW:** Gute Random-Performance (IOPS) sorgt für stabilere Installationen und weniger Lese-/Schreibfehler.
- **Vermeiden:** Sehr langsame oder No-Name-Karten, da sie emuMMC und Homebrew unnötig ausbremsen.

https://www.youtube.com/watch?v=WW53mOqHqIY

---

## Warum Geschwindigkeit entscheidend ist

CFW-Nutzer belasten die SD-Karte deutlich stärker als normale Switch-User:
- große Dateien laden  
- Spiele direkt von der SD-Karte installieren  
- Archive entpacken  
- emuMMC + CFW greifen parallel auf die Karte zu  

Langsame SD-Karten bremsen diesen Prozess erheblich und erhöhen das Risiko von  
Lese-/Schreibfehlern, Abstürzen oder beschädigten Daten.  
Entscheidend ist vor allem die **zufällige Lese-/Schreibgeschwindigkeit (IOPS)**,  
da dabei **tausende kleiner Dateien** verarbeitet werden.

## Vergleich typischer microSD-Karten

Nachfolgend eine Übersicht der im Test genannten Karten und ihrer relevanten Leistungswerte. Werte für **Samsung PRO Ultimate** stammen aus dem [COMPUTER BILD-Labortest](https://www.computerbild.de/bestenlisten/microSD-Karten-Test-11451231.html) (Schreib-IOPS aus Zugriffszeit ~0,494 ms). Für **T7/T9** gibt es noch keine vergleichbaren IOPS-Messwerte (nur Hersteller-A2: min. 4000/2000 IOPS).

| SD-Karte                 | Zugriffszeit (ms) | Lese-IOPS | Schreib-IOPS | Bewertung |
|--------------------------|-------------------|-----------|--------------|-----------|
| Adata SDXC 128 GB        | **0,572 ms**      | **1750 IOPS** | **375 IOPS**   | Deutlich zu langsam |
| Emtec Gaming 256 GB      | **0,862 ms**      | **1160 IOPS** | **40 IOPS**    | Unterdurchschnittlich |
| Amazon Basic 512 GBB (Gold) | **0,430 ms**   | **2325 IOPS** | **2450 IOPS**  | Ausreichend |
| Amazon Basic 1 TB (Black) | **0,430 ms**     | **2325 IOPS** | **2450 IOPS**  | Ausreichend |
| Kingston Canvas Go! Plus 512 GB | **0,299 ms**      | **3345 IOPS** | **2066 IOPS**  | Sehr schnell |
| Lexar 633x 512 GB        | **0,414 ms**      | **2418 IOPS** | **1640 IOPS**  | langsam |
| Samsung EVO 64 GB (gelb) | **0,391 ms**      | **2566 IOPS** | **1941 IOPS**  | langsam |
| Samsung EVO Plus 256 GB  | **0,367 ms**      | **2725 IOPS** | **2220 IOPS**  | Schnell |
| Samsung EVO Plus 512 GB  | **0,268 ms**      | **3728 IOPS** | **2081 IOPS**  | Sehr schnell / Empfehlung |
| Samsung EVO Select 1 TB  | **0,249 ms**      | **4025 IOPS** | **2580 IOPS**  | Sehr schnell / Empfehlung |
| Samsung PRO Ultimate     | **0,288 ms**      | **3476 IOPS** | **~2020 IOPS** | Sehr schnell / Empfehlung |
| Samsung T7               | —                 | —¹          | —¹           | Empfehlung (Nachfolger) |
| Samsung T9               | —                 | —¹          | —¹           | Empfehlung (Nachfolger) |
| SanDisk Ultra 512 GB     | **0,560 ms**      | **1975 IOPS** | **330 IOPS**   | Deutlich zu langsam |
| SanDisk Extreme 512 GB   | **0,437 ms**      | **2290 IOPS** | **2440 IOPS**  | Ausreichend |
| Silicon Power Superior Pro 256 GB | **0,666 ms**      | **1500 IOPS** | **500 IOPS**   | Unterdurchschnittlich |

¹ Herstellerangabe A2 (mindestens 4000 Lese- / 2000 Schreib-IOPS), keine unabhängigen Labormessungen im gleichen Format.

**Legende:**
- **Zugriffszeit:** je niedriger, desto schneller reagiert die Karte  
- **IOPS:** wie viele kleine Datenzugriffe pro Sekunde möglich sind  
- **Hohe Werte → schnellere Installationen, weniger Fehler, stabiler emuMMC-Betrieb**

## Zusammengefasst

Die Samsung EVO liegt leistungsmäßig praktisch gleichauf mit der teureren Canvas Go! Plus,  
kostet aber **20–30 € weniger**.  
SanDisk Ultra und ähnliche Low-End-Karten bremsen die Switch massiv aus und sollten für CFW/emuMMC **nicht verwendet werden**.

---

## Zuverlässigkeit schützt vor Datenverlust

Billige No-Name-Karten versagen oft schneller – im schlimmsten Fall mitten in einem Schreibvorgang. Das kann Speicherinhalte unbrauchbar machen. Markenmodelle bieten nicht nur höhere Geschwindigkeiten, sondern auch bessere Haltbarkeit und Fehlerkorrektur.

---

## Unsere Empfehlungen

Für eine reibungslose Nutzung der Nintendo Switch mit CFW empfehlen sich vor allem bewährte und getestete Modelle:

### Samsung EVO Select

**Preis-Leistungs-Sieger** mit soliden Geschwindigkeiten für alle Standard-Anwendungen. Diese Speicherkarte gibt es nur bei Amazon.

[!button variant="secondary" text="Samsung EVO Select bei Amazon" icon="/assets/amazon.svg" target="blank" corners="pill"](https://www.amazon.de/dp/B09D3LP52K)

![|234x140](/images/switch/vorbereitung/sd-karte/evoselect.png)

### Samsung EVO Plus

**Noch schneller beim Schreiben**, ideal für häufige Installationen und große Spielebibliotheken.

[!button variant="secondary" text="Samsung EVO Plus bei Amazon" icon="/assets/amazon.svg" target="blank" corners="pill"](https://www.amazon.de/dp/B0D1CHNC49)

![|234x140](/images/switch/vorbereitung/sd-karte/evoplus.png)

### Samsung PRO Plus

**High-End-Performance** mit maximaler Zuverlässigkeit, perfekt für Power-User und große Datenmengen.

[!button variant="secondary" text="Samsung PRO Plus bei Amazon" icon="/assets/amazon.svg" target="blank" corners="pill"](https://www.amazon.de/dp/B0BYPBY2JT)

![|234x140](/images/switch/vorbereitung/sd-karte/proplus.png)

### Samsung PRO Ultimate

**Top-Geschwindigkeit** mit bis zu 200 MB/s Lesen und 130 MB/s Schreiben (A2/V30), ideal für große Bibliotheken und intensive emuMMC-Nutzung.

[!button variant="secondary" text="Samsung PRO Ultimate bei Amazon" icon="/assets/amazon.svg" target="blank" corners="pill"](https://www.amazon.de/dp/B0CBMFJF7V)

![|234x140](/images/switch/vorbereitung/sd-karte/proultimate.png)

### Samsung T7

**Starker Allrounder** für Alltag und Gaming mit bis zu 170 MB/s Lesen, A2/V30 und Kapazitäten bis 1 TB. Gut geeignet für Switch und handheld-nahe Nutzung.

[!button variant="secondary" text="Samsung T7 bei MediaMarkt" icon="/assets/mediamarkt.png" target="blank" corners="pill"](https://www.mediamarkt.de/de/product/_samsung-t7-micro-sd-microsd-speicherkarte-256-gb-3044988.html)

![|234x140](/images/switch/vorbereitung/sd-karte/t7.png)

### Samsung T9

**Nachfolger im High-End-Segment** mit bis zu 200 MB/s Lesen und 130 MB/s Schreiben (A2/V30). Maximale Performance und Zuverlässigkeit für anspruchsvolle CFW-Setups.

[!button variant="secondary" text="Samsung T9 bei Samsung" icon="link" target="blank" corners="pill"](https://www.samsung.com/de/memory-storage/memory-card/t9-microsd-card-512gb-mb-mh512t-ww/)

![|234x140](/images/switch/vorbereitung/sd-karte/t9.png)

---

!!!info Fazit
Eine hochwertige microSD-Karte ist bei einer CFW-Nutzung der Nintendo Switch kein Luxus, sondern eine Notwendigkeit. Wer hier spart, riskiert Frust und Datenverlust und wer investiert, spielt sorgenfrei.
!!!
