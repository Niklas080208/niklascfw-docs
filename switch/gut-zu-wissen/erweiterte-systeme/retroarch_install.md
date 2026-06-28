# RetroArch installieren

![|700x420](/images/switch/allgemein/retroarch_logo.png)

**RetroArch** ist eine sogenannte Frontend-Anwendung für **Emulatoren**, Spiel-Engines und Mediaplayer. Auf der Nintendo Switch startest du damit klassische Konsolen als Homebrew.

---

## Voraussetzungen {#voraussetzungen}

!!!warning Uhrzeit synchronisieren
**Bitte darauf achten, dass deine Uhrzeit synchronisiert ist.**  
Ansonsten funktioniert der Download über UltraHand nicht!
!!!

[!ref text="Uhrzeit mit DBI synchronisieren (NTP)"](../../nachher/dbi_time)

---

## Installation {#installation}

>>> UltraHand öffnen
**UltraHand** starten (L, R und Plus gleichzeitig) und **NiklasCFW Downloader** öffnen.

![|700x420](/images/switch/allgemein/lakka1.jpg)

>>> RetroArch auswählen
Runterscrollen und **RetroArch** auswählen.

![|700x420](/images/switch/allgemein/retroarch1.jpg)

>>> Download starten
Auf **RetroArch** tippen und den Download starten (⬇️ Download läuft, ⬆️ Entpacken läuft).

![|700x420](/images/switch/allgemein/retroarch2.jpg)

RetroArch ist danach installiert. Als Nächstes den **Forwarder** einrichten (siehe unten).

>>> RetroArch herunterladen
Aktuelle Version für die Switch laden:

[!button variant="primary" text="RetroArch Switch Download" icon="download" target="blank"](https://buildbot.libretro.com/stable/1.21.0/nintendo/switch/libnx/RetroArch.7z)

>>> Auf die SD-Karte kopieren
**RetroArch.7z** entpacken und den Inhalt in das **Root** der microSD legen.

>>> In die CFW booten
In die **CFW** starten und den **RetroArch Forwarder** mit Sphaira anlegen (siehe nächster Abschnitt).
+++
>>>
---

## RetroArch Forwarder einrichten {#forwarder}

RetroArch muss im **Highmemory-Mode (Title Override)** laufen. Am einfachsten erreichst du das mit einem **Forwarder auf dem Homescreen**.

>>> Sphaira öffnen
**Sphaira** starten und **RetroArch** in der App-Liste suchen.

>>> Forwarder erstellen
**X-Taste** auf RetroArch drücken und **Forwarder installieren** wählen.

![RetroArch in Sphaira auswählen und X Optionen drücken|700x420](/images/switch/gut-zu-wissen/erweiterte-systeme/retroarch-forwarder.gif)

Der Forwarder erscheint danach auf dem **Homescreen** und startet RetroArch immer mit vollem RAM.

!!!tip Warum ein Forwarder?
Startest du Homebrew über das Album-Symbol, läuft Sphaira im **Applet-Modus** ohne genug Ressourcen. Ein Forwarder umgeht das, weil die Switch denkt, du startest ein Spiel.
!!!
>>>

[!ref text="Forwarder installieren (Sphaira-Anleitung)"](../../nachher/forwarder_installieren)

---

## ROMs hinzufügen {#roms}

>>> Ordner anlegen
Im **Root** der microSD einen Ordner `roms` erstellen.

>>> System-Unterordner
Für jedes System einen passenden Unterordner anlegen, zum Beispiel:

{.list-icon}
- :icon-file-directory: **n64** für Nintendo 64
- :icon-file-directory: **snes** für SNES
- :icon-file-directory: **gba** für Game Boy Advance

>>> ROMs ablegen
Die ROM-Dateien in die jeweiligen Unterordner kopieren.

!!!info Nur legal nutzen
Nutze nur ROMs, für die du eine Lizenz oder das Originalspiel besitzt. Wir geben **keine Hilfe bei Piracy**!
!!!
>>>

---

## Weitere Einstellungen {#einstellungen}

Feintuning der einzelnen Emulatoren findest du auf der [RetroArch Homepage](https://www.retroarch.com/).
