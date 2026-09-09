Released Changelog
1. raffprjkt-2.0-beta-arm64-release >
 New Released 
Direct access to BROM and Preloader mode using OTG
Backup and flash partition
Check active slot in BROM/Preloader
Multi Flash and Multi Backup
CLI Mode
ADB & Fastboot support
Change active slot in BROM/Preloader
English and Indonesian language
eMMC/UFS partition list
Non-root mode
DA session stays connected, so you don't need to reconnect for every operation
Reboot and shutdown menu

2. raffprjkt-3.0-beta-arm64-release
Update Hot Fix
Fix Issue Selector DA File Can't read From Folder
Fix App Can't Open In Older Android Version

3. raffprjkt-4.0-stable-arm64-release

- Bumped the MediaTek core to Penumbra 2.0.0. Updated XML/XFlash support and fixed the ARM64 extloader crash.
- Added TXT/XML scatter flashing with eMMC/UFS support, per-partition image selection, and device/image size checks. Download Only and Firmware Upgrade are both available.
- Firmware Upgrade now handles supported GPT devices with partition backups and layout verification. Migration rollback is available before formatting or writing images. Unchanged layouts skip the GPT rewrite, and supported A/B layouts get slot A selected at the end.
- Fixed up Preloader handling, USB reconnects during mode changes, and parsing of MediaTek vendor GPT layouts.
- Cleaned up the SLA flow. BROM and DA authorization are handled separately, with a two-step login dialog and fixes for challenges and server authorization.
- Reworked Fastboot logical partition flashing around the "Value too large for defined data type" issue. Added fastbootd and slot checks, 64-bit expanded image sizing, logical partition resizing, and capacity checks before flashing.
- Fixed raw/sparse splitting for large images and AVB footer placement on larger physical partitions. Added more checks for malformed or truncated images.
- Flashing stops on the first failure. Cancel handling got a cleanup too, and unfinished flashes are remembered so you get a heads-up before rebooting.
- Fixed ADB USB packet handling, checksums, stream IDs, partial transfers, and failed service/reboot requests being reported as successful.
- Added a built-in file picker with folder navigation, including support in ADB/Fastboot operations.
- Reworked the dashboard, settings, logs, and animations. Added custom color palettes and moved feedback popups to the bottom of the screen.
