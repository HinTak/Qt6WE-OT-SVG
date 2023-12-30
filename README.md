`rpm --rebuild ...` takes 5 hours 23 minutes (NINJAFLAGS=-v -j4):

```
2023-12-29T14:56:18
2023-12-29T20:19:16
```

```
qt6-qtwebengine-6.7.0-1  6.7.0 118.0.5993.124 119.0.6045.160
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
