# Auto RCM aktivieren

Ohne Modchip kann **Auto RCM** den **JIG** ersetzen: Die Switch bootet per **Power + RCM-Loader** (oder anderem RCM-Tool) direkt in **Hekate**, sobald Auto RCM gesetzt ist.

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
Die Switch startet mit der **RCM-Methode** (Power + RCM-Loader) direkt in Hekate – ohne JIG in den Joy-Con-Slot.
!!!
