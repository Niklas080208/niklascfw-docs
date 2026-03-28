---
icon: checklist
label: "Voraussetzungen"
order: 70
author:
  name: NiklasCFW
  avatar: /assets/niklas-pfp.png
---

# Voraussetzungen

Bevor du mit dem OmniNX Setup startest, solltest du folgende Punkte erfüllen.

!!!tip Kurz-Check
Alle Punkte auf dieser Seite solltest du erfüllen, bevor du mit [Download](download) weitermachst.
!!!

---

## Switch-Modell prüfen

Deine Switch muss **modbar** sein. Das heißt:

- **Switch V1 (2017–2018), ungepatcht** → CFW per RCM/Softmod möglich  
- **Switch V2 / OLED / Lite** → in der Regel nur mit Modchip

Prüfe deine Seriennummer hier:

- **[serialcheck.niklascfw.de](https://serialcheck.niklascfw.de/)**

![Seriennummer-Check](/images/switch/omninx/voraussetzungen/serialcheck.png)

!!!success Ungepatcht
Du kannst mit diesem Guide weitermachen – CFW per RCM/Softmod ist möglich.
!!!

!!!warning Möglicherweise gepatcht
Unsichere Auskunft. **RCM testen**, ob der Payload-Start funktioniert.
!!!

!!!danger Gepatcht
CFW ohne Modchip **nicht möglich**. Nur mit verbautem Modchip modbar.
!!!

Weitere Infos: [Seriennummern und Switch-Revisionen](/switch/vorbereitung/switch_ungepatcht_check)

---

## SD-Karte

!!!warning Immer FAT32
Für CFW und emuMMC **niemals exFAT** verwenden – nur **FAT32**.
!!!

- **Größe:** Mindestens **256 GB** (V1/V2/Lite), **512 GB** für OLED empfohlen.  
- **Qualität:** Schnelle, zuverlässige Karte (z. B. Samsung EVO Plus/Select, Kingston Canvas Go! Plus).

https://www.youtube.com/watch?v=WW53mOqHqIY

Warum FAT32 und welche Karte: [Richtige SD-Karte](/switch/vorbereitung/richtige_sd) · [SD formatieren](/switch/vorbereitung/sd_format)

---

## Hekate starten können

Du musst **Hekate** starten können, z. B. durch:

- **RCM + Payload-Injection** (z. B. TegraRcmGUI) bei ungepatchter V1, oder  
- **Modchip** bei V1/V2/OLED/Lite.

Falls du noch gar keine CFW hast: [Vorbereitung](/switch/vorbereitung/switch_ungepatcht_check).

---

## prod.keys sichern (empfohlen)

Die **prod.keys** werden mithilfe von dem SysNAND gedumpt. Sie sind z. B. für manche Homebrew-Apps nötig.

- Wenn du noch keine prod.keys hast: Sie können **vor oder nach** der Pack-Installation mit **Lockpick_RCM** aus Hekate gedumpt werden (Launch → Lockpick_RCM → Dump from Sysnand).  
- Bei **OmniNX** ist Lockpick RCM im Pack enthalten.

![Lockpick RCM](/images/switch/omninx/voraussetzungen/lockpick-home.png)

---

## Kurz-Checkliste

| Punkt | Erledigt? |
|-------|-----------|
| Switch modbar (Serial-Check oder Modchip) | :icon-checkbox: |
| SD-Karte FAT32, ausreichend groß & schnell | :icon-checkbox: |
| Hekate (oder Bootloader) startbar | :icon-checkbox: |
| prod.keys später dumperbar (Lockpick RCM) | :icon-checkbox: |

!!!success Alles erfüllt?
Weiter mit dem **[Download von OmniNX](download)**.
!!!
