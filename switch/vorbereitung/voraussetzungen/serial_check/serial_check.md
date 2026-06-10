---
icon: search
label: "Switch Modell prüfen"
order: 300
---

# Prüfe, ob deine Nintendo Switch ungepatcht ist

Diese Anleitung hilft dir dabei zu prüfen, ob deine Nintendo Switch ungepatcht ist und ob du CFW ohne Modchip nutzen kannst.

---

## Seriennummer prüfen

Nutze die folgenden Webseite, um anhand der Seriennummer deiner Switch zu prüfen, ob sie „ungepatcht" ist:

- [https://serialcheck.niklascfw.de/](https://serialcheck.niklascfw.de/)

![|700x420](/images/switch/omninx/voraussetzungen/serialcheck.png)

Gib dort deine Seriennummer ein (findest du auf dem Aufkleber am Gerät oder in den Systemeinstellungen) und lies das Ergebnis ab:

- **Ungepatcht** → CFW ohne Modchip möglich
- **Möglicherweise gepatcht** → Unsicher, Glückssache
- **Gepatcht** → Nur mit Modchip nutzbar

!!!success Ungepatcht
Du kannst mit dem Guide weitermachen. CFW per RCM/Softmod ist möglich.

Nächster Schritt: [Payload laden](rcm-methode/payload_laden)
!!!

!!!warning Möglicherweise gepatcht
Unsichere Auskunft. Teste per RCM, ob der Payload-Start funktioniert.

Wenn nach dem Laden des Payloads der Bildschirm schwarz bleibt, ist die Konsole sehr wahrscheinlich gepatcht.  
Prüfe vorher kurz Kabel, USB-Port und Payload-Datei.

Wenn der Payload-Start nicht klappt: [Modchip einbauen](modchip)
!!!

!!!danger Gepatcht
CFW ohne Modchip ist nicht möglich. Nur mit verbautem Modchip modbar.

Nächster Schritt: [Modchip einbauen](modchip)
!!!

---

## Hintergrundwissen

Die Nintendo Switch basiert auf dem Nvidia Tegra X1-Chip (seit 2017).  
Anfang 2018 wurde ein Hardware-Exploit namens **Fusée Gelée** entdeckt.

Dieser Exploit ist ein **Coldboot-Exploit**:  
→ Er erlaubt es, beim Einschalten der Konsole vollständigen Zugriff auf das System zu erhalten, bevor irgendeine Sicherheitssoftware geladen wird.

**Fusée Gelée** nutzt eine Schwachstelle im USB-Recovery-Modus der Switch.  
Dadurch wird der Schutz des Bootloaders umgangen.  
Wichtig: Dieser Exploit ist nicht dauerhaft, sondern muss nach jedem Ausschalten erneut aktiviert werden (über RCM und Payload Injection).

---

## Switch-Modelle im Überblick

### Ungepatchte Erista (2017-Modelle)

- CFW ohne Modchip möglich
- Verpackung: Weiß

![|560x336](/images/switch/vorbereitung/seriennummer/v1-grey-box.png)

### Gepatchte Erista (meist 2018-Modelle)

- CFW nur mit Modchip
- Verpackung: Weiß

![|560x336](/images/switch/vorbereitung/seriennummer/v1-grey-box.png)

### Mariko (ab 2019 – „neue" Switch)

- CFW nur mit Modchip
- Verpackung: Ganz Rot

![|560x336](/images/switch/vorbereitung/seriennummer/v2-box.png)

### Switch Lite

- CFW nur mit Modchip
- Alle Lite-Modelle sind gepatcht

![|560x336](/images/switch/vorbereitung/seriennummer/lite-box.png)

### Switch OLED

- CFW nur mit Modchip
- Alle OLED-Modelle sind gepatcht

![|560x336](/images/switch/vorbereitung/seriennummer/switch-oled-box.png)
