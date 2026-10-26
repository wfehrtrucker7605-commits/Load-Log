# LoadLog Android (offline native app)

This is a native Android Studio project for the LoadLog trucking log. It uses Android's built-in SQLite database (`loadlog.db`) stored privately on the phone. Load, fuel, and waiting records are available without internet. Company-paid fuel is recorded separately and is never deducted from earnings.

## Included
- Flat-rate load records (logs / wood chips, date, pay, pickup, delivery, ticket, times, notes)
- Company-paid fuel log (litres, station, odometer, receipt reference and total)
- Unpaid waiting-time log (supports overnight time ranges)
- Monthly total earnings, load counts and material breakdown; waiting and fuel summaries
- CSV export through Android's save-file picker
- Delete individual records

## Build an APK
1. Open this folder in Android Studio on a computer.
2. Let Gradle sync, then choose **Build > Build APK(s)**.
3. Install the generated debug APK on your Android phone. For distribution, make a signed release APK.

This environment generated the complete source project but did not compile/sign an APK. The project requires Android Gradle Plugin 8.6.1 and Android SDK 35 during build. The app itself does not require internet permission or internet access to record or view data.

## Important data note
Records live in the app's private database. Android app data can be lost if the app is uninstalled or its data is cleared. Export CSV backups regularly and save them somewhere safe. Android's automatic backup is enabled where the device supports it.
