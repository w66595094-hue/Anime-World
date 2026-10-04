# Anime World Android starter project

This is a small Android WebView app that packages the local Anime World interface into an Android APK.

## Current features
- Dark anime-themed home screen and category filters
- Sample anime catalogue (sample content, not a licensed streaming catalogue)
- A player field for direct, user-owned/authorized HTTP(S) video file URLs
- Android back navigation and WebView state handling
- GitHub Actions workflow to build a debug APK

## Build with GitHub Actions
1. Create a GitHub repository and upload the contents of this folder (not the ZIP file itself).
2. Open the repository's **Actions** tab.
3. Select **Build Anime World APK** and tap **Run workflow** (or push to the `main` branch).
4. When the run finishes, open it and download the `Anime-World-debug-APK` artifact.
5. Extract the artifact ZIP on Android and install `app-debug.apk`. Android may ask you to allow installs from that source.

## Build locally
Requires JDK 17, Android SDK Platform 35, Android Build Tools 35.0.0, and Gradle 8.9. Run:

```bash
gradle --no-daemon assembleDebug
```

APK output: `app/build/outputs/apk/debug/app-debug.apk`.

## Important limitations
- This is a starter app, not a finished production streaming service.
- Anime entries are sample catalogue cards. No episode database, accounts, cloud admin panel, or backend is included.
- The player expects a direct video URL that the Android WebView can play; ordinary webpage/watch-page links generally will not work.
- Only add videos you own or are authorized to distribute.
- The GitHub workflow builds a debug APK for testing. A release APK requires a private signing key and a separate release-signing setup.
