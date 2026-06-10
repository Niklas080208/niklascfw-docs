# Fehlerbehebung – Installation

Während der **OmniNX-Installation** können verschiedene Hinweise und Fehlermeldungen auftauchen. Hier sind die häufigsten dokumentiert.

---

## Warnung: SD-Karten-Klasse

Erfüllt deine microSD-Karte nicht die empfohlenen Mindestanforderungen (**U2 | V30 | A2**), zeigt der Installer diese Warnung:

![Warnung – SD-Karten-Klasse](/images/switch/omninx/installation/payload-sd-warnung.png)

**Mögliche Folgen bei schwachen Karten:**

- Langsamere emuMMC- / Spiel-Ladezeiten
- Höheres Risiko von Korruption oder Abstürzen
- Instabilität beim Schreiben größerer Daten

**Empfohlen:** **U2 | V30 | A2** oder besser. Bewährte Karten: **Samsung EVO Plus**, **EVO Select** und **PRO Plus**.

!!!info Was tun?
- **A** (oder **Power**) drücken, um **trotzdem fortzufahren** (auf eigenes Risiko).
- **Vol+ und Vol- gleichzeitig**: **Abbrechen** und zurück zu **Hekate**, dann eine passende Karte verwenden.
!!!

Mehr zur Kartenwahl: [!ref](../voraussetzungen/richtige_sd)
