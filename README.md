`rpm --rebuild ...` takes 5 hours 23 minutes (NINJAFLAGS=-v -j4):

```
2023-12-16T23:51:23
2023-12-17T05:14:09

2023-12-21T11:22:12
2023-12-21T16:39:38

2023-12-21T19:08:36
2023-12-22T00:17:21

2023-12-23T02:52:24
2023-12-23T08:02:48

2023-12-23T16:00:51
2023-12-23T21:15:07
```

```
qt6-qtwebengine-6.6.1-1s 6.6.1 112.0.5615.213 119.0.6045.123
```

github container inherited environment:

```
HOME=/github/home
GITHUB_ACTIONS=true
CI=true
```

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 60572200  26615820  70% /
```

source rpm is 378MB.

`dnf builddep`: Total download size: 420 M

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 62928520  24259500  73% /
```

After build (--noclean):

```
Filesystem     1K-blocks     Used Available Use% Mounted on
overlay         87204404 77630316   9557704  90% /
```
```
/github/home/rpmbuild/BUILD/qtwebengine-everywhere-src-6.6.1/redhat-linux-build/src/core/RelWithDebInfo/x86_64/gen/third_party/blink/renderer/platform/platform_jumbo_29.cc
```

```
$ xzcat .../qtwebengine-everywhere-src-6.7.0-beta1.tar.xz | dd of=/dev/null
7276320+0 records in
7276320+0 records out
3725475840 bytes (3.7 GB, 3.5 GiB) copied, 53.3683 s, 69.8 MB/s
```
