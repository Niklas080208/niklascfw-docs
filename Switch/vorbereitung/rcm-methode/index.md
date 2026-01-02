# RCM Methode - Einführung

Die **RCM-Methode (Recovery Mode)** ist der Standardweg, um Custom Firmware auf einer ungepatchten Nintendo Switch V1 zu installieren. Sie nutzt eine Schwachstelle im Boot-Prozess der Switch, um einen Payload (wie Hekate) direkt zu starten.

## 🎯 Was ist RCM?

RCM steht für **Recovery Mode** - ein spezieller Boot-Modus der Nintendo Switch, der normalerweise für Reparaturen und Updates verwendet wird. Durch diese Methode können wir den Boot-Prozess umgehen und direkt einen Payload starten, ohne die System-Firmware zu modifizieren.

## 📋 Voraussetzungen

Bevor du mit der RCM-Methode beginnst, stelle sicher, dass:

- ✅ Deine Switch eine **ungepatchte V1** ist (Serial Check durchgeführt)
- ✅ Du eine **FAT32-formatierte SD-Karte** hast
- ✅ Du einen **RCM-Jig** besitzt
- ✅ Ein **USB-C-Datenkabel** vorhanden ist
- ✅ Du den entsprechenden **Payload (hekate.bin)** heruntergeladen hast

## 🖥️ Plattform-spezifische Anleitungen

Wähle die Anleitung, die zu deinem Betriebssystem passt:

- 🪟 **[Windows Anleitung](switch_v1_softmod_windows)** - Mit TegraRcmGUI
- 🍎 **[macOS Anleitung](switch_v1_softmod_mac)** - Mit Web Fusée Launcher
- 🐧 **[Linux Anleitung](switch_v1_softmod_linux)** - Mit Command Line Tools

## ⚠️ Wichtige Hinweise

- 🔒 **RCM funktioniert nur bei ungepatchten Switch V1** Konsolen
- 💾 **FAT32 ist Pflicht** - exFAT funktioniert nicht!
- ⚡ **RCM-Jig vorsichtig verwenden** - Nicht dauerhaft stecken lassen
- 🔋 Stelle sicher, dass deine Switch genug **Akku** hat (mindestens 50%)