# Build the starter APK using only your Android phone

This project includes a GitHub Actions workflow so you do not need a computer or Android Studio to try building the **starter UI APK**. Internet access and a GitHub account are needed.

## Steps on your phone

1. Download and extract `MovieBoxMobile-source.zip` using your phone's Files app or an archive app.
2. Open https://github.com in your browser and sign in.
3. Create a **new public or private repository** named `MovieBoxMobile`.
4. Upload the *contents* of the `MovieBoxMobile` folder (not the outer folder itself), including the `.github/workflows/build-apk.yml` file. If the mobile website cannot upload the hidden `.github` folder, use GitHub's browser editor to create `.github/workflows/build-apk.yml` with the exact contents of that file.
5. Open the repository's **Actions** tab. If prompted, enable GitHub Actions.
6. Select **Build Android APK** and tap **Run workflow**. If that option is not shown, make a commit to `main` or `master` to trigger the workflow.
7. Wait for the workflow to finish. Open its completed run, scroll to **Artifacts**, and download `MovieBoxMobile-debug-apk`.
8. Extract the artifact ZIP and tap `app-debug.apk` to install it. Android may ask you to allow installs from that browser/files app; only allow it for files you trust.

## What this APK contains

This builds the current starter UI only. It does **not** yet contain the real MovieBox-TUI engine, live providers, real movie streams, or playback. The workflow creates an APK only if the source compiles successfully; check the Actions log if it fails.
