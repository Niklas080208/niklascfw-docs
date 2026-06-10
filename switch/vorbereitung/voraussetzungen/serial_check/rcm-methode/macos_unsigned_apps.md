# Unsigned Apps auf macOS Sequoia und neuer öffnen

Ab **macOS Sequoia (15)** reicht der alte Rechtsklick-Workaround oft nicht mehr aus.

---

## Methode 1: Terminal

Nutze im Terminal:

```bash
xattr -cr ./MyApp.app
```

Ersetze `MyApp.app` durch den Namen der betroffenen App (z. B. `CrystalRCM.app`).

---

## Methode 2: Systemeinstellungen

>>> App normal starten
App normal starten und den Fehlerdialog abwarten.
![|460x265](/images/switch/vorbereitung/rcm/sequoia/not-opened.png)

>>> Datenschutz & Sicherheit öffnen
Öffne **Systemeinstellungen -> Datenschutz & Sicherheit**.
![|620x372](/images/switch/vorbereitung/rcm/sequoia/privacy-security.png)

>>> Dennoch öffnen
Scrolle nach unten und klicke bei der App auf **Dennoch öffnen**.
![|460x265](/images/switch/vorbereitung/rcm/sequoia/open-anyway.png)

>>> Mit Admin-Rechten bestätigen
Bestätige den Vorgang mit Admin-Rechten.
![|460x265](/images/switch/vorbereitung/rcm/sequoia/authenticate.png)

>>> App erneut starten
App erneut starten.
>>>

---

## Hinweis

Nach dem ersten erfolgreichen Start lässt sich die App in der Regel wieder normal öffnen.

---

## Credits

- Textquelle: [Open unsigned applications on macOS Sequoia and newer](https://wiki.hacks.guide/wiki/Open_unsigned_applications_on_macOS_Sequoia_and_newer)
