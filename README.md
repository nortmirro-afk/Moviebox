# MovieBox Mobile — Android starter project

This is the first native Android UI project for a standalone app inspired by MovieBox-TUI. It opens directly into a modern movie-style home screen: poster cards, search, saved titles, detail pages, and bottom navigation. It does not show a terminal or open a keyboard on launch.

## Important: what this project is (and isn't)

- **Included:** Android/Kotlin/Jetpack Compose project source and a starter interface.
- **Not yet included:** the working MovieBox-TUI provider engine, live catalog/search results, real stream URLs, video playback integration, or a compiled APK.
- The sample titles are demo data. Poster images are loaded from TMDB image URLs and require internet access.
- Upstream MovieBox-TUI is a Rust terminal application. Its documentation currently describes Android use through Termux and an external media player, not a ready-made Android UI SDK. A proper standalone app needs a native integration layer; simply putting the terminal binary inside an APK will not create a touch UI.

Upstream project: https://github.com/mesamirh/MovieBox-Tui

## Build the starter APK (beginner steps)

1. On a computer, install Android Studio: https://developer.android.com/studio
2. Extract this ZIP.
3. In Android Studio, choose **Open** and select the extracted `MovieBoxMobile` folder (the one containing `settings.gradle.kts`).
4. Let Gradle sync and install the Android SDK platform requested by Android Studio if prompted.
5. Connect an Android phone with USB debugging enabled, or create an emulator.
6. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
7. Android Studio will show a link to the generated APK when the build completes.

## Planned next phase: real engine integration

1. Pin an upstream MovieBox-TUI release/commit and inspect its license and provider interfaces.
2. Build its Rust engine for Android arm64 using the Android NDK, or refactor provider/search code into a library/JSON interface.
3. Add a Kotlin JNI/IPC bridge implementing `core/MovieBoxEngine.kt`.
4. Add an Android media player (for example AndroidX Media3) and safely pass stream URLs, headers, and subtitles.
5. Test on a real Android device, including failures, provider changes, storage permissions, and playback.

## License / attribution

This starter UI is provided as a separate example project. MovieBox-TUI is a third-party project dual-licensed under MIT or Apache-2.0; review its upstream license files and comply with attribution/license requirements before bundling or redistributing its code or binaries. Use only media sources you are legally allowed to access.
