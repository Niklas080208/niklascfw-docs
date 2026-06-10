---
icon: "/assets/rcm-jig.png"
label: "RCM-Methode"
order: 400
---

# RCM-Methode verstehen

Bevor du den Payload sendest, ist es hilfreich zu verstehen, was bei RCM technisch passiert.

---

## Was ist RCM?

**RCM** steht für **Recovery Mode**. Das ist ein Wartungsmodus des Tegra-Chips in der Nintendo Switch.

Wenn die Switch in RCM startet, wartet sie auf einen Payload über USB.  
Bei einer ungepatchten V1 kann man dadurch z. B. **Hekate** laden.

!!!info Modus vs. Exploit
RCM als Modus existiert auf allen Switch-Modellen.  
Der eigentliche Exploit (`fusee-gelee`) funktioniert nur auf ungepatchten Geräten.
!!!

---

## Was macht der Payload?

Ein Payload (z. B. `hekate.bin`) ist ein kleines Programm, das beim Start direkt in den Speicher geladen wird.

Damit kannst du:

- Hekate starten
- Backups erstellen
- emuMMC verwalten
- CFW starten

---

## Warum funktioniert das nicht bei jeder Switch?

Der bekannte RCM-Exploit funktioniert nur bei **ungepatchten Erista-Modellen** (frühe V1).

- **Ungepatcht**: RCM-Payload-Start möglich
- **Gepatcht / V2 / Lite / OLED**: kein Softmod per RCM, nur mit Modchip

Wenn du unsicher bist, prüfe zuerst deine Seriennummer:
[!ref](../serial_check.md)

---

## Wichtig zu wissen

!!!warning Kein dauerhafter Jailbreak
RCM ist kein permanenter Exploit. Nach einem kompletten Ausschalten musst du den Payload erneut senden.
!!!

!!!info Sicherheit
RCM selbst ändert noch nichts an deinen Daten. Änderungen passieren erst durch das, was du danach startest.
!!!

---

## RCM sicher erreichen

!!!warning Kein Paperclip oder Alufolie
Improvisierte Kurzschluss-Methoden können die Joy-Con-Schiene beschädigen.  
Nutze nach Möglichkeit einen passenden RCM-Jig.
!!!

Standardablauf:

1. Switch vollständig ausschalten.
2. RCM-Jig rechts einsetzen.
3. **Volume +** halten und einmal **Power** drücken.
4. Bildschirm bleibt schwarz, dann ist RCM aktiv.

---

## Nächster Schritt

[!ref text="Payload laden (Windows/macOS/Linux)"](payload_laden)
