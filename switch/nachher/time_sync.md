---
icon: clock
label: "Uhrzeit Syncen (NTP)"
order: 80
description: "Systemzeit der Switch per QuickNTP (UltraHand) oder DBI per NTP synchronisieren."
---

# Uhrzeit synchronisieren

Eine korrekte **Systemzeit** ist wichtig für Online-Funktionen, Updates und viele Homebrew-Apps. Am schnellsten geht es mit **QuickNTP** in **UltraHand** – alternativ per **DBI** und **NTP**.

!!!info Internet erforderlich
Die Switch muss **mit dem Internet verbunden** sein – per WLAN oder Ethernet-Adapter.
!!!

!!!warning Systemzeit
OmniNX blockiert Nintendo-Server **standardmäßig** ([Details](/switch/gut-zu-wissen/system/nintendo-server)). Deshalb musst du die **Systemzeit** manuell synchronisieren. Sonst funktionieren **internetabhängige Aufgaben** nicht zuverlässig.
!!!

---

## Uhrzeit synchronisieren

>>> Datum und Uhrzeit öffnen
Öffne **Einstellungen → Konsole → Datum und Uhrzeit**.

![Datum und Uhrzeit in den Einstellungen|700x420](/images/switch/gut-zu-wissen/apps-tools/dbi/dbi_time1.jpg)

>>> Internet-Synchronisierung aktivieren
Stelle sicher, dass **Uhr mithilfe des Internets synchronisieren** auf **Ein** steht.

![Internet-Synchronisierung aktivieren|700x420](/images/switch/gut-zu-wissen/apps-tools/dbi/dbi_time2.jpg)
>>>

+++ QuickNTP (UltraHand)
>>> UltraHand öffnen
**UltraHand** öffnen (**L** + **R** + **Plus**).

![UltraHand – Pakete|700x420](/images/switch/omninx/einrichtung/ultrahand-home.jpg)

>>> Overlay-Sektion
Zur **Overlay**-Sektion wechseln (**D-Pad rechts**).

![UltraHand – Overlays|700x420](/images/switch/omninx/einrichtung/ultrahand-overlays.jpg)

>>> QuickNTP – Zeit synchronisieren
**QuickNTP** auswählen und Zeit synchronisieren (**A** auf **Sync time**).

![QuickNTP – Zeit synchronisieren|700x420](/images/switch/omninx/einrichtung/ultrahand-quickntp.jpg)
>>>

+++ DBI (NTP)
>>> DBI öffnen und Tools wählen
Starte **DBI** und wähle **Tools**.

![DBI Tools-Menü|700x420](/images/switch/gut-zu-wissen/apps-tools/dbi/dbi_time3.jpg)

>>> NTP-Zeitsynchronisierung starten
Wähle **NTP-Zeitsynchronisierung** bzw. **NTP time sync** und bestätige.

![NTP time sync in DBI|700x420](/images/switch/gut-zu-wissen/apps-tools/dbi/dbi_time4.jpg)

>>> Synchronisierung abschließen
Die Uhrzeit wird automatisch angepasst. Mit **B** das Menü wieder verlassen.

![Synchronisierung abgeschlossen|700x420](/images/switch/gut-zu-wissen/apps-tools/dbi/dbi_time5.jpg)
>>>
+++

---

!!!success Fertig
Die Systemzeit ist synchronisiert. Bei Download-Problemen später erneut prüfen oder [Fehlerbehebung](/switch/fehlerbehebung/apps-tools/niklascfwdownloadprobleme) lesen.
!!!
