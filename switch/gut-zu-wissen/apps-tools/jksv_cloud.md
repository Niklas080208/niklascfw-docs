---
icon: cloud
label: "JKSV Cloud"
order: 104
description: "JKSV-Spielstände nach Google Drive oder WebDAV sichern."
---

# JKSV Cloud Backup einrichten

JKSV kann Speicherstände direkt auf **Google Drive** oder einen **WebDAV-Server** hochladen.

![JKSV Start|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_start.jpg)

---

## Voraussetzungen

{.list-icon}
- Internetzugang auf der Switch
- :icon-cloud: Cloud-Dienst (Google Drive, Nextcloud, …)
- :icon-package: **JKSV v13/09/2025** oder neuer

---

+++ Google Drive
## Google Drive vorbereiten (PC)

>>> Google Cloud Projekt
[Google Cloud Console](https://console.cloud.google.com/welcome/new) → **Projekt auswählen** → **Neues Projekt** (`JKSV`).

![Google Cloud Projekt|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud.png)
![Neues Projekt|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud2.png)

Projektname **JKSV**, Speicherort leer lassen → erstellen.

![Projekt erstellen|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud3.png)

>>> Google Drive API aktivieren
**APIs und Dienste → Aktivierte APIs** → **Google Drive API** aktivieren (ggf. unter **Bibliothek** suchen).

![Drive API|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud5.jpg)

>>> OAuth einrichten
**Anmeldedaten → Zustimmungsbildschirm** – Anwendungsname `JKSV`, Zielgruppe **Extern**, Kontakt-E-Mail, Richtlinien akzeptieren.

![OAuth Schritte|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud4.png)
![Zustimmungsbildschirm|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud6.png)

>>> OAuth-Client erstellen
**Clients → Client erstellen** → Typ **Fernsehgeräte und Geräte mit begrenzter Eingabe**, Name z. B. `nxJKSV`.

![Client erstellen|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud7.png)

JSON herunterladen und umbenennen in **`client_secret.json`**.

![client_secret.json|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud8.jpeg)

!!!danger JSON nur einmal sichtbar
Die `client_secret.json` kann oft **nur einmal** angezeigt werden – sofort speichern.
!!!

>>> Testnutzer hinzufügen
**OAuth-Zustimmungsbildschirm → Zielgruppe → + Add users** → eigene E-Mail als Testnutzer.

![Testnutzer|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud10.png)

## Switch (Google Drive)

>>> client_secret auf SD
`client_secret.json` nach `sd:/config/JKSV/` kopieren.

>>> JKSV anmelden
**JKSV** starten → Anmeldecode und Link [google.com/device](https://google.com/device) am PC/Smartphone eingeben.

![JKSV Google Anmeldung|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_start2.jpg)

!!!info Speicherort in Drive
JKSV legt automatisch einen Ordner **`JKSV`** an – der Pfad ist nicht änderbar.
!!!
>>>

+++ WebDAV (Nextcloud)
## Server vorbereiten

>>> WebDAV aktivieren
Cloud-Server (z. B. **Nextcloud**) mit **WebDAV**. Optional eigener User (z. B. `nxsaver`).

>>> App-Passwort (bei 2FA)
In den Sicherheitseinstellungen ein **App-Passwort** erzeugen.

>>> Zielordner
In der Cloud z. B. `JKSV_SAVES` anlegen.

## Switch (WebDAV)

>>> webdav.json erstellen
Am PC `webdav.json` mit z. B.:

```json
{
  "origin": "https://cloud.deinedomain.de",
  "basepath": "remote.php/dav/files/nxsaver/JKSV_SAVES",
  "username": "nxsaver",
  "password": "DEIN-APP-PASSWORT"
}
```

!!!warning Kein extra `/` in origin/basepath
Zusätzliche Slashes am Ende von `origin` oder `basepath` brechen die Verbindung.
!!!

>>> webdav.json auf SD
Datei nach `sd:/config/JKSV/` kopieren, **JKSV** starten → **„WebDAV erfolgreich gestartet!“**
+++

---

## Automatischer Upload

!!!tip Nach der Einrichtung
In JKSV aktivieren:

- **Backups automatisch benennen:** Ein
- **Backups automatisch im Remote-Speicher hochladen:** Ein

Bestehende lokale Backups ggf. manuell in den Cloud-Ordner **`JKSV`** verschieben.
!!!
