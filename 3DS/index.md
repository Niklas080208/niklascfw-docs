# Nintendo 3DS CFW Dokumentation

<div style="text-align: center; margin: 2rem 0;">
  <img src="/assets/3ds.png" alt="Nintendo 3DS" style="max-width: 200px; margin-bottom: 1rem;">
  <p style="font-size: 1.2em; color: #666;">Komplette Anleitung für Custom Firmware auf dem 3DS</p>
</div>

---

## 🚀 **Schnellstart-Guide**

<div style="background: #e8f5e8; border: 2px solid #28a745; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #28a745;">💡 Neu hier? Starte hier!</h4>
<p style="margin-bottom: 0;">Folge diesem <strong>linearen Pfad</strong> für die beste Erfahrung:</p>
</div>

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1rem; margin: 2rem 0;">

<div style="border: 2px solid #007bff; border-radius: 8px; padding: 1.5rem;">
<h3>🔍 1. Vorbereitung</h3>
<p>3DS prüfen & SD-Karte vorbereiten</p>
<ul style="margin: 1rem 0;">
<li>✅ <a href="vorbereitung/3ds_modell_herausfinden">3DS Modell herausfinden</a></li>
<li>📀 <a href="vorbereitung/firmware_pruefen">3DS Firmware Version prüfen</a></li>
<li>💾 <a href="vorbereitung/sd_formatieren">SD Karte richtig formatieren (FAT32)</a></li>
<li>⚡ <a href="vorbereitung/mset9_exploit_einrichten">MSET9 Exploit einrichten</a></li>
</ul>
</div>

<div style="border: 2px solid #28a745; border-radius: 8px; padding: 1.5rem;">
<h3>🛠️ 2. Installation</h3>
<p>Custom Firmware installieren</p>
<ul style="margin: 1rem 0;">
<li>🎯 <a href="installation/safeb9sinstaller_starten">SafeB9SInstaller starten</a></li>
<li>💾 <a href="installation/boot9strap_installieren">boot9strap installieren</a></li>
<li>📦 <a href="installation/luma3ds_konfiguration">Luma3DS konfigurieren</a></li>
</ul>
</div>

<div style="border: 2px solid #ffc107; border-radius: 8px; padding: 1.5rem;">
<h3>⚙️ 3. Nach der Installation</h3>
<p>CFW abschließen & absichern</p>
<ul style="margin: 1rem 0;">
<li>🚀 <a href="nachher/mset9_entfernen">MSET9 entfernen</a></li>
<li>📱 <a href="nachher/godmode9_backup_erstellen">NAND Backup mit GodMode9</a></li>
<li>🎨 <a href="nachher/homebrew_installieren">Homebrew & Apps installieren</a></li>
</ul>
</div>

</div>

---

## ⚠️ **Wichtige Sicherheitshinweise**

<div style="background: #f8d7da; border: 2px solid #dc3545; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #dc3545;">🚨 KRITISCH - Lies das ZUERST!</h4>
<ul style="margin-bottom: 0;">
<li>💾 <strong>NAND Backup ist PFLICHT</strong> – Ohne Backup hohes Brick-Risiko</li>
<li>🚫 <strong>Nur FAT32 verwenden</strong> – exFAT wird NICHT unterstützt</li>
<li>🔄 <strong>Immer aktuelle Luma3DS Version</strong> verwenden</li>
<li>❌ <strong>Keine fremden Tutorials mischen</strong></li>
</ul>
</div>

<div style="background: #fff3cd; border: 2px solid #ffc107; border-radius: 8px; padding: 1.5rem; margin: 1rem 0; color: #212529;">
<h4 style="margin-top: 0; color: #b8860b;">⚖️ Rechtliche Hinweise</h4>
<ul style="margin-bottom: 0;">
<li>📖 Nur für <strong>Bildungszwecke</strong></li>
<li>⚖️ <strong>Homebrew ≠ Piraterie</strong></li>
<li>🛡️ Modifikation kann <strong>Garantieverlust</strong> bedeuten </li>
<li>🎮 Online-Funktionen können eingeschränkt werden</li>
</ul>
</div>

---

## 🎯 **Empfohlener Installations-Ablauf**

```mermaid
graph TD
    Start([🎮 Start]) --> Check[🔍 3DS Modell prüfen]
    Check --> Prep[MSET9 Exploit vorbereiten]
    Prep --> Install[🚀 SafeB9SInstaller starten]
    Install --> B9S[boot9strap installieren]
    B9S --> Luma[Luma3DS konfigurieren]
    Luma --> Remove[MSET9 entfernen]
    Remove --> Backup[💾 NAND Backup]
    Backup --> Done([🎉 Fertig!])

    style Start fill:#e1f5fe
    style Done fill:#e8f5e8
    style Backup fill:#fff3cd
