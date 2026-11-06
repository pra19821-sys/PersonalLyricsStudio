# Personal Lyrics Studio (starter APK project)

A personal Android music-library and manual-lyrics-sync starter project.

## Included in this first build
- Reads music indexed by Android MediaStore (internal/shared storage and SD card media that Android indexes).
- Select a track and play/pause/stop it inside this app.
- Choose a photo from your phone's gallery for each song; the chosen photo is remembered for that track and shown in the player screen.
- Type lyric lines and tap **Timestamp** while the song plays to capture the current playback position.
- Save lyric lines locally against the selected track.
- Export the saved lines as LRC text using Android's share sheet.
- Optional floating overlay that displays the current manually-timed lyric line while this app's player is playing.

## Build an APK with GitHub Actions
1. Create a GitHub repository named `PersonalLyricsStudio`.
2. Upload the contents of this folder to the repository root (not the containing folder).
3. Open **Actions** and enable workflows if GitHub asks.
4. Run **Android APK** using **Run workflow**, or push a commit to `main`.
5. Download the `PersonalLyricsStudio-APK` artifact from the completed workflow and install `app-debug.apk`.

## Notes / current limitations
- This is a functional starter, not a finished Musixmatch clone.
- Floating lyrics currently follow songs played by this app's built-in player. Controlling/recognising playback from YouTube or other music apps is not included in this first version.
- The first version captures timestamps when you tap the button; it does not generate or synchronize lyrics automatically.
- Lyrics and each song's selected background photo reference are stored locally on the device. LRC export uses the Android share sheet.
- The photo picker uses Android's document picker, so the app does not need broad gallery access.
- Android may require the user to grant the **Display over other apps** permission for the floating overlay.
- Music files must be visible to Android's MediaStore. Some SD-card or app-private audio may not appear.
- The project uses Android's basic MediaPlayer. A later iteration can add waveform/timestamp editing, draggable overlay, font/color/opacity controls, better library browsing, and more robust background playback.
