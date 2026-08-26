---
icon: shield-check
label: "Nintendo-Server"
order: 180
description: "OmniNX blockiert Kommunikation zu Nintendo-Servern standardmäßig über DNS-MitM."
---

# Sind Nintendo-Server blockiert?

**Ja.** Sobald OmniNX auf der SD liegt und du in die **CFW** (emuMMC) bootest, ist die Kommunikation zu Nintendo-Servern **standardmäßig unterdrückt**. Du musst kein extra DNS, 90DNS oder ähnliche Blocker einrichten.

---

## Was ist bereits aktiv?

OmniNX bringt **DNS-MitM** (Atmosphere-Hosts) in **allen Varianten** mit: Light, Standard und OC. Damit werden Nintendo-Adressen in der CFW abgefangen, bevor eine Verbindung zustande kommt.

!!!success Pack drauf = Blockade aktiv
Die typische Frage: *„Wenn ich das Pack herunterlade und auf die Switch lege, ist die Kommunikation mit Nintendo-Servern dann verhindert?“*  
**Ja**, in der CFW. Dafür ist nichts zusätzlich zu konfigurieren.
!!!

Die Blockade gilt **nur in der CFW**. In der **OFW** (unmodifiziertes Originalsystem) erreichst du Nintendo-Dienste weiterhin, sofern dein SysNAND sauber ist. Siehe [emuMMC erstellen](/switch/vorbereitung/emummc_erstellen).

---

## Prüfen, ob es greift

1. In die **CFW (emuMMC)** booten.
2. **Sphaira** öffnen (Album).
3. **DNS_mitm Tester** starten.
4. Alle Nintendo-Einträge sollten als **blockiert** gemeldet werden.

Der Tester ist in jeder OmniNX-Variante enthalten.

---

## Was nicht blockiert wird

- **Homebrew** mit eigenem Online-Zugang (Downloader, JKSV Cloud, AppStores, …).
- **Server von Drittentwickler-Spielen** mit eigenem Online-Modus.
- Die **OFW**: dort erreichst du eShop, Updates und Nintendo-Online – z. B. zum Herunterladen, bevor du Inhalte in der CFW nutzt. Siehe [Sphaira: OFW-Dumps](/switch/gut-zu-wissen/spiele/sphaira_games_und_updates_aus_der_ofw_dumpen).

---

## Uhrzeit

Weil die Switch die Zeit nicht mehr über Nintendo holen kann, musst du sie selbst setzen: zuerst in **Hekate**, danach per **QuickNTP**. Anleitung: [Uhrzeit synchronisieren](/switch/nachher/time_sync).
