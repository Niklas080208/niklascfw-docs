---
icon: search
label: "Switch Modell prüfen"
order: 300
---

# Prüfe, ob deine Nintendo Switch ungepatcht ist

Diese Anleitung hilft dir dabei zu prüfen, ob deine Nintendo Switch ungepatcht ist und ob du CFW ohne Modchip nutzen kannst.

---

## 🔍 Seriennummer prüfen

### Schritt 1: Webseite öffnen

Nutze die folgenden Webseite, um anhand der Seriennummer deiner Switch zu prüfen, ob sie „ungepatcht" ist:

- [https://serialcheck.niklascfw.de/](https://serialcheck.niklascfw.de/)

![|700x420](/images/vorbereitung/serial_check.png)

### Schritt 2: Seriennummer eingeben

Gib dort deine Seriennummer ein (findest du auf dem Aufkleber am Gerät oder in den Systemeinstellungen) und lies das Ergebnis ab:

- **Ungepatcht** → CFW ohne Modchip möglich
- **Möglicherweise gepatcht** → Unsicher, Glückssache
- **Gepatcht** → Nur mit Modchip nutzbar

---

## 📖 Hintergrundwissen

Die Nintendo Switch basiert auf dem Nvidia Tegra X1-Chip (seit 2017).  
Anfang 2018 wurde ein Hardware-Exploit namens **Fusée Gelée** entdeckt.

Dieser Exploit ist ein **Coldboot-Exploit**:  
→ Er erlaubt es, beim Einschalten der Konsole vollständigen Zugriff auf das System zu erhalten, bevor irgendeine Sicherheitssoftware geladen wird.

**Fusée Gelée** nutzt eine Schwachstelle im USB-Recovery-Modus der Switch.  
Dadurch wird der Schutz des Bootloaders umgangen.  
Wichtig: Dieser Exploit ist nicht dauerhaft, sondern muss nach jedem Ausschalten erneut aktiviert werden (über RCM und Payload Injection).

---

## 🎮 Switch-Modelle im Überblick

### Ungepatchte Erista (2017-Modelle)

- CFW ohne Modchip möglich
- Verpackung: Weiß

![|700x420](/images/switch_ungepatcht_check/V1-Grey-Box.png)

### Gepatchte Erista (meist 2018-Modelle)

- CFW nur mit Modchip
- Verpackung: Weiß

![|700x420](/images/switch_ungepatcht_check/V1-Grey-Box.png)

### Mariko (ab 2019 – „neue" Switch)

- CFW nur mit Modchip
- Verpackung: Ganz Rot

![|700x420](/images/switch_ungepatcht_check/V2-Box.png)

### Switch Lite

- CFW nur mit Modchip
- Alle Lite-Modelle sind gepatcht

![|700x420](/images/switch_ungepatcht_check/LITE-Box.png)

### Switch OLED

- CFW nur mit Modchip
- Alle OLED-Modelle sind gepatcht

![|700x420](/images/switch_ungepatcht_check/Switch-Oled-Box.png)
