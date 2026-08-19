---
icon: download
label: "Sphaira: OFW-Dumps"
order: 104
description: "Spiele, Updates und DLCs aus der OFW mit Sphaira dumpen und in der CFW installieren."
---

# Sphaira: Games und Updates aus der OFW dumpen

!!!danger Eigenverantwortung und Bann-Risiko
Du bist zu **100 % selbst** für dein Handeln verantwortlich. NiklasCFW übernimmt **keinerlei Haftung** für einen eventuellen **Online-Bann**.
!!!

!!!warning Stock CFW: nichts installieren
In **Stock CFW** darfst du **nichts installieren**. Nur dumpen und danach die OFW zurücksetzen.
!!!

---

## Vorbereitung in der OFW

>>> Spiele in der OFW herunterladen
In der **OFW** alle gewünschten **Spiele**, **Updates** und **DLCs** aus dem eShop herunterladen.

>>> Flugmodus aktivieren
**Flugmodus** einschalten, um Hintergrundkommunikation zu verhindern.

>>> Neu starten bis Hekate
Die Switch **neu starten**, bis du im **Hekate-Bootloader** landest.

>>> prod.keys mit Lockpick RCM dumpen
In Hekate: **Lockpick RCM** → nur **Dump from SysMMC** → **Power** drücken und durchlaufen lassen. Anschließend mit den **Lautstärketasten** auf **Reboot to Hekate** navigieren und wieder **Power** drücken.

>>> Stock CFW starten
In Hekate: **More Config** → **Stock CFW** starten.

>>>

!!!tip Stock CFW fehlt unter More Config?
Über **UltraHand** → **OmniNX Downloader** → **Ini** nachladen. Danach erscheint **Stock CFW** unter **More Config** in Hekate.
!!!

!!!tip Fehler SphairaError_KeyMissingNcaKeyArea
Diese Meldung bedeutet: Schritt **prod.keys dumpen** (Lockpick RCM) wurde übersprungen. Zurück zu Hekate und **Dump from SysMMC** ausführen.
!!!

[!ref text="prod.keys mit Lockpick RCM"](../../system-backup/prodkeys)
[!ref text="UltraHand im Pack"](../apps-tools/ultrahand_cfwpack)

---

## Sphaira per Title Override starten

>>> Spiel auswählen
Ein beliebiges **Spiel** auf dem Startbildschirm markieren.

>>> Mit R-Taste starten
**R-Taste gedrückt halten** und das Spiel mit **A** starten.

>>> Sphaira erreichen
**R loslassen**, sobald **Sphaira** erscheint – statt des Spiels öffnet sich **Sphaira**.

>>>

[!ref text="Title Override (Highmemory Mode)"](../customization/title_override)

---

## Inhalte dumpen

### Spiele-Menü öffnen

>>> Minus-Taste drücken
Im Sphaira-Hauptbildschirm die **MINUS-Taste (−)** am Joy-Con drücken. Der Bereich **Spiele** öffnet sich.

>>>

### Spiel auswählen

>>> Spiel und Inhaltsliste öffnen
1. **Spiel** auswählen und mit **X** bestätigen, um das Optionsmenü zu öffnen.
2. **View Application Content** wählen.

Es erscheint eine Liste aller enthaltenen Daten:

- Application (Base Game)
- Update
- DLC
- Zusätzliche Inhalte

>>>

### Inhalte exportieren

Sphaira hat in diesem Menü **keine Alles-dumpen-Funktion** – alle Inhalte werden **einzeln** exportiert.

Für **jeden** Eintrag:

1. Eintrag auswählen
2. **X** drücken
3. **Export NSZ** wählen
4. Dump abwarten (du bleibst im Menü)
5. Nächsten Eintrag dumpen

**Beispiel:**

- Application → **X** → Export NSZ
- Update → **X** → Export NSZ
- DLC → **X** → Export NSZ

Die Dumps landen automatisch unter:

`/dumps/NSZ/`

---

## OFW zurücksetzen

!!!warning Vor dem Wechsel zurück in die CFW
**Unbedingt** zuerst die OFW zurücksetzen – sonst bleiben Spuren auf dem SysNAND.
!!!

>>> UltraHand öffnen
In **Sphaira** **UltraHand** öffnen (bekannte Tastenkombination oder **von links nach rechts wischen**).

>>> Reboot NX wählen
**Reboot NX** auswählen.

>>> Neustart OFW
Direkt danach **Neustart OFW** wählen. Die Konsole startet in die **OFW**.

>>> Rücksetzmodus öffnen
Sobald das **erste Nintendo-Switch-Logo** verschwindet, **Vol+** und **Vol−** **gleichzeitig gedrückt halten**, bis der **Nintendo Switch Rücksetzmodus** erscheint.

>>> Werksreset durchführen
Im Rücksetzmodus **unbedingt den Werksreset** ausführen, um Spuren zu verwischen.

>>>

!!!tip SD-Karte nach Werksreset
Nach einem Werksreset erkennt die OFW die SD-Karte nicht, solange der alte **Nintendo**-Ordner noch darauf liegt. In der OFW einfach auf **Löschen** tippen – dann wird **nur** der Nintendo-Ordner neu erstellt, **nichts anderes** angefasst. Die **CFW bleibt vollständig erhalten** (keine Formatierung der SD). Danach erkennt die OFW die SD-Karte wieder normal.

Wenn du später erneut in die OFW kommst, wirst du ggf. erneut zum Löschen aufgefordert – das ist erwartet.
!!!

[!ref text="Switch zurücksetzen / Rücksetzmodus"](../system/switch_ruecksetzmodus)

---

## In CFW booten und installieren

### In die CFW booten

>>> Nach Werksreset zu Hekate
Nach dem Werksreset startet die Konsole neu – du landest in **Hekate**.

>>> CFW starten
Unter **Launch** → **CFW** wählen und in die **Custom Firmware** booten.

>>>

### Dumps im Datei-Manager finden

>>> Sphaira starten
**Sphaira** in der CFW normal starten.

>>> Datei-Manager öffnen
**L** drücken, um den **Datei-Manager** zu öffnen.

>>> Zum NSZ-Ordner navigieren
Zu **`/dumps/NSZ/`** wechseln. Dort liegen Ordner pro Spiel (z. B. *Inazuma Eleven*) mit Unterordnern wie Application, Update, DLC und weiteren Inhalten.

>>>

### Installationsmöglichkeiten

**Option A: Installation über Sphaira**

- Reihenfolge: **Base** → **Update** → **DLC**
- Zum Installieren **X** drücken und **Installieren** wählen
- Mit **A** wird nur der **getrimmte** Ordner geöffnet

**Option B: Installation über TinWoo**

TinWoo unterstützt **Mehrfachauswahl** und eignet sich gut für viele DLCs:

1. **Von SD-Karte installieren** → **A**
2. **dumps** → **A**
3. **NSZ** → **A**
4. Spielordner (z. B. *Inazuma Eleven*) → **A**
5. Mit **Y** alle Einträge auswählen und mit **Plus (+)** am Joy-Con die Installation bestätigen

!!!success Fertig
Spiele und Updates sind gedumpt und in der CFW installiert.
!!!

[!ref Spiele installieren (DBI / Sphaira)](spiele_installation_dbi_sphaira)
