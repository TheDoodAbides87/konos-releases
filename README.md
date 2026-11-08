# VMP — Vibes Media Player

Releases of VMP, and its pacman repository. The source code lives in a
separate repository; this one holds only the built packages.

## What VMP is

**VMP is an overhaul of VLC.** It is VLC media player with a new interface:
playback, codecs, subtitles, discs, streaming and all audio/video effects come
from **libVLC 3**, the engine inside VLC, made by the
[VideoLAN](https://www.videolan.org/) project. VMP replaces the interface
around it, written from scratch in C++/Qt 6.

## Credits

**The design is by [Juxtopposed](https://www.youtube.com/@juxtopposed)**, from
the video [*I Redesigned VLC After 25 Years*](https://youtu.be/ERFeOgqk324).
VMP builds that redesign as a working player; each release works through a
part of the video.

- Playback engine: [VLC / libVLC](https://www.videolan.org/vlc/) by VideoLAN
  and the VLC contributors (LGPL 2.1 or later). The AppImage bundles libVLC
  and its plugins unchanged.
- Interface toolkit: [Qt 6](https://www.qt.io/) (LGPL 3); tags via
  [TagLib](https://taglib.org/).

VMP is an independent project. It is not affiliated with or endorsed by
VideoLAN or Juxtopposed. "VLC" and the VLC cone are trademarks of VideoLAN.

## Installing

### Arch Linux (pacman)

Add to `/etc/pacman.conf`:

```ini
[vmp]
SigLevel = Optional TrustAll
Server = https://github.com/TheDoodAbides87/vmp-releases/releases/latest/download
```

then `sudo pacman -Sy vmp`. `sudo pacman -Syu` keeps it up to date.

### Other Linux distributions (AppImage)

Download `VMP-<version>-x86_64.AppImage` from the
[latest release](https://github.com/TheDoodAbides87/vmp-releases/releases/latest),
make it executable (`chmod +x`) and run it. VMP offers **Update Now** when a
new version is out.

VMP's own code is under the [MIT licence](LICENSE).
