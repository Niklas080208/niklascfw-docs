# Anleitung: OFW-Spiele + Updates in emuMMC übernehmen (ohne Saves zu verlieren)

:warning: **Wichtig – nur wenn alle Bedingungen erfüllt sind, funktioniert das Dumpen:**

:small_orange_diamond: Deine Konsole muss zur **Ticketverwendung registriert** sein  
Und Einstellungen > Nutzer > Online-Lizenz-Einstellung > Nutzername > Online-Lizenz-Einstellung **Aus**

---

Du holst dir Spiele & Updates aus der echten Firmware (OFW) in eine neue emuMMC.  
:heavy_check_mark: Spielstände (Saves) bleiben erhalten  
:heavy_check_mark: Und du kannst deine Spiele durch die Methode auch gleich auf dem PC dumpen und somit Archivieren. 

---

:ladder: **Schritte im Detail:**

:one: **In OFW Spiele & Updates installieren**  
- In die normale Firmware (SysNAND) booten  
- Wunschspiele + Updates ganz normal installieren

:two: **Neue emuMMC erstellen**  
- Hekate → Close → `emuMMC` → `Create emuMMC`  
- **SD File** wählen (**KEINE Partition!**)  
- Beispiel: es wird `/emuMMC/SD00/` erstellt

:three: **Nintendo-Ordner kopieren**  
- SD-Karte in den PC stecken  
- Den ganzen `Nintendo`-Ordner vom SD-Hauptverzeichnis kopieren nach:  
  ➤ `emuMMC/SD00/Nintendo`  
  (je nachdem wie deine emuMMC heißt – `SD01`, `SD02` usw.)

:four: **In die neue emuMMC wechseln**  
- Hekate → Close → `emuMMC` → `Change emuMMC`  
- Deine neue SD-emuMMC auswählen
(je nachdem wie deine emuMMC heißt – SD01, SD02 usw.)

:five: **In die neue emuMMC booten**

---

:small_orange_diamond: **Bei Linkalho:**  
:octagonal_sign: **Den Original-Account NICHT durch einen Fake-Account ersetzen!**  
→ Wenn du mit einem echten Account heruntergeladen hast, **darfst du ihn nicht löschen oder durch Linkalho ersetzen**,  
→ sonst fehlen die Lizenzen – und **DBI kann die Spiele NICHT dumpen!**

---

:six: **DBI starten & MTP verwenden**  
:pushpin: *Falls du DBI noch nie genutzt hast:*

➤ **So startest du DBI via Title Override:**  
- Halte **R-Taste** gedrückt und starte ein Spiel > Andererseits kannst auch über das Album ein Forwarder installieren da nach all dem gantrn löscst du den **Ersatz emuMMC**
- Du landest im Homebrew-Menü → DBI starten

> ⚠️ **Hinweis:**  
>**Jetzt wichtig:**  
>Für **Cartridge Game Updates** muss das Cartridge Game **vorher über DBI oder Sphaira installiert** werden,  
>sodass die Updates dann unter `SD Install` angezeigt werden. 

>➡️ Anleitung: [Spiele von Gamecards installieren](https://docs.niklascfw.de/switch/gut-zu-wissen/spiele/spiele_installation_dbi_sphaira/#dbi)

1. Starte anschließend "MTP Responder".  
2. Verbinde deine Switch per USB mit dem PC  
3. Am PC erscheint sie wie ein USB-Stick

:floppy_disk: Öffne den Ordner `Installed Games` → dort Findest du Ordner zu den Spielen (Spiele + Updates). Diese kannst du die  ganz einfach auf deinen PC kopieren!

---

:seven: **Zurück zur Ziel-emuMMC**  
- Wieder `Change emuMMC` in Hekate → wähle den emuMMC, für den du das alles gemacht hast. 
- Boot in diesen emuMMC  
- Öffne DBI  
- Starte den MTP Responder  
- Diesmal → `SD Install` auswählen  
  → Spiele & Updates auf deiner SD installieren

---

:white_check_mark: **Fertig!**  
Deine Spiele + Updates sind in der emuMMC drin  
Saves bleiben erhalten, alles sauber übertragen
