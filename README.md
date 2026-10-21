# Ember: an alarm app with a few unusual ideas

- **Sunrise ramp**: sound and screen brightness rise slowly (10-30 min) so it never starts at full blast.
- **Early start**: begins quietly up to 30 min before your set time.
- **Proof you are awake**: the alarm only stops after you repeat a flashing tile pattern (3 or 5 tiles).
- **Shrinking snooze**: 9, then 5, then 2 minutes, then none. Shows how many minutes you borrowed.
- **First move**: after waking you name your first task; it waits on the home screen.

Alarms use Android's exact alarm clock API, so they ring with the phone locked, in Doze, and after a restart.

## Get the APK without installing anything (GitHub)
1. Create a free account at github.com and make a **new empty repository** (any name).
2. On the repository page choose **Add file > Upload files** and drag in everything from this folder
   (including the hidden `.github` folder), then **Commit changes**.
3. Open the **Actions** tab. The "Build Ember APK" run starts by itself (about 3-5 minutes).
4. When it shows a green tick, open it and download **Ember-APK** at the bottom. Unzip it to get `app-debug.apk`.
5. Send the APK to your phone (Drive, WhatsApp, USB). Tap it and allow "Install unknown apps" for that app.

## Or build on a computer
Open this folder in Android Studio and press Run, or run `./gradlew assembleDebug`.
The APK is created at `app/build/outputs/apk/debug/app-debug.apk`.

## First launch on the phone
- Allow **notifications** when asked.
- On Android 14+, allow **full-screen alarms** when the settings page opens, so Ember can show over the lock screen.
- Press **Test ring** on the home screen, then lock the phone and wait 5 seconds to check sound and the lock-screen screen.
