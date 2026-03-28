# Spielstände sichern und wiederherstellen mit JKSV

**JKSV** ist ein Homebrew-Tool für die Switch, mit dem man **Speicherstände** (Savegames) **sichern**, **wiederherstellen** und **verwalten** kann.

## Funktionen

- 📂 **Backup von Speicherständen**  
  Du kannst Spielstände von deiner Switch auf die SD-Karte sichern, um sie später wieder einzuspielen.
- 🔄 **Wiederherstellen & Transfer**  
  Gesicherte Spielstände können einfach wiederhergestellt oder auf eine andere Switch mit CFW übertragen werden.
- 🧩 **Unterstützt mehrere Benutzer & Spiele**  
  Das Tool erkennt alle Benutzerkonten auf der Konsole und zeigt die dazugehörigen Saves an.

---

## Spielstände sichern

1. Starte deine Switch in CFW.
2. Öffne das Homebrew Menu (z. B. **R** gedrückt halten und ein beliebiges Spiel starten – am besten erstellst du dir einen Forwarder).
3. Wähle **JKSV** aus der App-Liste.
4. Im JKSV-Menü:
   - Wähle dein Benutzerprofil.
   - Wähle das Spiel aus, dessen Speicherstand du sichern willst.
   - Drücke **Y** für *Backup*.
5. Vergib einen Namen (z. B. mit Datum: `Zelda_2025-08-11`).
6. Fertig – der Save liegt jetzt auf deiner SD-Karte unter:  
   `/JKSV/[Spielname]/[Backupname]/`

---

## Speicherstände wiederherstellen

1. Starte deine Switch in CFW.
2. Öffne das Homebrew Menu (z. B. **R** gedrückt halten und ein beliebiges Spiel starten – am besten erstellst du dir einen Forwarder).
3. Wähle **JKSV** aus der App-Liste.
4. Im JKSV-Menü:
   - Wähle dein Benutzerprofil → Spiel → Backup-Ordner.
5. Drücke **X** für *Restore*.
6. Bestätigen → Save wird ins System kopiert.

---


> 💡 **Hinweis:** **Regelmäßig sichern** – besonders vor Modding oder Experimenten.