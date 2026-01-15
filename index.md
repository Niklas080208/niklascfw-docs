---
visibility: hidden
---

# Willkommen bei den NiklasCFW Docs

---

## 📚 Was findest du hier?

Diese Dokumentation bietet dir **alles**, was du für die Einrichtung und Nutzung von Custom Firmware auf der Nintendo Switch benötigst:

### 🚀 **Schnellstart**
- ✅ **[Switch Modell prüfen](/Switch/vorbereitung/switch_ungepatcht_check)** - Ist deine Switch modbar?
- ✅ **[SD-Karte vorbereiten](/Switch/vorbereitung/richtige_sd)** - Die richtige Ausstattung
- ✅ **[CFW Installation](/Switch/erweiterte-guides/switch_v1_softmod_guide)** - Der Hauptguide

### 🛠️ **Erweiterte Features**
- 🎯 **[NiklasCFW Pack](/Switch/niklascfw-pack/)** - Alles-in-einem Paket
- 💾 **[NAND Backup](/Switch/system-backup/nand_backup)** - Sicherheit zuerst!
- 🎨 **[Themes & Customization](/Switch/gut-zu-wissen/customization/theme_install)** - Switch individuell gestalten
- 🎮 **[Game Installation](/Switch/gut-zu-wissen/)**
- 🔧 **[RetroArch Setup](/Switch/gut-zu-wissen/erweiterte-systeme/retroarch_install)**

### 🆘 **Support & Troubleshooting**
- 🔧 **[Fehlerbehebung](/Switch/fehlerbehebung/)** - Häufige Probleme lösen
- 📱 **[Serialchecker](https://serialcheck.niklascfw.de)** - Online Tool
- 💬 **[Discord Community](https://discord.gg/niklascfw)** - Hilfe von anderen Nutzern

---

## ⚠️ **Wichtige Hinweise**

<div style="background: #fff3cd; border: 2px solid #ffc107; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #b8860b;">⚠️ Bevor du startest</h4>
<ul style="margin-bottom: 0;">
<li>📖 <strong>Lies ALLE Anleitungen</strong> vollständig durch</li>
<li>💾 <strong>Erstelle IMMER ein NAND Backup</strong> vor Modifikationen</li>
<li>🎯 <strong>Verwende nur aktuelle Versionen</strong> aller Tools</li>
<li>🚫 <strong>Nutze niemals exFAT</strong> - nur FAT32!</li>
</ul>
</div>

<div style="background: #d1ecf1; border: 2px solid #17a2b8; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #17a2b8;">⚖️ Rechtliches</h4>
<ul style="margin-bottom: 0;">
<li>Diese Guides sind nur für <strong>Bildungszwecke</strong></li>
<li><strong>Du</strong> trägst die Verantwortung für deine Konsole</li>
<li><strong>Garantieverlust</strong> ist möglich</li>
</ul>
</div>

---

## 🎯 **Schnellzugriff nach Gerät**

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem; margin: 2rem 0;">

<div style="border: 2px solid #28a745; border-radius: 8px; padding: 1rem; text-align: center;">
<h3>🎮 Switch V1 (2017-2018)</h3>
<p><strong>✅ Vollständig modbar</strong></p>
<p>RCM + Softmod möglich</p>
<a href="/Switch/switch_v1_softmod_guide" style="background: #28a745; color: white; padding: 0.5rem 1rem; border-radius: 4px; text-decoration: none;">→ Guide starten</a>
</div>

<div style="border: 2px solid #dc3545; border-radius: 8px; padding: 1rem; text-align: center;">
<h3>🎮 Switch V2/OLED/Lite</h3>
<p><strong>❌ Nicht modbar</strong></p>
<p>Hardmod erforderlich</p>
<a href="/Switch/vorbereitung/switch_ungepatcht_check" style="background: #dc3545; color: white; padding: 0.5rem 1rem; border-radius: 4px; text-decoration: none;">→ Prüfen</a>
</div>

</div>

---

## 📈 **Empfohlener Installations-Ablauf**

```mermaid
graph TD
    Start([🎮 Start]) --> Check[🔍 Switch V1?]
    Check -->|✅ Ja| Serial[📋 Serial prüfen]
    Check -->|❌ Nein| Modchip[🔧 Modchip einbau]
    
    Serial -->|✅ Modbar| RCM[⚡ RCM Setup]
    Serial -->|🟨 50/50| RCMTest[🧪 RCM Test]
    Serial -->|❌ Gepatcht| Modchip
    
    RCMTest -->|✅ Funktioniert| RCM
    RCMTest -->|❌ Funktioniert nicht| Modchip
    
    Modchip --> SD[💾 SD FAT32]
    
    RCM --> SD
    SD --> CFW[🚀 CFW installieren]
    CFW --> Backup[💾 NAND Backup]
    Backup --> Pack[🎯 NiklasCFW Pack]
    Pack --> Done([🎉 Fertig!])
    
    style Start fill:#e1f5fe
    style Done fill:#e8f5e8
    style Modchip fill:#ffc107
    style RCMTest fill:#fff3e0
    style Backup fill:#fff3e0
```

---

## 🔗 **Nützliche Links**

| Tool | Beschreibung | Link |
|------|-------------|------|
| 🔍 **Serialchecker** | Prüfe deine Switch | [serialcheck.niklascfw.de](https://serialcheck.niklascfw.de) |
| 📺 **YouTube** | Video-Tutorials | [@NiklasCFW](https://youtube.com/@NiklasCFW) |
| 💬 **Discord** | Community Support | [discord.gg/niklascfw](https://discord.gg/niklascfw) |
| 📱 **GitHub** | Source Code | [NiklasCFW Pack GitHub Repo](https://github.com/Woody-NX/NiklasCFW_Pack) |

---

## 🆕 **Was ist neu?**

<div style="background: #d4edda; border: 2px solid #28a745; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #28a745;">💡 Aktuelle Updates</h4>
<ul style="margin-bottom: 0;">
<li>✨ <strong>Komplett überarbeitete Struktur</strong> mit besserer Navigation</li>
<li>🎯 <strong>NiklasCFW Pack</strong> - Alles-in-einem Paket</li>
<li>📱 <strong>Mobile-optimierte</strong> Darstellung</li>
<li>🔄 <strong>Regelmäßige Updates</strong> für neue Firmware-Versionen</li>
</ul>
</div>

---

<div style="text-align: center; margin: 3rem 0; padding: 2rem; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); border-radius: 12px; color: white;">
  <h2 style="margin-bottom: 1rem;">🚀 Bereit loszulegen?</h2>
  <p style="font-size: 1.1em; margin-bottom: 1.5rem;">Starte jetzt mit der Modifikation deiner Nintendo Switch!</p>
  <a href="/Switch/" style="background: white; color: #667eea; padding: 1rem 2rem; border-radius: 6px; text-decoration: none; font-weight: bold; font-size: 1.1em;">📖 Zur Dokumentation →</a>
</div> 

Test

