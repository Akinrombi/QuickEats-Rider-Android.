# QuickEats Rider Android wrapper

This is a small Android WebView wrapper for the existing live rider site. It does not edit or replace the Render website or the original partner repository.

## What it does
- Opens `https://partner-app-5l9f.onrender.com` in an Android app named QuickEats Rider.
- Enables JavaScript and browser storage needed by the existing dashboard.
- Requests Android location permission when the website requests GPS.

## Build an APK using GitHub Actions
1. Upload these files into a **new GitHub repository** (keep the existing partner website repository unchanged).
2. Open that repository's **Actions** tab.
3. Select **Build QuickEats Rider APK** and click **Run workflow** (or push to `main`).
4. Open the completed workflow run and download the `QuickEats-Rider-APK` artifact.
5. The artifact is a ZIP containing `app-debug.apk`. Extract it, then install the APK on your Android phone. You may need to allow installing apps from your browser/file manager.

## Important limitations
- This wrapper is an initial APK build, not a signed Play Store release.
- It does not guarantee GPS tracking while the app is in the background or when Android suspends the app. Reliable background tracking requires a native foreground service and additional Android permission handling.
- The first APK build must run on a machine with Android SDK/Gradle. This environment does not have Android SDK build tools installed, so it cannot directly compile the APK here.
