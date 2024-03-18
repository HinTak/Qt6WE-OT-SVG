# Chromium/QT WebEngine SVG in OpenType support

This is a set of QT WebEngine patches to address
Chromium [Issue 306078: SVG in OpenType support](https://bugs.chromium.org/p/chromium/issues/detail?id=306078).
It was first done for QT 6.6/m112, then moved to QT 6.7 Beta 1/m118. After that, work commences instead with Chromium Stable
(m120 at the time of writing) at [Chromium OT-SVG patches](https://github.com/HinTak/chromium-mod-CI).

This set of patches modifies the libQt6WebEngine* libraries in the typical QT6 installation.
Tested with the QT6 browser example in [minimal web browser collections](https://github.com/HinTak/minimal-web-browsers/).

Discussions in [Chromium OT-SVG patches](https://github.com/HinTak/chromium-mod-CI).

## misc

`rpm --rebuild ...` takes 5 hours 23 minutes (NINJAFLAGS=-v -j4):

```
2023-12-29T14:56:18
2023-12-29T20:19:16
```

```
qt6-qtwebengine-6.7.0-1  6.7.0 	Chrome based:  118.0.5993.124 	Chrome patched:  119.0.6045.160 # beta 1
qt6-qtwebengine-6.7.0-2b 6.7.0 	Chrome based:  118.0.5993.124 	Chrome patched:  120.0.6099.109 # beta 2
qt6-qtwebengine-6.7.0-3b 6.7.0 	Chrome based:  118.0.5993.124 	Chrome patched:  120.0.6099.224 # beta 3
qt6-qtwebengine-6.7.0-3d 6.7.0 	Chrome based:  118.0.5993.220 	Chrome patched:  122.0.6261.58  # rc
```

github container inherited environment:

```
HOME=/github/home
GITHUB_ACTIONS=true
CI=true
```

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 60574024  26613996  70% /
```

`dnf builddep`: Total download size: 420 M

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 62932100  24255920  73% /
```

After build (--noclean):

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 79964496   7223524  92% /
```
```
$ xzcat .../qtwebengine-everywhere-src-6.7.0-beta1.tar.xz | dd of=/dev/null
7276320+0 records in
7276320+0 records out
3725475840 bytes (3.7 GB, 3.5 GiB) copied, 53.3683 s, 69.8 MB/s
```
