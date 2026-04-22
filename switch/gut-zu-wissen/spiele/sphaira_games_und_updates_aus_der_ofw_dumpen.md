# Sphaira: Games und Updates aus der OFW dumpen

> 💡 **Hinweis:**   Du bist zu 100 % selbst für dein Handeln verantwortlich.
NiklasCFW übernimmt keinerlei Haftung für den eventuellen Bann. 
> ⚠️Wichtig: In Stock CFW **nichts installieren**. ⚠️

---

# 1. Vorbereitungen in der OFW

1. In der OFW alle gewünschten Spiele, Updates und DLCs aus dem eShop herunterladen.
2. Danach den **Flugmodus aktivieren**, um Hintergrundkommunikation zu verhindern.
3. Die Switch neu starten, damit du im Hekate-Bootloader landest.
4. In Hekate: **Lockpic_RCM** >nur **Dump from SysMMC** >Power drücken und machen lassen.
	      >Anschließend mit den **Laustärketasten** auf reboot to Hekate navigieren und wieder Power drücken.  
5. In Hekate: **More Config → Stock CFW** starten.

>‼️ Falls Stock CFW bei dir nicht unter „More Config“ angezeigt wird, kannst du sie über Ultrahand → NiklasCFW Downloader → „Ini“ nachladen. Danach erscheint die Stock-CFW im Hekate >unter More Config.
>
> 💡Fall eine Fehlermeldung **SphairaError_KeyMissingNcaKeyArea** erscheint hast du Punkt 4 der **Vorbereitung** vergessen.
---

# 2. Sphaira über Title Override starten

1. Ein beliebiges Spiel auswählen.
2. **R-Taste gedrückt halten** und das Spiel starten.
3. Dadurch öffnet sich automatisch **Sphaira** statt dem Spiel.

---

# 3. Spiele und Updates dumpen

## 3.1 In das Spiele-Menü gelangen
- Im Sphaira-Hauptbildschirm die **MINUS-Taste (–)**Joycon drücken.
- Der Bereich **Spiele** öffnet sich.

## 3.2 Das gewünschte Spiel auswählen

1. **Spiel** auswählen und mit **X** bestätigen um das Spiel Optionen Menü zu öffnen.
2. **View Application Content** wählen .
3. Es erscheint eine Liste aller enthaltenen Daten:
   - Application (Base Game)
   - Update
   - DLC
   - Zusätzliche Inhalte

## 3.3 Dump der Inhalte
Da Sphaira in diesem Menü **keine Alles-dumpen-Funktion** hat, werden alle Inhalte **einzeln** exportiert.

Für jeden Eintrag:

1. Eintrag auswählen
2. X drücken
3. „Export NSZ“ wählen
4. Dump abwarten
5. → Du bleibst im Menü
6. → Nächsten Eintrag dumpen

Beispiel:
- Application → X → Export NSZ
- Update → X → Export NSZ
- DLC → X → Export NSZ

Die Dumps erscheinen danach automatisch im Ordner:
> 📂/dumps/NSZ/

> ❗Bevor du je wieder in die CFW gehst. 

1. Im Sphaira **Ultrahand** über bekannte Tastenkombination oder mit wischen von links nach rechts öffnen.
2. **Reboot NX** wählen.
3. Danach direkt **„Neustart OFW“** auswählen.
4. Die Konsole startet in die OFW. 
5. Wenn das Erste Nintendo Switch Logo weg ist halte Vol **+** und Vol **-** gedrückt um in den Nintendo Switch Rücksetzmodus zu kommen. In diesem bitte unbedingt den Werksreset machen um die Spuren zu verwischen. 

Wenn du irgendwann wieder in die OFW kommst wirst du aufgefordert zu Löschen. 

>📌 Nach einem Werksreset erkennt die OFW die SD-Karte nicht, solange der alte Nintendo-Ordner noch drauf ist. Du musst in der OFW einfach nur auf „Löschen“ drücken, dann wird ausschließlich der Nintendo-Ordner neu erstellt und nichts anderes angefasst. Danach erkennt die OFW die SD-Karte wieder ganz normal. Die CFW bleibt komplett erhalten, da wird nichts formatiert oder gelöscht.

# 4. In die CFW wechseln

1. Nach dem du deine Switch auf Werkseinstellungen gesetzt hast dauert ein Bisschen startet Sie neu und du erreichst Hekate. 
2. Von da kannst du dann unter Launch wieder auf CFW gehen und in die Custom Firmware booten. 

---

# 5. Dumps finden und installieren

## 5.1 Dumps im Datei-Manager finden
1. Sphaira in der CFW normal starten.
2. **L drücken**, um den Datei-Manager zu öffnen.
3. Navigieren zu:

> 📂/dumps/NSZ/

4. Dort liegen Ordner wie zum Beispiel: Inazuma Eleven

Darin dann:
 - Application (Base Game)
   - Update
   - DLC
   - Zusätzliche Inhalte

## 5.2 Installationsmöglichkeiten

### Option A: Installation über Sphaira
- Reihenfolge: Base → Update → DLC

Zum Installieren X Drücken und dann **Installieren** im Menü wählen. 
Wenn A gedrückt wird geht nur der getrimte Ordner auf.

### Option B: Installation über TinWoo

- TinWoo unterstützt **Mehrfachauswahl** und ist ideal für mehrere DLCs.

1. Von SD-Karte Installieren -> A
2. dumps -> A
3. NSZ -> A
4. Beispiel Inazuma Eleven -> A
5. Mit ->Y<- Alle auswählen und mit ->PLUS-Taste (+)<- vom Joycon drücken und damit die installation bestätigen.

---

>🐒**Ende:**  
Du hast gerade erfolgreich deine Spiele und Updates gedumpt.
