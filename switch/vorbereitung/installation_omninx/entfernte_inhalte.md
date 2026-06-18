# Entfernte Inhalte – Clean vs. Update

Gegenüberstellung der **Deletion Lists** im OmniNX Installer: `deletion_lists_clean.h` (Saubere Installation) und `deletion_lists_update.h` (Update).

:icon-trash: = Pfad steht in der jeweiligen Liste. — = nicht in dieser Liste.

---

## Übersicht

| Bereich | Saubere Installation | Update |
| --- | --- | --- |
| `atmosphere/` | `sd:/atmosphere` (ein Eintrag) | 27 Unterordner, 32 Title-IDs unter `contents/`, 8 Dateien |
| `bootloader/` | 7 Unterordner, 6 Dateien | 7 Unterordner, 7 Dateien (+ `nyx.ini`) |
| `config/` | 8 Ordner | 9 Ordner (+ `quickntp`) |
| `switch/` | `sd:/switch` (ein Eintrag) | 54 Ordner, 49 Dateien/NROs |
| SD-Root | 12 Dateien | 12 Dateien (identisch) |
| Sonstiges | 11 Ordner, 8 Dateien | 10 Ordner, 8 Dateien |
| Alte Versionsmarker | 8 Dateien | — |
| Nach Restore | `switch/tinfoil/db` | — |

Insgesamt **63** Einträge in der Clean-Liste, **224** in der Update-Liste, **51** in beiden.

---

## Atmosphere

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/atmosphere` | :icon-trash: | — |
| `sd:/atmosphere/config` | — | :icon-trash: |
| `sd:/atmosphere/config/exosphere.ini` | — | :icon-trash: |
| `sd:/atmosphere/config/stratosphere.ini` | — | :icon-trash: |
| `sd:/atmosphere/contents/0000000000534C56` | — | :icon-trash: |
| `sd:/atmosphere/contents/00FF0000636C6BFF` | — | :icon-trash: |
| `sd:/atmosphere/contents/00FF0000A53BB665` | — | :icon-trash: |
| `sd:/atmosphere/contents/00FF0000B378D640` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000008` | — | :icon-trash: |
| `sd:/atmosphere/contents/010000000000000D` | — | :icon-trash: |
| `sd:/atmosphere/contents/010000000000002B` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000032` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000034` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000036` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000037` | — | :icon-trash: |
| `sd:/atmosphere/contents/010000000000003C` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000042` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000895` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000000F12` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000001000` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000001007` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100000000001013` | — | :icon-trash: |
| `sd:/atmosphere/contents/010000000000DA7A` | — | :icon-trash: |
| `sd:/atmosphere/contents/010000000000bd00` | — | :icon-trash: |
| `sd:/atmosphere/contents/01006a800016e000` | — | :icon-trash: |
| `sd:/atmosphere/contents/01009D901BC56000` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100A3900C3E2000` | — | :icon-trash: |
| `sd:/atmosphere/contents/0100F43008C44000` | — | :icon-trash: |
| `sd:/atmosphere/contents/050000BADDAD0000` | — | :icon-trash: |
| `sd:/atmosphere/contents/4200000000000000` | — | :icon-trash: |
| `sd:/atmosphere/contents/420000000000000B` | — | :icon-trash: |
| `sd:/atmosphere/contents/420000000000000E` | — | :icon-trash: |
| `sd:/atmosphere/contents/4200000000000010` | — | :icon-trash: |
| `sd:/atmosphere/contents/4200000000000FFF` | — | :icon-trash: |
| `sd:/atmosphere/contents/420000000007E51A` | — | :icon-trash: |
| `sd:/atmosphere/contents/420000000007E51B` | — | :icon-trash: |
| `sd:/atmosphere/contents/690000000000000D` | — | :icon-trash: |
| `sd:/atmosphere/crash_reports` | — | :icon-trash: |
| `sd:/atmosphere/erpt_reports` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/CrunchPatch` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/Crunchyroll Patch 1.10.0` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/SaltyNX_Fixes` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/audio_mastervolume` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/bluetooth_patches` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/bootlogo` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/btm_patches` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/es_patches` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/hid_patches` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/logo` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/nfim_ctest` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/nim_ctest` | — | :icon-trash: |
| `sd:/atmosphere/exefs_patches/nvnflinger_cmu` | — | :icon-trash: |
| `sd:/atmosphere/extrazz` | — | :icon-trash: |
| `sd:/atmosphere/fatal_errors` | — | :icon-trash: |
| `sd:/atmosphere/fatal_reports` | — | :icon-trash: |
| `sd:/atmosphere/flags` | — | :icon-trash: |
| `sd:/atmosphere/hbl.nsp` | — | :icon-trash: |
| `sd:/atmosphere/hbl_html` | — | :icon-trash: |
| `sd:/atmosphere/hosts` | — | :icon-trash: |
| `sd:/atmosphere/kip1` | — | :icon-trash: |
| `sd:/atmosphere/kip_patches` | — | :icon-trash: |
| `sd:/atmosphere/kips` | — | :icon-trash: |
| `sd:/atmosphere/kips/hoc.kip` | — | :icon-trash: |
| `sd:/atmosphere/kips/loader.kip` | — | :icon-trash: |
| `sd:/atmosphere/logs` | — | :icon-trash: |
| `sd:/atmosphere/package3` | — | :icon-trash: |
| `sd:/atmosphere/reboot_payload.bin` | — | :icon-trash: |
| `sd:/atmosphere/stratosphere.romfs` | — | :icon-trash: |

---

## Bootloader

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/bootloader/ArgonNX.bin` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/boot` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/bootlogo` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/bootlogo.bmp` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/hekate_ipl.ini` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/ini/EmuMMC ohne Mods.ini` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/ini2` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/nyx.ini` | — | :icon-trash: |
| `sd:/bootloader/patches.ini` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/payloads` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/reboot` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/res` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/sys` | :icon-trash: | :icon-trash: |
| `sd:/bootloader/update.bin` | :icon-trash: | :icon-trash: |

---

## Config

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/config/aio-switch-updater` | :icon-trash: | :icon-trash: |
| `sd:/config/blue_pack_updater` | :icon-trash: | :icon-trash: |
| `sd:/config/kefir-updater` | :icon-trash: | :icon-trash: |
| `sd:/config/nx-hbmenu` | :icon-trash: | :icon-trash: |
| `sd:/config/quickntp` | — | :icon-trash: |
| `sd:/config/sys-con` | :icon-trash: | :icon-trash: |
| `sd:/config/sys-patch` | :icon-trash: | :icon-trash: |
| `sd:/config/uberhand` | :icon-trash: | :icon-trash: |
| `sd:/config/ultrahand` | :icon-trash: | :icon-trash: |

