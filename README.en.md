# NeoMusic for phone

The phone version of NeoMusic, for the NeoDex Android app. It keeps the same library as NeoMusic on PC (same id `neodex.music`): your playlists and favorites sync between both.

## What it keeps from the PC

The same code as NeoMusic on PC, with its 18 themes, the pixel-art turntable, covers, progress bar, playlists, favorites, trash, statistics, 33 achievements, levels, sleep mode and widget.

## What changes on phone

- **☰ menu** at the top left: playlists and the library open in a drawer, which closes when you pick something.
- The turntable is at the top, the list below (scroll). **Tap** a track to play it, **long-press** to open its menu.
- Sound goes through the NeoDex YouTube player and keeps playing with the screen off; the notification has play / pause, previous and next.
- "Offline" playlists play online on the phone; the PC downloads their files as usual.
- No equalizer, balance, spectrum or waveform (YouTube sound does not go through the page), no keyboard shortcuts, no file, artist, capsule or MuPlayer import, no alarm, no recommendations (they come from Deezer through the PC). Only YouTube tracks play.

## Permissions

- **storage**: keep the library;
- **music**: YouTube search and the NeoDex player on phone;
- **network:i.ytimg.com**: track covers;
- **widget**: the home widget.

## For developers

The repository is named like the PC one with `-phone` at the end. The `catsync.js` tool (`outils-publication` folder) reads its latest signed Release and writes it to the catalog's `phone` field; the Android app then installs that version instead of the PC one. Sound goes through the NeoDex phone music service (`neo.musicSearch`, `neo.musicInfo`, `neo.musicPlayer`, `neo.onMusicPlayer`), described in `NeoDyme/mobile/shell/neo-music.js`.
