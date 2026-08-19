# Auto RCM aktivieren

Ohne Modchip kann **Auto RCM** den **JIG** ersetzen: Nach **Power** geht die Switch automatisch in den **RCM-Modus** – ohne JIG im Joy-Con-Slot. Den **Payload** (z. B. Hekate) musst du trotzdem per **RCM-Loader** oder anderem RCM-Tool laden.

!!!warning Nur für ungepatchte Switches (RCM)
Auto RCM ist für **RCM-Softmod**-Setups gedacht – **nicht** für Modchip-Konsolen.
!!!

[!ref text="Payload laden (Windows/macOS/Linux)"](../vorbereitung/voraussetzungen/serial_check/rcm-methode/payload_laden)

---

## Auto RCM in Hekate aktivieren

>>> Hekate öffnen
Starte **Hekate** und tippe oben rechts auf **Close**.

![Hekate Launch – Close|700x420](/images/switch/allgemein/hekate_launch_close.jpg)

>>> Tools öffnen
Wähle **Tools**.

![Hekate Tools|700x420](/images/switch/allgemein/hekate_tools.jpg)

>>> Arch bit RCM Touch Pkg öffnen
Tippe auf **Arch bit RCM Touch Pkg 1/2**.

![Arch bit RCM Touch Pkg|700x420](/images/switch/allgemein/hekate_archbits1.jpg)

>>> Auto RCM aktivieren
Wähle **Auto RCM**.

![Auto RCM auswählen|700x420](/images/switch/allgemein/autorcmaktivieren.jpg)

Bestätige die Meldung mit **OK**.

![Auto RCM Bestätigung|700x420](/images/switch/allgemein/autorcmbestaetigung.jpg)

Auto RCM ist damit aktiv.

![Auto RCM aktiv|700x420](/images/switch/allgemein/autorcmaktiv.jpg)

>>>

!!!success Fertig
Die Switch geht nach **Power** automatisch in den RCM-Modus – ohne JIG. Payload wie gewohnt per **RCM-Loader** laden, danach bootest du in **Hekate**.
!!!