---

## Switch

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/switch` | :icon-trash: | — |
| `sd:/switch/.overlays` | — | :icon-trash: |
| `sd:/switch/.packages` | — | :icon-trash: |
| `sd:/switch/90DNS_tester` | — | :icon-trash: |
| `sd:/switch/90DNS_tester/90DNS_tester.nro` | — | :icon-trash: |
| `sd:/switch/AtmoXL-Titel-Installer` | — | :icon-trash: |
| `sd:/switch/ChoiDujourNX` | — | :icon-trash: |
| `sd:/switch/ChoiDujourNX.nro` | — | :icon-trash: |
| `sd:/switch/DBI.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_810_DE.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_810_EN.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_845_DE.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_845_EN.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_849_DE.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_849_EN.nro` | — | :icon-trash: |
| `sd:/switch/DBI/DBI_EN.nro` | — | :icon-trash: |
| `sd:/switch/DBI_810_DE/DBI_810.nro` | — | :icon-trash: |
| `sd:/switch/DBI_810_DE/DBI_810_DE.nro` | — | :icon-trash: |
| `sd:/switch/DBI_810_EN/DBI_810_EN.nro` | — | :icon-trash: |
| `sd:/switch/DBI_DE/DBI_DE.nro` | — | :icon-trash: |
| `sd:/switch/DBI_RU/DBI_RU.nro` | — | :icon-trash: |
| `sd:/switch/DNS_mitm Tester` | — | :icon-trash: |
| `sd:/switch/DNS_mitm Tester.nro` | — | :icon-trash: |
| `sd:/switch/Daybreak` | — | :icon-trash: |
| `sd:/switch/EdiZon` | — | :icon-trash: |
| `sd:/switch/EdiZon.nro` | — | :icon-trash: |
| `sd:/switch/FTPD` | — | :icon-trash: |
| `sd:/switch/Fizeau` | — | :icon-trash: |
| `sd:/switch/Fizeau.nro` | — | :icon-trash: |
| `sd:/switch/Goldleaf` | — | :icon-trash: |
| `sd:/switch/Goldleaf.nro` | — | :icon-trash: |
| `sd:/switch/JKSV` | — | :icon-trash: |
| `sd:/switch/JKSV.nro` | — | :icon-trash: |
| `sd:/switch/Linkalho` | — | :icon-trash: |
| `sd:/switch/Moonlight-Switch` | — | :icon-trash: |
| `sd:/switch/Moonlight-Switch.nro` | — | :icon-trash: |
| `sd:/switch/NX-Activity-Log` | — | :icon-trash: |
| `sd:/switch/NX-Save-Sync` | — | :icon-trash: |
| `sd:/switch/NX-Shell` | — | :icon-trash: |
| `sd:/switch/NX-Shell.nro` | — | :icon-trash: |
| `sd:/switch/NX-Update-Checker ` | — | :icon-trash: |
| `sd:/switch/NXGallery` | — | :icon-trash: |
| `sd:/switch/NXGallery.nro` | — | :icon-trash: |
| `sd:/switch/NXRemoteLauncher` | — | :icon-trash: |
| `sd:/switch/NXThemesInstaller` | — | :icon-trash: |
| `sd:/switch/NXThemesInstaller.nro` | — | :icon-trash: |
| `sd:/switch/Neumann` | — | :icon-trash: |
| `sd:/switch/Neumann.nro` | — | :icon-trash: |
| `sd:/switch/Payload_launcher` | — | :icon-trash: |
| `sd:/switch/Reboot` | — | :icon-trash: |
| `sd:/switch/Shutdown_System` | — | :icon-trash: |
| `sd:/switch/SimpleModDownloader` | — | :icon-trash: |
| `sd:/switch/SimpleModDownloader.nro` | — | :icon-trash: |
| `sd:/switch/SimpleModManager` | — | :icon-trash: |
| `sd:/switch/SimpleModManager.nro` | — | :icon-trash: |
| `sd:/switch/Switch-Time` | — | :icon-trash: |
| `sd:/switch/SwitchIdent` | — | :icon-trash: |
| `sd:/switch/SwitchIdent.nro` | — | :icon-trash: |
| `sd:/switch/Switch_themes_Installer` | — | :icon-trash: |
| `sd:/switch/Switch_themes_Installer/NXThemesInstaller.nro` | — | :icon-trash: |
| `sd:/switch/Sys-Clk Manager` | — | :icon-trash: |
| `sd:/switch/Sys-Clk Manager/sys-clk-manager.nro` | — | :icon-trash: |
| `sd:/switch/Sys-Con` | — | :icon-trash: |
| `sd:/switch/Sys-Con.nro` | — | :icon-trash: |
| `sd:/switch/aio-switch-updater` | — | :icon-trash: |
| `sd:/switch/amsPLUS-downloader` | — | :icon-trash: |
| `sd:/switch/appstore` | — | :icon-trash: |
| `sd:/switch/breeze` | — | :icon-trash: |
| `sd:/switch/breeze.nro` | — | :icon-trash: |
| `sd:/switch/cheats-updater` | — | :icon-trash: |
| `sd:/switch/cheats-updater.nro` | — | :icon-trash: |
| `sd:/switch/checkpoint` | — | :icon-trash: |
| `sd:/switch/chiaki` | — | :icon-trash: |
| `sd:/switch/chiaki.nro` | — | :icon-trash: |
| `sd:/switch/crash_ams` | — | :icon-trash: |
| `sd:/switch/daybreak.nro` | — | :icon-trash: |
| `sd:/switch/fw-downloader` | — | :icon-trash: |
| `sd:/switch/gamecard_installer` | — | :icon-trash: |
| `sd:/switch/haze` | — | :icon-trash: |
| `sd:/switch/haze.nro` | — | :icon-trash: |
| `sd:/switch/kefir-updater` | — | :icon-trash: |
| `sd:/switch/ldnmitm_config` | — | :icon-trash: |
| `sd:/switch/ldnmitm_config.nro` | — | :icon-trash: |
| `sd:/switch/linkalho.nro` | — | :icon-trash: |
| `sd:/switch/nxdumptool` | — | :icon-trash: |
| `sd:/switch/nxdumptool.nro` | — | :icon-trash: |
| `sd:/switch/nxmtp` | — | :icon-trash: |
| `sd:/switch/nxtc.bin` | — | :icon-trash: |
| `sd:/switch/reboot_to_argonNX` | — | :icon-trash: |
| `sd:/switch/reboot_to_hekate` | — | :icon-trash: |
| `sd:/switch/reboot_to_payload.nro` | — | :icon-trash: |
| `sd:/switch/sphaira` | — | :icon-trash: |
| `sd:/switch/sphaira.nro` | — | :icon-trash: |
| `sd:/switch/studious-pancake` | — | :icon-trash: |
| `sd:/switch/swr-ini-tool/swr-ini-tool.nro` | — | :icon-trash: |
| `sd:/switch/sys-clk-manager` | — | :icon-trash: |
| `sd:/switch/sys-clk-manager.nro` | — | :icon-trash: |
| `sd:/switch/themezer-nx` | — | :icon-trash: |
| `sd:/switch/themezernx` | — | :icon-trash: |
| `sd:/switch/tinfoil.nro` | — | :icon-trash: |
| `sd:/switch/tinfoil/tinfoil.nro` | — | :icon-trash: |
| `sd:/switch/tinwoo` | — | :icon-trash: |
| `sd:/switch/tinwoo.nro` | — | :icon-trash: |
| `sd:/switch/tinwoo/tinwoo.nro` | — | :icon-trash: |

---

## SD-Root

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/boot.dat` | :icon-trash: | :icon-trash: |
| `sd:/boot.ini` | :icon-trash: | :icon-trash: |
| `sd:/exosphere.bin` | :icon-trash: | :icon-trash: |
| `sd:/exosphere.ini` | :icon-trash: | :icon-trash: |
| `sd:/hbmenu.nro` | :icon-trash: | :icon-trash: |
| `sd:/install.bat` | :icon-trash: | :icon-trash: |
| `sd:/license` | :icon-trash: | :icon-trash: |
| `sd:/loader.bin` | :icon-trash: | :icon-trash: |
| `sd:/mc-mitm.log` | :icon-trash: | :icon-trash: |
| `sd:/payload.bin` | :icon-trash: | :icon-trash: |
| `sd:/update.bin` | :icon-trash: | :icon-trash: |
| `sd:/version` | :icon-trash: | :icon-trash: |

