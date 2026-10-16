# Digital Sign App — Android native starter project

Independent Android app project inspired by the broad workflow of the provided MARIGOLD_USB_4.7.3.apk. It does not copy its proprietary source code, branding, assets, or implementation.

## Included in this starter
- Android TV / Android signage launcher entry (Leanback category included).
- Offline image and video playlist.
- Import from Android's system file picker, including USB drives exposed by the device's file manager. Imported files are copied to app-private storage.
- Full-screen looping playback; images use a configurable default duration and videos advance on completion.
- Daily start/end schedule with overnight time ranges; player shows a standby screen outside the schedule and checks periodically.
- Optional portrait orientation.
- Optional boot auto-start receiver, subject to Android OS/vendor background-launch restrictions.
- Keep-screen-on during playback.

## Build
Open this folder in Android Studio (current stable version), allow Gradle sync, then choose **Build > Build APK(s)**. The project uses Android Gradle Plugin 8.6.1, compile SDK 35, min SDK 23 and Java source.

A compiled APK is not included because this execution environment has Java but no Android SDK/build-tools or Gradle installation. Build and test on the actual target device before production use.

## Test checklist
1. Import a JPG/PNG and an MP4 from USB.
2. Disconnect USB and confirm the imported media still plays offline.
3. Confirm playlist loops and video playback advances.
4. Set a near-future schedule window and verify standby/resume.
5. Test portrait mode on the actual panel.
6. Enable auto-start and reboot. Some Android TV vendors block activities launched from boot; use the device's kiosk/auto-launch setting or a managed-device policy if necessary.
7. Check supported video codecs/resolutions and long-run playback for 24–72 hours.

## Known limitations of this first native build
- Scheduling is one daily time window for the whole playlist, not separate per-playlist day/time rules.
- USB import uses the Android document picker rather than scanning USB storage without user consent.
- Auto-start after reboot depends on Android version, OEM restrictions and device configuration.
- No remote/cloud management, content download, admin PIN, per-item scheduling, or watchdog service yet.
