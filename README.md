# Konos — Konos Media Player

Releases of Konos, and its pacman repository. The source code lives in a
separate repository; this one holds only the built packages.

> **Early development.** Konos is a beta that changes often: features move,
> settings may reset, and things can break between releases. Keep that in mind
> before relying on it.

## What Konos is

**Konos is an overhaul of VLC.** It is VLC media player with a new interface:
playback, codecs, subtitles, discs, streaming and all audio/video effects come
from **libVLC 3**, the engine inside VLC, made by the
[VideoLAN](https://www.videolan.org/) project. Konos replaces the interface
around it, written from scratch in C++/Qt 6.

## Credits

**The design is by [Juxtopposed](https://www.youtube.com/@juxtopposed)**, from
the video [*I Redesigned VLC After 25 Years*](https://youtu.be/ERFeOgqk324).
Konos builds that redesign as a working player; each release works through a
part of the video.

- Playback engine: [VLC / libVLC](https://www.videolan.org/vlc/) by VideoLAN
  and the VLC contributors (LGPL 2.1 or later). The AppImage bundles libVLC
  and its plugins unchanged.
- Interface toolkit: [Qt 6](https://www.qt.io/) (LGPL 3); tags via
  [TagLib](https://taglib.org/).

Konos is an independent project. It is not affiliated with or endorsed by
VideoLAN or Juxtopposed. "VLC" and the VLC cone are trademarks of VideoLAN.

## Installing

### Arch Linux (pacman)

Add to `/etc/pacman.conf`:

```ini
[konos]
SigLevel = Optional TrustAll
Server = https://github.com/TheDoodAbides87/konos-releases/releases/latest/download
```

then `sudo pacman -Sy konos`. `sudo pacman -Syu` keeps it up to date.

### Other Linux distributions (AppImage)

Download `Konos-<version>-x86_64.AppImage` from the
[latest release](https://github.com/TheDoodAbides87/konos-releases/releases/latest),
make it executable (`chmod +x`) and run it. Konos offers **Update Now** when a
new version is out.

Konos's own code is under the [MIT licence](LICENSE).

Konos was called VMP (Vibes Media Player) up to 0.5. A `pacman.conf` that
still says `[vmp]` keeps working and moves over to the `konos` package.
