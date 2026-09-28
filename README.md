<div align="center">

# RaffXLink

### Release Changelog

[![Latest Release](https://img.shields.io/badge/Latest_Release-v4.1_Stable-00c896?style=for-the-badge&labelColor=182230)](#v41-stable)
[![Android](https://img.shields.io/badge/Android-ARM64-6fcf97?style=for-the-badge&logo=android&logoColor=white&labelColor=182230)](#release-information)
[![Non-root](https://img.shields.io/badge/USBFS-Non--root-67b7ff?style=for-the-badge&labelColor=182230)](#v41-stable)

[![README Views](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2Fmuhammadrafiasyddiq%2Fpenumbra-android&label=README%20Views&labelColor=%23182230&countColor=%2300c896&style=for-the-badge)](https://visitorbadge.io/status?path=https%3A%2F%2Fgithub.com%2Fmuhammadrafiasyddiq%2Fpenumbra-android)

**From v2.0 Beta to v4.1 Stable — a major update to MediaTek flashing, authorization, USB communication, and the Android experience.**

[Latest Release](#v41-stable) · [Previous Releases](#previous-releases) · [Release Information](#release-information)

</div>

---

<a id="v41-stable"></a>
## v4.1 Stable

**`raffprjkt-4.1-stable-arm64-release`**

![Stable](https://img.shields.io/badge/Release-STABLE-00c896?style=flat-square&labelColor=182230)
![Major Update](https://img.shields.io/badge/Update-MAJOR-67b7ff?style=flat-square&labelColor=182230)

RaffXLink v4.1 Stable brings major improvements to the MediaTek flashing engine, Scatter Flashing, Firmware Upgrade, Xiaomi Authorization, the Android USBFS non-root backend, and overall application stability.

### 01 · MediaTek Flash Engine

- Updated the MediaTek core to **Penumbra 2.0.0**, improved XML/XFlash support, and fixed the ARM64 extloader crash.
- Added **Scatter V5 (TXT)** and **Scatter V6 (XML)** flashing with eMMC and UFS support.
- Introduced SP Flash Tool-style **Download Only** and **Firmware Upgrade** operations.
- Added per-partition image selection, device and image-size checks, and improved partition mapping.
- Improved GPT/PMT parsing, including MediaTek vendor GPT layouts, and storage compatibility validation.
- Improved Preloader handling and USB reconnection during device mode changes.

### 02 · Firmware Upgrade

- Implemented Firmware Upgrade engines for supported **Scatter V5 and V6** devices.
- Added GPT layout verification, partition backup, and migration support, including PGPT and SGPT handling where supported.
- Enhanced seccfg handling and Auto Relock options.

### 03 · Xiaomi Authorization

- Introduced a dedicated **Xiaomi Authorization** interface with device model selection.
- Integrated server-based authentication through RaffXLink.
- Improved support for Xiaomi devices using legacy and newer BROM SLA security mechanisms.
- Separated **BROM SLA** and **DA SLA** authorization handling.
- Added a two-step login dialog with authentication progress logs and detailed error reporting.
- Improved challenge processing, server authorization responses, and USB-session handling during authentication.

### 04 · USBFS, ADB & Fastboot

- Reworked the Android USB backend for **non-root USBFS** operation.
- Improved MediaTek USB communication, reconnect handling, and transfer diagnostics.
- Fixed ADB USB packet handling, checksums, stream IDs, and partial transfers.
- Fixed failed ADB service and reboot requests being incorrectly reported as successful.
- Improved Fastboot and Fastbootd connection and slot checks.
- Reworked Fastboot logical partition flashing, including **64-bit expanded image sizing**, partition resizing, and capacity checks.
- Fixed raw/sparse image splitting, large-image transfer handling, and AVB footer placement on larger physical partitions.
- Added checks for malformed or truncated images and improved handling of the **“Value too large for defined data type”** error.

### 05 · Partition & Backup Manager

- Added **Erase Partition** functionality.
- Improved individual partition flashing and backup operations.
- Enhanced A/B slot management with BootControl verification.
- Improved partition selection, validation, and handling of duplicate Scatter entries.
- Updated flashing and backup progress reporting for better readability.
- Flashing stops on the first failure; cancel handling and unfinished-flash warnings have been improved.

### 06 · UI & User Experience

- Redesigned the dashboard, navigation, settings, logs, animations, dialogs, and notifications.
- Introduced the dedicated Xiaomi Authorization interface.
- Added custom interface color palettes and improved language settings.
- Added a built-in file picker with folder navigation, including ADB and Fastboot integration.
- Added an application update checker.
- Improved operation progress indicators and moved feedback popups to the bottom of the screen.

### 07 · Security & Stability

- Fixed multiple crashes affecting flashing and backup workflows.
- Improved compatibility across Android API levels.
- Enhanced Scatter TXT/XML validation, partition-size checks, and duplicate-entry detection.
- Improved Download Agent acknowledgment handling, connection recovery, and failure reporting.
- Temporarily removed root CLI mode And CLI Non-root to focus development on the **non-root Android backend**.

### STILL W.I.P · 

- MI ASSISTANT 
- META MODE(FOR WRITE IMEI)
- ANTICRACK FIX TRANSSION

---

<a id="previous-releases"></a>
## Previous Releases

<details>
<summary><strong>v3.0 Beta</strong> — raffprjkt-3.0-beta-arm64-release</summary>

**Update Hot Fix**

- Fix Issue Selector DA File Can't read From Folder
- Fix App Can't Open In Older Android Version

</details>

<details>
<summary><strong>v2.0 Beta</strong> — raffprjkt-2.0-beta-arm64-release &gt;</summary>

**New Released**

- Direct access to BROM and Preloader mode using OTG
- Backup and flash partition
- Check active slot in BROM/Preloader
- Multi Flash and Multi Backup
- CLI Mode
- ADB & Fastboot support
- Change active slot in BROM/Preloader
- English and Indonesian language
- eMMC/UFS partition list
- Non-root mode
- DA session stays connected, so you don't need to reconnect for every operation
- Reboot and shutdown menu

</details>

---

<a id="release-information"></a>
## Release Information

| | |
| :--- | :--- |
| **Release** | `4.1-stable` |
| **Changelog baseline** | `2.0-beta` |
| **Version code** | `301` |
| **Architecture** | `arm64-v8a` |
| **Minimum Android** | Android 8.0 (API 26) |
| **USB backend** | Android USBFS (non-root) |

> [!IMPORTANT]
> Xiaomi Authorization requires access to a compatible authentication server. Firmware operations require matching firmware and a compatible Download Agent. Back up important device data before flashing; feature support varies by chipset, security configuration, and device.

<div align="center">

[↑ Back to top](#raffxlink)

<sub>README Views is a third-party badge counter. It tracks badge requests from the time the counter is enabled, not verified unique readers or historical GitHub traffic.</sub>

</div>
