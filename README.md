This repository focuses on supporting SVG in OpenType fonts within the Chromium/Qt WebEngine environment.

- Topics of Interest: Focused on enhancing font rendering and web technologies using OpenType-SVG within the Qt6 framework.

# Chromium/QT WebEngine SVG in OpenType support
[![CI](https://github.com/HinTak/Qt6WE-OT-SVG/actions/workflows/ci.yml/badge.svg)](https://github.com/HinTak/Qt6WE-OT-SVG/actions/workflows/ci.yml)


This is a set of QT WebEngine patches to address
Chromium [Issue 306078: SVG in OpenType support](https://bugs.chromium.org/p/chromium/issues/detail?id=306078).
See the latest release on what QT release it supports. I try to patch QT6 beta's and release candidates
before they come out.

Here is the table of the latest patched builds, and their reported chrome versions:

```
                               	               130.0.6723.192 	                 137.0.7151.68  # v6.10.0-beta2
                               	               130.0.6723.192 	                 136.0.7103.114 # v6.10.0-beta1

qt6-qtwebengine-6.9.1-1g 6.9.1 	Chrome based:  130.0.6723.192 	Chrome patched:  136.0.7103.114 # Qt:  6.9.1      PyQt:  6.9.0
qt6-qtwebengine-6.9.0-1f 6.9.0 	Chrome based:  130.0.6723.192 	Chrome patched:  133.0.6943.141 # Qt:  6.9.0      PyQt:  6.9.0
qt6-qtwebengine-6.9.0-1e 6.9.0 	Chrome based:  130.0.6723.192 	Chrome patched:  133.0.6943.141 # 6.9.0 Qt:  6.8.2      PyQt:  6.8.1.dev2502011625
qt6-qtwebengine-6.9.0-1d 6.9.0 	Chrome based:  130.0.6723.192 	Chrome patched:  133.0.6943.141 # rc
qt6-qtwebengine-6.9.0-1c 6.9.0 	Chrome based:  130.0.6723.192 	Chrome patched:  132.0.6834.159 # 6.9.0 beta 3 Qt: 6.8.2 (also qtwebengine/CHROMIUM_VERSION)
qt6-qtwebengine-6.9.0-1b 6.9.0 	Chrome based:  126.0.6478.165 	Chrome patched:  129.0.6668.58  # 6.9.0 beta 2 qt 6.8.2
qt6-qtwebengine-6.9.0-1a 6.9.0 	Chrome based:  126.0.6478.165 	Chrome patched:  129.0.6668.58  # 6.9.0 beta 2

                         6.8.2 	               122.0.6261.171 	                 132.0.6834.111 # from qtwebengine/CHROMIUM_VERSION

qt6-qtwebengine-6.8.1-3b 6.8.1 	Chrome based:  122.0.6261.171 	Chrome patched:  131.0.6778.70  # fedora 2->3 - Add optional deps/libva for VA-API support/qtwebsockets for websockets
qt6-qtwebengine-6.8.1-2a 6.8.1 	Chrome based:  122.0.6261.171 	Chrome patched:  131.0.6778.70  # 6.8.1
qt6-qtwebengine-6.8.0-1h 6.8.0 	Chrome based:  122.0.6261.171 	Chrome patched:  129.0.6668.70  # release, fc41 + 6.8.0 qtbase rebuild
qt6-qtwebengine-6.8.0-1g 6.8.0 	Chrome based:  122.0.6261.171 	Chrome patched:  129.0.6668.70  # release
qt6-qtwebengine-6.8.0-1f 6.8.0 	Chrome based:  122.0.6261.171 	Chrome patched:  129.0.6668.58  # rc
qt6-qtwebengine-6.8.0-1e 6.8.0 	Chrome based:  122.0.6261.171 	Chrome patched:  127.0.6533.99  # beta 4
qt6-qtwebengine-6.8.0-1d 6.8.0 	Chrome based:  122.0.6261.171 	Chrome patched:  124.0.6367.202 # beta 3
qt6-qtwebengine-6.8.0-1c 6.8.0 	Chrome based:  122.0.6261.171 	Chrome patched:  124.0.6367.202 # beta 2
qt6-qtwebengine-6.8.0-1a 6.8.0 	Chrome based:  118.0.5993.220 	Chrome patched:  122.0.6261.128 # beta 1

                         6.7.3 	               118.0.5993.220 	                 129.0.6668.58
                         6.7.2 	               118.0.5993.220 	                 125.0.6422.142
                         6.7.1 	               118.0.5993.220 	                 124.0.6367.202

qt6-qtwebengine-6.7.0-3f 6.7.0 	Chrome based:  118.0.5993.220 	Chrome patched:  122.0.6261.128 # release
qt6-qtwebengine-6.7.0-3e 6.7.0 	Chrome based:  118.0.5993.220 	Chrome patched:  122.0.6261.128 # rc2
qt6-qtwebengine-6.7.0-3d 6.7.0 	Chrome based:  118.0.5993.220 	Chrome patched:  122.0.6261.58  # rc
qt6-qtwebengine-6.7.0-3b 6.7.0 	Chrome based:  118.0.5993.124 	Chrome patched:  120.0.6099.224 # beta 3
qt6-qtwebengine-6.7.0-2b 6.7.0 	Chrome based:  118.0.5993.124 	Chrome patched:  120.0.6099.109 # beta 2
qt6-qtwebengine-6.7.0-1  6.7.0 	Chrome based:  118.0.5993.124 	Chrome patched:  119.0.6045.160 # beta 1
```

It was first done for QT 6.6/m112, then moved to QT 6.7 Beta 1/m118.
See also [QT Webengine tracker issue](https://bugreports.qt.io/browse/QTBUG-120543).
After that, work commences instead with Chromium Stable
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

```
# 6.8.0 beta3 requires just 5 hours 35 minutes and 17GB to build:
2024-08-15T10:20:06.8607133Z
2024-08-15T10:30:57.9374055Z overlay         75085112 45067348  30001380  61% /
2024-08-15T10:31:57.8326410Z overlay         75085112 47385152  27683576  64% /
2024-08-15T10:32:04.0178062Z overlay         75085112 47403584  27665144  64% /
2024-08-15T15:54:22.2197374Z overlay         75085112 64229784  10838944  86% /
2024-08-15T15:54:44.1414143Z

# 6.8.0 beta2 requires just over 6 hours and 18GB to build:
2024-07-27T21:18:33.2668337Z
2024-07-27T21:28:50.0503731Z overlay         76026616 54672064  21338168  72% /
2024-07-27T21:29:49.3830630Z overlay         76026616 57067560  18942672  76% /
2024-07-28T03:22:31.6752030Z overlay         76026616 74954596   1055636  99% /
2024-07-28T03:22:54.7418005Z
```
