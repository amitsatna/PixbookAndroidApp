# Pixbook Android App

Official Android Application for **Pixbook** (`com.pix.pixbook`). Built for high performance, camera photo uploads, Razorpay payment processing, and Google Play Store compliance.

---

## 📱 Features

- **Google Play Store Ready**: Target SDK 34 (Android 14) compliance.
- **Camera & Gallery Photo Uploads**: Full `<input type="file">` support via native `WebChromeClient` file provider.
- **Razorpay Payments Integration**: Handles Razorpay checkout modal smoothly within Android WebView.
- **SwipeRefreshLayout**: Native pull-to-refresh for easy page reloads.
- **Offline Network Support**: Native offline detector with clean retry view.
- **Automated CI/CD**: GitHub Actions workflow (`.github/workflows/android.yml`) automatically builds test APK (`app-debug.apk`) and Play Store bundle (`app-release.aab`) on every push.

---

## 🛠️ Project Structure

```
PixbookAndroidApp/
├── app/
│   ├── build.gradle                   # App dependencies & SDK 34 config
│   └── src/
│       └── main/
│           ├── AndroidManifest.xml    # Permissions & FileProvider
│           ├── java/com/pix/pixbook/  # MainActivity.java (WebView Core)
│           └── res/                   # Layouts, Colors, Styles & File Paths
├── .github/workflows/android.yml       # GitHub Actions Automated APK Builder
├── build.gradle                       # Project level gradle
├── settings.gradle                    # Project settings
└── gradlew                            # Gradle wrapper script
```

---

## ⚡ Automated APK & AAB Builds

Every push to `main` branch automatically triggers GitHub Actions:
1. Go to **Actions** tab in this GitHub repository.
2. Select the latest build.
3. Download **`pixbook-debug-apk`** for testing on your phone.
4. Download **`pixbook-release-aab`** for uploading to [Google Play Console](https://play.google.com/console).
