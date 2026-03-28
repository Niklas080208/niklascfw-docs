# 🔍 Vorbereitung

Bevor du mit der Installation von Custom Firmware auf deiner Nintendo Switch beginnst, musst du einige wichtige Vorbereitungsschritte durchführen. Diese Checkliste führt dich Schritt für Schritt durch alles, was vor der eigentlichen CFW-Installation wichtig ist.

---

## 📋 Vorbereitungs-Checkliste

### 1️⃣ **Switch Modell prüfen**
- 🔍 [Switch Modell prüfen](switch_ungepatcht_check) - Ist deine Switch modbar?
- ⚠️ Nur **ungepatchte Switch V1** (2017-2018) können per Softmod modifiziert werden
- 🎮 Switch V2, OLED und Lite benötigen einen Hardmod (Modchip)

### 2️⃣ **SD-Karte vorbereiten**
- 💾 [Richtige SD-Karte](richtige_sd) - Welche Speicherkarte ist die beste Wahl?
- 🔧 [SD auf FAT32 formatieren](sd_format) - FAT32 ist **Pflicht** für CFW!

### 3️⃣ **RCM-Methode einrichten**
- ⚡ [RCM Methode](rcm-methode/) - Anleitungen für Windows, macOS und Linux
- 🎯 RCM ist der Standardweg für ungepatchte Switch V1 Konsolen

---

## 🎯 **Empfohlene Reihenfolge**

```mermaid
graph LR
    A[🔍 Switch prüfen] --> B{✅ Modbar?}
    B -->|Ja| C[💾 SD-Karte wählen]
    B -->|Nein| D[❌ Hardmod nötig]
    C --> E[🔧 SD formatieren]
    E --> F[⚡ RCM einrichten]
    F --> G[🚀 CFW installieren]
```

---

## ⚠️ **Wichtige Hinweise**

<div style="background: #fff3cd; border: 2px solid #ffc107; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #b8860b;">💡 Bevor du startest</h4>
<ul style="margin-bottom: 0;">
<li>📖 <strong>Lies alle Anleitungen</strong> vollständig durch</li>
<li>💾 <strong>FAT32 ist Pflicht</strong> - exFAT funktioniert nicht!</li>
<li>🎯 <strong>Qualität der SD-Karte</strong> ist entscheidend für Performance</li>
<li>⚡ <strong>RCM-Jig vorsichtig</strong> verwenden - nicht dauerhaft stecken lassen</li>
</ul>
</div>

<div style="background: #f8d7da; border: 2px solid #dc3545; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #dc3545;">🚨 Kritisch</h4>
<ul style="margin-bottom: 0;">
<li>🚫 <strong>Niemals exFAT verwenden</strong> - nur FAT32!</li>
<li>🔋 <strong>Akku-Stand</strong> - mindestens 50% vor Start</li>
<li>💾 <strong>Backup vorhanden?</strong> - Wichtig für später!</li>
</ul>
</div>

---

## 📚 **Weiterführende Links**

Nach der Vorbereitung kannst du mit der eigentlichen CFW-Installation beginnen:

- 🚀 [CFW Installation](/switch/erweiterte-guides/switch_v1_softmod_guide) - Der Hauptguide
- 💾 [NAND Backup](/switch/system-backup/nand_backup) - Sicherheit zuerst!
- 🎯 [NiklasCFW Pack](/switch/niklascfw-pack/guide1.4.0) - Alles-in-einem Paket

---

<div style="text-align: center; margin: 2rem 0; padding: 1.5rem; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 12px; color: white;">
  <h3>✅ Bereit?</h3>
  <p style="margin: 1rem 0;">Wenn alle Vorbereitungsschritte abgeschlossen sind, kannst du mit der CFW-Installation beginnen!</p>
  <a href="/switch/erweiterte-guides/switch_v1_softmod_guide" style="background: white; color: #667eea; padding: 0.8rem 1.5rem; border-radius: 6px; text-decoration: none; font-weight: bold;">🚀 CFW Installation starten →</a>
</div>

