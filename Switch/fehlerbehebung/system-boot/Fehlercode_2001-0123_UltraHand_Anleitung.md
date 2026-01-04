Anleitung: Fehlercode 2001-0123 (UltraHand-ID) beheben

Ursache:
Der Fehlercode 2001-0123 steht in diesem Zusammenhang für UltraHand.
Die installierte System-Firmware ist zu niedrig für die verwendete UltraHand-Version
oder das CFW-Pack ist nicht aktuell bzw. nicht korrekt installiert.

Lösung – Schritt für Schritt:

1. CFW-Pack aktualisieren
- Lade die neuste Niklas CFW herunter. 
- Falls nötig, das Pack manuell aktualisieren.

2. Overlay temporär deaktivieren
- SD-Karte in den PC einlegen
- Zum folgenden Pfad navigieren:
  /switch/.overlays/
- Datei umbenennen:
  ovlmenu.ovl -> ovlmenu.ovl.bak

3. Firmware herunterladen
- Aktuelle Firmware herunterladen:
  https://github.com/THZoria/NX_Firmware/releases

4. Firmware installieren
- Firmware entpacken
- Den entpackten Ordner vollständig auf die SD-Karte kopieren
- SD-Karte wieder in die Switch einsetzen
- Switch starten
- Album öffnen -> Daybreak
- Firmware-Update durchführen (empfohlen: Preserve Settings)

5. Overlay wieder aktivieren
- Switch ausschalten
- SD-Karte wieder in den PC stecken
- Zum Pfad /switch/.overlays/ gehen
- Datei wieder umbenennen:
  ovlmenu.ovl.bak -> ovlmenu.ovl

Abschluss:
- SD-Karte wieder einsetzen
- Switch starten
- UltraHand und Overlay sollten nun wieder funktionieren -> Ultrahand started erscheint oben links. 
