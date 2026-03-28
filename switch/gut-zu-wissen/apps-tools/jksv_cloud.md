---
icon: cloud
label: "JKSV Cloud"
order: 104
---

# JKSV Cloud Backup einrichten

JKSV bietet eine Funktion, mit der ihr Speicherdaten der JKSV-Homebrew-App direkt auf **Google Drive** oder einem **WebDAV-Server** sichern könnt. Die Einrichtung dieser Funktion wird im Folgenden detailliert beschrieben.
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_start.jpg)

---

## 📋 Voraussetzungen

- Internetzugang  
- Clouddienst (z. B. Google Drive, Nextcloud, ...)  
- JKSV **v13/09/2025** oder neuer  

---

## ☁️ Option 1: Google Drive

### 🔧 Google Drive vorbereiten

1. Gehe auf die Website: [https://console.cloud.google.com/welcome/new](https://console.cloud.google.com/welcome/new)
2. Erstelle ein neues Projekt über **„Projekt auswählen“ → „Neues Projekt“**

![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud.png)
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud2.png)
   - Projektnamen: `JKSV`  
   - Speicherort/Organisation: leer lassen  
   
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud3.png)
3. Klicke auf das **Benachrichtigungssymbol** und warte, bis das Projekt erstellt ist.  
   Anschließend sollte statt „Projekt auswählen“ nun **„JKSV“** angezeigt werden.
4. Öffne das Menü **„APIs und Dienste → Aktivierte APIs und Dienste“**.  
   Scrolle bis **„Google Workspace“** und wähle **„Google Drive API“**.  
   > 💡 Falls nicht sichtbar, findest du es unter **„Bibliothek“ → „APIs und Dienste“**.
5. Aktiviere **Google Drive API**.

![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud5.jpg)
6. Gehe zu **„Anmeldedaten → Zustimmungsbildschirm konfigurieren → Erste Schritte“**
7. Fülle das Formular aus:
   - Anwendungsname: `JKSV`
   - Zielgruppe: **Extern**
   - Kontaktdaten: deine eigene Mailadresse  
   - Akzeptiere die Nutzerrichtlinien und klicke **„Erstellen“**
   
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud4.png)
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud6.png)
8. Gehe zu **„Clients“ → „Client erstellen“**
   - Anwendungstyp: **Fernsehgeräte und Geräte mit begrenzter Eingabe**
   - Name: z. B. `nxJKSV`
   - Erstellen klicken  
   
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud7.png)
   > **Alternativ:** *APIs und Dienste → Anmeldedaten → Anmeldedaten erstellen → OAuth-Client-ID*
9. Lade die erstellte JSON-Datei herunter und benenne sie um in:  
   **`client_secret.json`**
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud8.jpeg)
   > 💡 Die `client_secret.json` Datei kann man sich nur einmal anzeigen lassen und muss direkt abgespeichert werden!
10. Füge dich selbst als Testnutzer hinzu:  
    - Menü: **„APIs und Dienste → OAuth-Zustimmungsbildschirm → Zielgruppe“**  
    - **„+ Add users“** → eigene Mailadresse eintragen  
    - Stelle sicher, dass sie unter „Testnutzer“ angezeigt wird
    
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_cloud10.png)

---

### 🎮 Nintendo Switch vorbereiten

1. Kopiere die Datei **`client_secret.json`** auf deine SD-Karte nach:  
   ```
   sd:/config/JKSV
   ```
2. Starte **JKSV** auf deiner Switch.  
3. Auf dem Bildschirm erscheint nun eine Anmeldeaufforderung mit einem Code und Link:  
   👉 [https://google.com/device](https://google.com/device)  
4. Öffne den Link am PC oder Smartphone und gib den angezeigten Code ein, um dein Gerät zu aktivieren.
5. Nach erfolgreicher Anmeldung zeigt JKSV beim nächsten Start:  
   **„Erfolgreich bei Google Drive angemeldet!“**
![|700x420](/images/switch/gut-zu-wissen/apps-tools/jksv/jksv_start2.jpg)

> ⚠️ **Hinweis:**  
> Der Speicherort im Google Drive kann **nicht geändert** werden.  
> JKSV legt automatisch einen Ordner **`JKSV`** als Zielverzeichnis an.

---

## 🌐 Option 2: WebDAV (Beispiel: Nextcloud)

### 🖥️ Cloud-Server vorbereiten

1. Richte einen Cloudserver (z. B. **Nextcloud**) ein und stelle sicher, dass **WebDAV aktiviert** ist.
2. Optional: Lege einen eigenen Benutzer für die Switch an (z. B. `nxsaver`).
3. Wenn du **2FA** aktiviert hast, erstelle in den Sicherheitseinstellungen ein **App-Passwort**,  
   z. B.:  
   ```
   nqQYw-Ln6kt-Zs3f5-qyYhw-P1WIR
   ```
4. Lege in deiner Cloud ein Verzeichnis an, z. B. `JKSV_SAVES`, in dem die Spielstände gespeichert werden sollen.

---

### 🎮 Nintendo Switch vorbereiten

1. Ermittle die WebDAV-Adresse deines Cloudservers, z. B.:  
   ```
   https://cloud.deinedomain.de/remote.php/dav/files/nxsaver
   ```
2. Erstelle am PC eine Datei namens **`webdav.json`** mit folgendem Inhalt (Beispiel):

   ```json
   {
     "origin": "https://cloud.deinedomain.de",
     "basepath": "remote.php/dav/files/nxsaver/JKSV_SAVES",
     "username": "nxsaver",
     "password": "nqQYw-Ln6kt-Zs3f5-qyYhw-P1WIR"
   }
   ```

   > ⚠️ **Wichtig:**  
   > Achte darauf, dass du **kein zusätzliches „/“** bei `origin` oder `basepath` setzt,  
   > sonst funktioniert die Verbindung nicht korrekt.

3. Kopiere die Datei **`webdav.json`** auf deine SD-Karte nach:  
   ```
   sd:/config/JKSV
   ```
4. Starte **JKSV**.  
   Wenn alles korrekt ist, erscheint die Meldung:  
   **„WebDAV erfolgreich gestartet!“**



> ⚠️ **Wenn ihr fertig seid.**  
> Backups Automatisch benennen auf **Ein**.  
> Backups automatisch im Remote-Speicher hochladen: **Ein**.
> Somit habt ihr beim erstellen von Backups alle direkt in der Cloud

> ⚠️ **Hinweis:**  
> Alle bisherigen Backups müssen manuell in den automatisch angelegten **`JKSV`** Ordner in der gewählten Cloud variante gelegt werden.  


