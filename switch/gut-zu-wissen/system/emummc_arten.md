---
icon: copy
label: "emuMMC-Typen"
order: 102
---

# Welchen emuMMC hab ich?

In dieser Anleitung erfährst du, wie du herausfinden kannst, **welchen emuMMC** du verwendest.  
Es gibt **zwei Möglichkeiten** – entweder direkt **am PC** oder über **Hekate** auf deiner Switch.

---

## 🖥️ Möglichkeit 1: Am PC

1. Öffne den **emuMMC-Ordner** auf deiner SD-Karte.  
   Pfad: `Root/emuMMC`
2. Dort findest du Unterordner mit Namen wie: RAW1, RAW2, usw. Diese stehen für **SD Partition emuMMC**.
![|700x420](/images/switch/allgemein/emummc.jpg)

3. Alternativ kann auch ein **SD File emuMMC** vorhanden sein – diesen erkennt man an den Ordnern SD00, SD01, usw.
![|700x420](/images/switch/allgemein/emummc2.jpg)
 
---

## 🎮 Möglichkeit 2: Über Hekate (Switch)

1. Starte deine Switch in **Hekate**.  
2. Gehe auf: Close > emuMMC
3. Oben links findest du die Option **Enable**.  
4. Dort steht der aktive Typ, z. B.:  
- **Type: SD RAW** → Partition-basierter emuMMC  
- **SD00**, **SD01**, usw. → Datei-basierter emuMMC

![|700x420](/images/switch/allgemein/emummc3.jpg)

---

> ✅ **Fazit:**  
Wenn bei dir **RAW1** oder **SD RAW** steht, hast du einen **Partition-emuMMC**.  
Wenn du **SD00** oder **SD01** siehst, nutzt du einen **Datei-emuMMC**.