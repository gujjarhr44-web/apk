# GHH WebView APK Project

Location: `I:\beta program for ghh\app testing\ghh-webview`

This is a simple Android WebView app that loads:

- `app/src/main/assets/index.html`

## Local Build With Android Studio

1. Open this folder in Android Studio.
2. Let Android Studio sync Gradle and download Android SDK packages.
3. Click `Build > Build APK(s)`.

## Build APK Using GitHub

This project is prepared for GitHub Actions.

Workflow file:

- `.github/workflows/build-apk.yml`

When you push this project to GitHub, the workflow can build:

- `app/build/outputs/apk/debug/app-debug.apk`

### GitHub Steps

1. Create a new repository on GitHub.
2. Upload or push the full `ghh-webview` folder to that repository.
3. Make sure your default branch is `main` or `master`.
4. Open the GitHub repository in browser.
5. Go to `Actions`.
6. Open `Build APK`.
7. Click `Run workflow`.
8. Wait for the build to finish.
9. Open the workflow run.
10. Download the artifact named `ghh-debug-apk`.
11. Inside that artifact you will get `app-debug.apk`.

## Push To GitHub From Your PC

If you want to use GitHub Desktop:

1. Install GitHub Desktop.
2. Click `Add an Existing Repository from your Local Drive`.
3. Choose this folder: `I:\beta program for ghh\app testing\ghh-webview`
4. Publish repository to GitHub.
5. After upload, go to GitHub Actions and run `Build APK`.

If you want to use Git manually:

```bash
git init
git add .
git commit -m "Initial Android WebView app"
git branch -M main
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main
```

## Important Notes

- I could scaffold the full Android project here.
- I could not generate the final `.apk` on this machine because `java` / Android build tools are not installed in the current environment.
- Your website source was copied into:
  - `app/src/main/assets/index.html`
