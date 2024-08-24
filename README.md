# Orange-Pi-5-Plus-Android-TV-12-Gapps
Orange Pi 5 Plus Android TV 12 Gapps (Official System) Magisk module

## Guide
 1. Download repo apk dir and [Releases](https://github.com/shiyunjin/Orange-Pi-5-Plus-Android-TV-12-Gapps/releases) module zip push to Orange Pi storage.
 2. Install `Cx File Explorer_2.3.2.apk` and `Magisk.apk` .
 3. Open `Cx File Explorer` grant permissions.
 4. Open Magisk, Start `install`, Select `Direct install`, Reboot.
 5. Open Magisk, Select `Modules` Tab, Click `Install from storage`, select `Cx File Explorer` -> `Always`, select `Orange-Pi-5-Plus-Android-TV-12-Gapps-xxxxxx.zip`, Click `OK`, Reboot.
 6. Open `Settings`, Click `Apps`, Click `See all apps`, Find `Google Play Store`, Set `UI mode` to `TV`.
 7. In `Settings` -> `Apps`, Find `Android TV Remote Service`, Click `Permissions`, Grant All.
 8. Open `Google Play Store`, try login once (It should fail, no problem, just keep going).
 9. Link Orange Pi to PC ADB (Network ADB can also).
 10. Run in terminal
     ```
     adb root
     adb shell
     sqlite3 /data/user/0/*/*/gservices.db "select * from main where name = \"android_id\";"
     ```
     well show `android_id|3****************`
 11. Open [Link](https://www.google.com/android/uncertified/) in brower, login your Google account, input `3****************`(your android_id), Register.
 12. In `Settings` -> `Apps`, Find `Google Play Store`, Clean All Data.
 13. Reboot.
 14. Open `Google Play Store`, Try login again.
 15. All done.

## Troubleshooting
 * `Google Play Movies & TV` crash, Need Set `UI mode` to `TV` on App Settings.
 * Magisk may get stuck at the start screen. Do not wait and restart the machine immediately to recover.

## Tested Rom Version
 * OrangePi5Plus-RK3588_Android12-box_v1.0.0.tar.gz [Download Link](https://drive.google.com/file/d/1oyPoUTUPhVSqmwT-SSkec1nOau_70LTC/view)