---

## Sonstiges

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/NSPs (Tools)` | :icon-trash: | :icon-trash: |
| `sd:/Patched Apps` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/exceptions.txt` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/flags` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/patches` | :icon-trash: | — |
| `sd:/SaltySD/saltysd_bootstrap.elf` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/saltysd_bootstrap32_3k.elf` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/saltysd_bootstrap32_5k.elf` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/saltysd_core.elf` | :icon-trash: | :icon-trash: |
| `sd:/SaltySD/saltysd_core32.elf` | :icon-trash: | :icon-trash: |
| `sd:/TegraExplorer` | :icon-trash: | — |
| `sd:/argon` | :icon-trash: | :icon-trash: |
| `sd:/fusee-primary.bin` | :icon-trash: | :icon-trash: |
| `sd:/fusee.bin` | :icon-trash: | :icon-trash: |
| `sd:/games` | :icon-trash: | :icon-trash: |
| `sd:/scripts` | :icon-trash: | :icon-trash: |
| `sd:/switch/tinfoil/db` | — | :icon-trash: |
| `sd:/themes/systemData` | :icon-trash: | :icon-trash: |
| `sd:/tools` | :icon-trash: | :icon-trash: |
| `sd:/warmboot_mariko` | :icon-trash: | :icon-trash: |

---

## Alte Versionsmarker

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/1.4.0-pre` | :icon-trash: | — |
| `sd:/1.4.0-pre-c` | :icon-trash: | — |
| `sd:/1.4.0-pre-d` | :icon-trash: | — |
| `sd:/1.4.1` | :icon-trash: | — |
| `sd:/1.5.0` | :icon-trash: | — |
| `sd:/1.6.0` | :icon-trash: | — |
| `sd:/1.6.1` | :icon-trash: | — |
| `sd:/1.6.2` | :icon-trash: | — |

---

## Nach Restore (nur Clean)

| Pfad | Saubere Installation | Update |
| --- | :---: | :---: |
| `sd:/switch/tinfoil/db` | :icon-trash: | — |

---

## Legende

| Symbol | Bedeutung |
| --- | --- |
| :icon-trash: | Pfad ist in der Deletion List dieses Modus eingetragen |
| — | Pfad ist in der Deletion List dieses Modus **nicht** eingetragen |

!!!Quelle
Listen und Gruppierung entsprechen `clean_mode_wipe()` in `install_clean.c` bzw. `update_mode_cleanup()` in `install_update.c` im Repository [OmniNX-Installer-Payload](https://git.niklascfw.de/OmniNX/OmniNX-Installer-Payload) (`deletion_lists_clean.h`, `deletion_lists_update.h`). Der Eintrag `sd:/switch/tinfoil/db` wird bei Clean erst **nach** der DBI-Wiederherstellung entfernt (`clean_post_restore_dirs_to_delete`), beim Update bereits in der Bereinigung (`misc_dirs_to_delete`).
!!!
