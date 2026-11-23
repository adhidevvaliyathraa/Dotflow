# DotFlow — Android Studio project

A first-stage, Nothing-inspired floating pill for Android. Target device: Nothing Phone 3a.

## Included in this starter build
- Floating monochrome pill overlay (user starts/stops it).
- Charging state indicator.
- Notification title/text preview after Notification Access is enabled.
- Basic incoming-call / call-in-progress state via Android phone-state broadcast.
- Tapping the pill opens the DotFlow control screen.
- No Wireless debugging, ADB pairing, account, or network connection.

## Not yet implemented
- Media-session metadata and playback buttons.
- In-app timer and stopwatch UI.
- Drag-to-reposition, polished dot-matrix artwork, animation, notification filtering and privacy controls.
These are planned follow-up features; they are not represented as completed.

## Build
1. Install Android Studio (current stable) and Android SDK Platform 35.
2. Open this folder as a project.
3. Allow Android Studio to sync Gradle and install the required Android Gradle Plugin/Kotlin plugin.
4. Build > Build Bundle(s) / APK(s) > Build APK(s).
5. The debug APK is normally created at `app/build/outputs/apk/debug/app-debug.apk`.

## First launch
1. Open DotFlow.
2. Allow “Display over other apps” if you want the floating pill.
3. Optionally enable DotFlow under Android's Notification access settings to show notification previews.
4. Optionally grant Phone permission for call-state indication.
5. Tap START DOTFLOW. Tap STOP DOTFLOW to remove the pill.

## Privacy and permission notes
- Overlay access lets the app draw its pill above other apps. Android requires this special access.
- Notification access is powerful: Android lets the service read notification content. Enable it only if you trust this app and want previews. The starter app does not upload notification content.
- Phone state permission is used only to display basic call state. Android/OEM versions may restrict background call-state delivery.
- The persistent foreground-service notification is required while the overlay is running.
- Charging state is displayed while the service is active.
- This starter does not request Wireless debugging or ADB access.

## Compatibility
The project targets API 35 and supports Android 8.0+ (API 26+). Actual behavior can vary by Nothing OS version and Android background-execution policies. Test on-device before relying on call or notification behavior.
